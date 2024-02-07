# Configure Ubuntu

Config for a fresh Ubuntu installation (read: my research workstation).

## OS Settings

- **Appearance**
  - **Style** = `Dark`
    - **Color** = blue
  - **Desktop Icons**
    - **Size** = `Small`
    - **Position of New Icons** = `Top Left`
  - **Dock**
    - **Icon size** = `32`
    - **Show on** = `All displays`
    - **Position on screen** = `Bottom`
    - **Configure dock behavior**
      - **Show Volumes and Devices** = `false`
- **Power**
  - **Power Mode** = `Performance`
  - **Power Saving Options**
    - **Dim Screen** = `false`
    - **Screen Blank** = `Never`
  - **Suspend & Power Button**
    - **Power Button Behavior** = `Nothing`
- **Screen Display**
  - **Night Light**
    - **Night Light** = `true`
    - **Color Temperature** = `Less Warm`
- **Language and Region**
  - **My Account**
    - **Language**
      - **Language** = `English (Canada)`
    - **Formats**
      - **Formats** = `Canada`
  - **Login Screen**
    - **Language**
      - **Language** = `English (Canada)`
    - **Formats**
      - **Formats** = `Canada`

## Connecting to eduroam at the University of Waterloo

1. Follow the [Ubuntu-specific instructions](https://uwaterloo.ca/mechanical-mechatronics-engineering-information-technology/frequently-asked-questions-faq/wireless-eduroam#Ubuntu) provided by MME-IT.

## Dock

1. Files
2. System Monitor
3. Calculator
4. Prospect Mail
5. Slack
6. Teams for Linux
7. Zoom
8. Spotify
9. Typora
10. Visual Studio Code
11. Firefox

## Applications

Uninstall the following from Ubuntu Software:

- AisleRiot Solitaire
- Mahjongg
- Mines
- Sudoku

Install the following from Ubuntu Software:

- GNOME Tweaks
- Hardware Sensors Indicator (the one by Alex Murray)
- Prospect Mail
- Slack
- Spotify
- Teams for Linux
- Typora
- Visual Studio Code
- Xournal++

Install the following via web download:

- Zoom

## GNOME Tweaks

- **General**
  - **Suspend when laptop lid is closed** = `false`
- **Keyboard & Mouse**
  - **Mouse**
    - **Middle Click Paste** = `false`
  - **Touchpad**
    - **Mouse Click Emulation** = `Area`
- **Top Bar**
  - **Clock**
    - **Weekday** = `true`
    - **Date** = `true`
    - **Seconds** = `true`

## Disable Middle Click Paste

Middle-click paste is the most infuriating GTK feature.
[Patching it out of GTK](https://web.archive.org/web/20211025212803/https://app.assembla.com/spaces/slipstream/wiki/Disabling_GTK%27s_middle_mouse_button_functionality) is beyond my comfort zone, but there is an easier solution.
Since I never use middle-click anyways, we can just remap it to null.
The Ubuntu Wiki provides [a tutorial](https://wiki.ubuntu.com/X/Config/Input#Example:_Disabling_middle-mouse_button_paste_on_a_scrollwheel_mouse) for how to do exactly this via the `xinput` command:
```sh
xinput set-button-map "${DEVICE}" 1 0
```

The button maps modified using `xinput` do not persist through reboots.
To set them again after each startup, place the commands in the `~/.xstartup` file.

The [`.xstartup`](./.xstartup) file provided automatically goes through a list (WIP) of known mouse/trackpad devices and remaps all of their middle-clicks to the null action.

> Alternatively, one could loop through all pointer devices from `xinput list`, but I prefer to be a bit more explicit.

## Disable Emoji Keyboard

The emoji keyboard is the second-most annoying feature.

```sh
sudo apt install dbus-x11
sudo ibus-setup
```

Then, in the IBus Preferences window:

- **Emoji**
  - **Keyboard Shortcuts**
    - **Emoji annotation:**
      - delete all keyboard shortcuts

```sh
sudo ibus restart
# or, if you don't want IBus to keep running
sudo ibus exit
```

## Configure APT

Before the first time you use an APT command (such as `apt-get`), run the following command:

```sh
sudo dpkg --configure -a
```

Afterwards, before installing packages you should always first run

```sh
sudo apt-get update
```

## Fix MP3 and Other File Formats

```sh
sudo apt-get install ubuntu-restricted-extras
```

Use the arrow keys to navigate and accept any license agreement pop-ups.

## Clipboard via Terminal

```sh
sudo apt-get install xclip
```

## Troubleshooting

### Ubuntu Software Hangs

> See also: [Ubuntu Software not loading](https://askubuntu.com/a/1291111).

```sh
killall snap-store
```
