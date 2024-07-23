# CATV - CSV Advanced Terminal Viewer

CATV is a extremely simple bash script that allows you to view (`less`) CSV files in a formatted table directly in your terminal for exploratory purposes.

## Features

- Select specific columns to display.
- Automatically adjusts column widths.
- Respects terminal width constraints.
- Supports scrolling for large data.

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/albertoperdomo2/catv.git /tmp/catv
   ```

2. Move the script:
   ```
   sudo mv /tmp/catv/catv /usr/local/bin
   ```

That's it!

## Usage

```
catv <file.csv> -c col_name1,col_name2,col_name3 [-h <cols_number>]
```

Examples:
```
catv example/data.csv -c id,name,email -h 2
```

## Configuration

You can set the `CATV_LINE_LENGTH` environment variable to change the maximum line length:

```
CATV_LINE_LENGTH=120 catv example/data.csv -c id,name,email
```

Or just set it in your `~/.zshrc`. 

## Requirements

- Bash
- less (usually pre-installed on most Unix-like systems)

## Caveats
`catv` is not fast nor it is intended to be, since it is only a simple visualiztion tool for quick exploring. Therefore, the `-h` flag lets you limit the amount of lines of the original file that you want to read.
