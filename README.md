# dwm — my build

My configuration of [dwm](https://dwm.suckless.org/), the suckless dynamic tiling window manager for X, version 6.2. Upstream's own README is kept as [README.suckless](README.suckless).

## Patches

- [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/) — the bar shows only tags that have windows on them ([diff](dwm-hide_vacant_tags-6.2.diff))
- [title colour](https://dwm.suckless.org/patches/titlecolor/) — the focused window's title gets its own colour scheme ([diff](dwm-titlecolor-20190206-6.2.diff))

## What's changed in config.h

- **Mod key is Alt** (`Mod1Mask`): `Alt+d` opens dmenu, `Alt+Return` opens a terminal (st), `Alt+q` closes a window, `Alt+Shift+Return` zooms.
- **Launchers on single keys:** `Alt+n` the nnn file manager, `Alt+p` my password manager ([pwm](https://github.com/gregoryjayuk/pwm)), `Alt+2` a bookmarks new-tab page ([newtab](https://github.com/gregoryjayuk/newtab)), `Alt+Super+b` bookmarks, `Alt+s` a screenshot, `Alt+v` the VPN, and the brightness keys mapped to fixed levels.
- **Look:** Fira Code 14, a black bar with purple borders and a green selected tag, icon-font tags, 2 px borders.

## Build

```bash
make
sudo make install
```

Needs Xlib, Xft and Xinerama headers. Edit `config.h` and rebuild to change anything; `config.def.h` is upstream's default for comparison.

Pairs with my [dmenu](https://github.com/gregoryjayuk/dmenu), [st](https://github.com/gregoryjayuk/st) and [dwmblocks](https://github.com/gregoryjayuk/dwmblocks) builds.
