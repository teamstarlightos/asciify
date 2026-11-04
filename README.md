# asciify

Turn an image into ASCII art for use with fastfetch (or anywhere else).

## Install

```bash
sudo apt install python3-pil
install -m 755 asciify ~/.local/bin/asciify
```

## Usage

```bash
asciify logo.png -w 34 -o ~/.config/fastfetch/logo.txt
fastfetch --logo ~/.config/fastfetch/logo.txt
```

Options: `-w` width, `-t` threshold (0-255), `-c` character, `--invert`, `--color`, `-o` output file.
