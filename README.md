# Wi-Fi Speed Widget

A tiny always-on-top desktop widget for Windows 11 that shows your PC's live
Wi-Fi download and upload speed, the network name, and a one-minute rolling
graph. It measures the Wi-Fi adapter only (Ethernet, VPN and virtual adapters
are ignored) and can start automatically with Windows.

Built with Python (tkinter + psutil). No admin rights needed.

## Install

1. Install [Python 3.9+](https://www.python.org/downloads/) (tick "Add python.exe to PATH").
2. Download this repository and open the `widget` folder.
3. In Command Prompt: `pip install psutil`
4. Double-click `wifi_widget.pyw` to run it.
5. To launch it with Windows: `python install_startup.py`
   (undo with `python install_startup.py --remove`).

Keep the files in a permanent folder: the startup shortcut points to them.

## Use

- Drag with the left mouse button; the position is remembered.
- Right-click for the menu (Quit).
- Tweak refresh rate, size, opacity and colors in the constants at the top of `wifi_widget.pyw`.

## As a Claude skill

`wifi-speed-widget.skill` (also unpacked in `skill/`) is a skill for Claude that
builds and sets up this widget when you ask for things like "show network usage
on the desktop". Upload the `.skill` file in Claude's skills settings.

## Limitations

- Windows only; it is a desktop overlay, not an official Windows 11 Widgets board widget.
- Shows this PC's own traffic, not the whole network.
- Speeds are shown in KB/s and MB/s, not megabits.

## License

MIT. See `LICENSE` (replace the name placeholder with yours).
