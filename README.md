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

# Allow backwards alt tabbing with Alt+Shift+Tab
gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<alt>Tab']"
gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<alt><shift>Tab']"

# Set kitty as default terminal
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
# Change layout on Alt+Shift
gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']" >> /etc/profile
```

## Utilities

1. [Extension manager](https://github.com/mjakeman/extension-manager) (a replacement for gnome-extensions-app with a beautiful UI and a feature to search without using your browser)
   To install it use [Flatpak](#Flatpak)
2. gnome-tweaks
3. dconf editor

```bash
sudo dnf install \
  gnome-tweaks \
  dconf-editor
```

# Apps

1. Gradience (libadwaita theming)
2. [Youtube Music](https://github.com/th-ch/youtube-music) (electron client for Linux to not use a PWA)
3. [Google Chat](https://github.com/ankurk91/google-chat-electron) (same as for yt music, but for for google chat)

## Flatpak

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

