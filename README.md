# Termux Custom Keys

Custom 5-row extra keys layout for Termux on Android.

### Layout

```text
F1 F2 F3 F4 F5 F6 SHIFT
F7 F8 F9 F10 F11 F12 FN
INS DEL BKSP ENTER KEYBOARD SPACE '
END PGUP PGDN ↓ ↑ ← →
ESC TAB CTRL ALT HOME - DRAWER
```

### Installation

Run this command in Termux:

```bash
mkdir -p ~/.termux && sed -i '/^[[:space:]]*extra-keys[[:space:]]*=/d' ~/.termux/termux.properties && printf "%s\n" "extra-keys = [['F1','F2','F3','F4','F5','F6','SHIFT'],['F7','F8','F9','F10','F11','F12','FN'],['INS','DEL','BKSP','ENTER','KEYBOARD','SPACE','APOSTROPHE'],['END','PGUP','PGDN','DOWN','UP','LEFT','RIGHT'],['ESC','TAB','CTRL','ALT','HOME',{key: '-', popup: '|'},'DRAWER']]" >> ~/.termux/termux.properties && termux-reload-settings
```