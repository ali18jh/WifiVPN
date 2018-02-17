# WifiVPN
Wifi and Nord VPN connect script using Network Manager Command Line Interface (NMCLI), written in Bash.

<img src="https://i.imgur.com/OcSBlOe.png" />

## Requirements
A Linux installation with the following packages installed:

    * Systemd
    * NetworkManager
    * WPA_Supplicant
    * dhclient (for IPv6 support)
    * Dialog

## Pre-Flight
Make sure Network Manger is running

    #   sudo systemctl enable NetworkManager.service
    #   sudo systemctl start NetworkManager.service

Download the Nord VPN server connection files:

__https://nordvpn.com/api/files/zip__

Extract the zip and copy the files in the `ovpn_tcp` directory to the `vpn-servers` directory from this repo.

## Usage
Launch the script and you'll be presented with an interface that lets you:

* Log onto a wifi network
* Log into a Nord VPN server
* Disconnect from wifi
* Disconnect from VPN
* Manage related settings

## Terminal Alias
For convenience you can add the following function to your .bashrc file:

    # Wifi/VPN connection utility
    function wifivpn() {
        $HOME/path/to/WifiVPN/wifivpn.sh
    }


## Credits

Written by __[Rick Ellis](http://rickellis.com/)__.

## License

MIT

Copyright 2018 Rick Ellis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.