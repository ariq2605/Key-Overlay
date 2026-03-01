# Key Overlay

A lightweight OBS-compatible keyboard & mouse input visualizer for streamers.

---

## Running from Source

### Requirements

- Python 3.8+
- pynput

Install dependencies:

```bash
pip install pynput
```

### Linux Extra Steps

On Linux, `pynput` requires access to input devices which is restricted by default.

**1. Install tkinter** (it's not always bundled with Python on Linux):

```bash
# Debian/Ubuntu
sudo apt install python3-tk

# Arch
sudo pacman -S tk

# Fedora
sudo dnf install python3-tkinter
```

**2. Add yourself to the `input` group** (required for global key/mouse listening):

```bash
sudo usermod -aG input $USER
```
Log out and back in for this to take effect.

**3. If using Wayland**, pynput may not capture input globally. Switch to an X11 session from your login screen, or set this environment variable before running:

```bash
GDK_BACKEND=x11 python main.py
```

### Run

```bash
python main.py
```

---

## Windows

Just run the `.exe` — no setup needed.
