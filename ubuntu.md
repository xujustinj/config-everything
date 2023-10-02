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
  - **Suspend & Power Button**
    - **Power Button Behavior** = `Nothing`
- **Region & Language**
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

## Applications

### Bloatware

Uninstall the following from Ubuntu Software:

- AisleRiot Solitaire
- Mahjongg
- Mines
- Sudoku

### Spotify

Install via Snap Store.

### Visual Studio Code

1. Install via Snap Store.
2. Sign in with GitHub (sync only Settings).

### Slack

Install via Snap Store.

### Typora

Install via Snap Store.

## Troubleshooting

### Ubuntu Software Hangs

> See also: [Ubuntu Software not loading](https://askubuntu.com/a/1291111).

```sh
killall snap-store
```
