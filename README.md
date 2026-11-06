# asciify

Turn any image into ASCII art for fastfetch, straight from your terminal.

## Supported formats

asciify uses Pillow to open images, so it supports any format Pillow can read, including PNG, JPG/JPEG, WebP, GIF, BMP, and TIFF. Transparent pixels are placed on a black background by default (use `--bg white` to change it).

## Install

    sudo apt install python3-pil
    install -m 755 asciify ~/.local/bin/asciify

## Usage

    asciify your-image.png -w 34 -o ~/.config/fastfetch/logo.txt
    fastfetch --logo ~/.config/fastfetch/logo.txt

## Options

- `-w`, `--width`: width in columns (default 34)
- `-t`, `--threshold`: brightness cutoff, 0-255 (default 128)
- `-c`, `--char`: character to draw with (default `@`)
- `--bg`: background for transparent pixels, `black` or `white` (default `black`)
- `--invert`: swap filled and empty areas
- `--color`: ANSI color code (default 97, bright white; use 0 for none)
- `-o`, `--out`: write to a file instead of stdout
