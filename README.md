# kids-kilauncher

[KiLauncher](http://www.alandmoore.com/kilauncher/kilauncher.html) config to set up children's game/education machine.

## Requirements

This has been developed and tested on (L)Ubuntu 16.04. It's quite simple and will probably work on other distributions with minor changes.

## Installation

1. `sudo apt update && sudo apt -y install git && sudo git clone https://github.com/hillsy/kids-kilauncher.git /etc/kilauncher`
2. `sudo apt install -y $(cat /etc/kilauncher/pkglist)`
3. `sudo git clone https://github.com/alandmoore/KiLauncher.git /usr/local/share/kilauncher`
