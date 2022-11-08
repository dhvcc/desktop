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
gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Alt>Tab']"
gsettings set org.gnome.desktop.wm.keybindings switch-windows-backward "['<Alt><Shift>Tab']"
# Disable default GNOME "application" switching, not windows. Conflicts with our keybindings
settings set org.gnome.desktop.wm.keybindings switch-applications  "[]"
settings set org.gnome.desktop.wm.keybindings switch-applications-backward  "[]"

# OPTIONAL

# Set kitty as default terminal
gsettings set org.gnome.desktop.default-applications.terminal exec kitty
# Change layout on Alt+Shift
gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']"
```

## Utilities

1. [Gnome shell extensions](https://wiki.gnome.org/action/show/Projects/GnomeShellIntegration/Installation?action=show&redirect=Projects%2FGnomeShellIntegrationForChrome%2FInstallation)
2. [Extension manager](https://github.com/mjakeman/extension-manager) (a replacement for gnome-extensions-app with a beautiful UI and a feature to search without using your browser). To install it use [Flatpak](#flatpak)
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

1. [Blur-my-shell](https://extensions.gnome.org/extension/3193/blur-my-shell/)
   "TODO: Add expandable preview of before and after"
2. [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
3. [GSConnect](https://extensions.gnome.org/extension/1319/gsconnect/)
4. [Bluetooth Quick Connect](https://extensions.gnome.org/extension/1401/bluetooth-quick-connect/)
5. [Tiling Assistant](https://extensions.gnome.org/extension/3733/tiling-assistant/)
6. [Just Perfection](https://extensions.gnome.org/extension/3843/just-perfection/)
7. [Media Controls](https://extensions.gnome.org/extension/4470/media-controls/)
8. [Freon](https://extensions.gnome.org/extension/841/freon/)
9. [User Themes](https://extensions.gnome.org/extension/19/user-themes/)
10. [Sound IO Chooser](https://extensions.gnome.org/extension/906/sound-output-device-chooser/) (only for GNOME <43)
11. [Soft Brightness](https://extensions.gnome.org/extension/1625/soft-brightness/)
13. [Gnome Email Noifications](https://extensions.gnome.org/extension/1230/gmail-message-tray/)

### Settings

TODO

Idk how to dump gnome extension settings (`dconf dump`/`load` ?)

## Icons and app gnome-like themes

1. [yaru-theme](https://github.com/ubuntu/yaru)
   ```bash
   sudo dnf install yaru-theme
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

1. [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) (Ad blocker)
2. [Privacy Badger](https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/) (Tracker blocker)
3. [ClearURLs](https://addons.mozilla.org/en-US/firefox/addon/clearurls/) (remove useless tracking meta data from urls)
4. [BitWarden](https://addons.mozilla.org/en-US/firefox/addon/bitwarden-password-manager/) (password manager, also available for mobile/web/desktop)
6. [Dark Reader](https://addons.mozilla.org/en-US/firefox/addon/darkreader/) (universal dark mode support)
7. [Auto Tab Discard](https://addons.mozilla.org/en-US/firefox/addon/auto-tab-discard/) (save RAM on tabs you're not using)
8. [CustomCSS](https://addons.mozilla.org/en-US/firefox/addon/customcss-injector/) (inject custom CSS on any site)
9. [Vimium C](https://addons.mozilla.org/en-US/firefox/addon/vimium-c/) (best vim plugin for Firefox)
