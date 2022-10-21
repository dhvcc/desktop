# Pretty and usefull GNOME desktop

**This is written for Fedora 36/37 GNOME, different distros may require additional settings**

**Fedora note**
[Enabling RPMFusion](https://docs.fedoraproject.org/en-US/quick-docs/setup_rpmfusion/#proc_enabling-the-rpmfusion-repositories-using-command-line-utilities_enabling-the-rpmfusion-repositories) will make your life much easier

## Preview

TODO

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

# OPTIONAL

# Set kitty as default terminal
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
# Change layout on Alt+Shift
gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']" >> /etc/profile
```

## Utilities

1. [Gnome shell extensions](https://wiki.gnome.org/action/show/Projects/GnomeShellIntegration/Installation?action=show&redirect=Projects%2FGnomeShellIntegrationForChrome%2FInstallation)
2. [Extension manager](https://github.com/mjakeman/extension-manager) (a replacement for gnome-extensions-app with a beautiful UI and a feature to search without using your browser)
   To install it use [Flatpak](#Flatpak)
3. [gnome-tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks)
4. [dconf editor](https://gitlab.gnome.org/GNOME/dconf-editor)

```bash
sudo dnf install \
  gnome-tweaks \
  dconf-editor
```

# Apps

1. [Youtube Music](https://github.com/th-ch/youtube-music) (electron client for Linux to not use a PWA)
2. [Google Chat](https://github.com/ankurk91/google-chat-electron) (same as for yt music, but for for google chat)

## Flatpak

[Install](https://flatpak.org/setup/)
[Search for apps](https://flathub.org/home)

### Apps

1. [Gradience](https://flathub.org/apps/details/com.github.GradienceTeam.Gradience) (libadwaita theming)
2. [Celluloid](https://flathub.org/apps/details/io.github.celluloid_player.Celluloid)
   Media player (frontend for MPV player)
3. [Touché](https://flathub.org/apps/details/com.github.joseexposito.touche)
   Configuration UI for `touchegg` gesture recognizer
4. [Peek](https://flathub.org/apps/details/com.uploadedlobster.peek) / [Kooha](https://flathub.org/apps/details/io.github.seadve.Kooha)
   Media recorder if you don't like GNOME's new default

## Extensions and settings

1. Blur-my-shell
   "Expandable preview of before and after"
2. Dash to Dock
3. GSConnect
4. Bluetooth Quick Connect
5. Tiling Assistant
6. Just Perfect
7. Media Controls
8. Freon
9. User Themes
10. Sound IO Chooser
11. Soft Brightness
13. Gnome Email Noifications

### Settings

TODO
Idk how to dump gnome extension settings (`dconf dump`/`load` ?)

## Icons and app gnome-like themes

1. [yaru-theme](https://github.com/ubuntu/yaru)
   ```bash
   sudo dnf install yaru-themes
   ```
2. [Firefox gnome theme](https://github.com/rafaelmardojai/firefox-gnome-theme) (can be themed with Gradience/CSS)
3. [Telegram theme](https://github.com/Fenimoure/Telegram-Adwaita-Dark-theme) (doesn't follow yaru colors)

# Browsers and codecs

There are license problems with bundling codecs with the OS by default. Make sure to enable RPMFusion repositories

### Chromium

There's already chromium bundled with all of the codecs.

```bash
sudo dnf install chromium-freeworld
```

### Firefox

You need to install codecs separately from RPMFusion repository.

```bash
sudo dnf install ffmpeg-libs
```

## Firefox extensions

1. uBlock Origin (Ad blocker)
2. Privacy Badger (Tracker blocker)
3. ClearURLs (remove useless tracking meta data from urls)
4. BitWarden (password manager)
6. Dark Reader (universal dark mode support)
7. Auto Tab Discard (save RAM on tabs you're not using)
8. CustomCSS (inject custom CSS on any site)
9. Vimium C (best vim plugin for Firefox)
