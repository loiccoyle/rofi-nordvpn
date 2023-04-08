# rofi-nordvpn

<p align="center">
  <img src="https://i.imgur.com/Y5kDbVf.png">
</p>

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
  <a href="https://aur.archlinux.org/packages/rofi-nordvpn-git/"><img src="https://img.shields.io/aur/version/rofi-nordvpn-git"></a>
</p>

Dynamic menu interface for `nordvpn`.

## Installation

**Dependencies:**

- `rofi`
- `nordvpn`

### Manual

Just git clone this repo and place the `rofi-nordvpn` file somewhere on your `PATH` and make sure it is executable `chmod +x rofi-nordvpn`.

### Arch

For Arch Linux (and derivatives):

```sh
paru -S rofi-nordvpn-git
```

## Status bars

For easy embedding into your chosen status bar, consider using the `-s` flag which outputs the current vpn status.

```sh
$ rofi-nordvpn -s
Paris
```

For `polybar`:

```ini
[module/vpn]
type = custom/script
label = 👻 %output%
exec = rofi-nordvpn -s
interval = 10
click-left = rofi-nordvpn &
```
