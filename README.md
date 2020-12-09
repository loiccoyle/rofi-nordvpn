# rofi-nordvpn

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
</p>

Dynamic menu interface for `nordvpn`.

# Dependencies:

 * `rofi`
 * `nordvpn`

# Installation:

Just git clone this repo and place the `rofi-nordvpn` file somewhere on your `PATH` and make sure it is executable `chmod +x rofi-nordvpn`.

# Configuration:

There isn't much to configure. If you are not a `rofi` user don't fret you simply need to adjust the `menu` function to use your chosen dynamic menu program.

# Status bars:

For easy embeding into your chosen status bar, consider using the `-s` flag which outputs the current vpn status. When using the `-s` flag you can specify a "LABEL" which will prefix the status message.

```sh
$ rofi-nordvpn -s 👻
👻 Paris
```

For polybar here is my module (using the [Siji](https://github.com/stark/siji) font):

```ini
[module/vpn]
type = custom/script
exec = rofi-nordvpn -s 
interval = 10
click-left = rofi-nordvpn &
```
