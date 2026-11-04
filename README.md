# asciify

Turn an image into ASCII art for use with fastfetch (or anywhere else).

## Supported formats

asciify uses Pillow to open images, so it supports any format Pillow can read, including PNG, JPG/JPEG, WebP, GIF, BMP, and TIFF. Transparent images are flattened onto a white background first.

## Install

```bash
sudo apt install python3-pil
install -m 755 asciify ~/.local/bin/asciify
```

## Usage

```bash
asciify your-image.png -w 34 -o ~/.config/fastfetch/logo.txt
fastfetch --logo ~/.config/fastfetch/logo.txt
```

Replace `your-image.png` with the path to your image in any supported format.

## Options

- `-w`, `--width`: width in columns (default 34)
- `-t`, `--threshold`: brightness cutoff, 0-255 (default 128)
- `-c`, `--char`: character to draw with (default `@`)
- `--invert`: swap filled and empty areas
- `--color`: ANSI color code (default 97, bright white; use 0 for none)
- `-o`, `--out`: write to a file instead of stdout
