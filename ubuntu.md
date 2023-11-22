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
4. Firefox
5. Visual Studio Code
6. Typora
7. Spotify
8. Slack
9. Prospect Mail

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
- Typora
- Visual Studio Code
- Xournal++

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

## Configure APT

Before the first time you use an APT command (such as `apt-get`), run the following command:

```sh
sudo dpkg --configure -a
```

Afterwards, before installing packages you should always first run

```sh
sudo apt-get update
```

## Troubleshooting

### Ubuntu Software Hangs

> See also: [Ubuntu Software not loading](https://askubuntu.com/a/1291111).

```sh
killall snap-store
```
