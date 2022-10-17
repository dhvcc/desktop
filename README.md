# Pretty and usefull GNOME desktop

**This is written for Fedora 36 GNOME, different distros may require additional settings **

"before GIF"
"after GIF"

## Gnome settings

```bash
# Disable hot corners
gsettings set org.gnome.desktop.interface enable-hot-corners false
# Show app button on the top/left
gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top true

# Set kitty as default terminal
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
# Change layout on Alt+Shift
gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']" >> /etc/profile
```

## Utilities

1. gnome-shell-extensions
2. gnome-tweaks
3. dconf editor

```bash
sudo dnf install gnome-extensions-app \
  gnome-tweaks \
  dconf-editor
```

## Flatpack

[Install]()
[Search for apps]()

### Apps

1. Celluloid
   Media player (frontend for MPV player)
2. Touché
   Configuration UI for `touchegg` gesture recognizer
3. Peek / Kooha
   Media recorder if you don't like GNOME's new default

## Extensions and settings

1. Blur-my-shell
   "Expandable preview of before and after"
2. Dash to Dock
3. GSConnect
4. Tiling Assistant
5. Just Perfect
6. Media Controls
7. Freon
8. User Themes
9. Sound IO Chooser
10. Soft Brightness
12. Gnome Email Noifications

### Settings

Idk how to dump gnome extension settings

## Icons and app gnome-like themes

1. yaru-theme
   ```bash
   sudo dnf install yaru-themes
   ```
2. [Firefox gnome theme](https://github.com/rafaelmardojai/firefox-gnome-theme) (can be themed with Gradience/CSS)
3. [Telegram theme](https://github.com/Fenimoure/Telegram-Adwaita-Dark-theme) (doesn't follow yaru colors)

## Firefox extensions

1. uBlock Origin (Ad blocker)
2. Privacy Badger (Tracker blocker)
3. ClearURLs (remove useless tracking meta data from urls)
4. BitWarden (password manager)
6. Dark Reader (universal dark mode support)
7. Auto Tab Discard (save RAM on tabs you're not using)
8. CustomCSS (inject custom CSS on any site)
9. Vimium C (best vim plugin for Firefox)

