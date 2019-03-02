# Personal Build of ST - Simple (Suckless) Terminal

This version is forked from [Luke Smith's](https://github.com/LukeSmithxyz/st).

This is the [Simple (Suckless) Terminal (st)](https://st.suckless.org/) with some additional features:

* compatibility with `Xresources` and `pywal` for dynamic colors
* default [gruvbox](https://github.com/morhetz/gruvbox) colors otherwise
* transparency/alpha, which is also adjustable from `~/.Xresources`
* default font is system "mono" at 16pt, meaning the font will match your system font
* very useful keybinds including:
  * Alt+c to copy, Alt+v to paste or Alt+p to paste from primary
  * Alt+l to feed all urls on screen to dmenu, so the user can choose and follow one (requires `xurls` and `dmenu` installed)
  * Alt+Shift+k/Alt+Shift+j to zoom in and out (Alt+Shift+u/Alt+Shift+d for larger intervals, Alt+Home to reset)
  * Alt+k/Alt+↑ and Alt+j/Alt+↓ to move up/down in the terminal (Shift+MouseWheel do the same)
  * Alt+u and Alt+d scroll back/forward in history one page at a time (Alt+PageUp and Alt+PageDown do the same)
+ vertcenter
+ scrollback
+ updated to latest version 0.8.1

## Installation

```
git clone https://github.com/remigourdon/st.git
cd st/
sudo make install
```

You can also copy the `.desktop` file in `~/.local/share/applications/`.

### Ubuntu Dependencies

On ubuntu you may need to install the following packages to compile (you may remove them after the install is done):

```
sudo apt install libx11-dev libxft-dev
```

## .Xresources Configuration

For many key variables, this build of `st` will look for X settings set in either `~/.Xdefaults` or `~/.Xresources`.
You must run `xrdb` on one of these files to load the settings.

For example, you can define your desired fonts, transparency or colors:

```
*.font:	Liberation Mono:pixelsize=12:antialias=true:autohint=true;
*.alpha: 150
*.color0: #111
...
```

The `alpha` value (for transparency) goes from *0* (transparent) to *255* (opaque).
