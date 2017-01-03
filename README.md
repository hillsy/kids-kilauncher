# kids-kilauncher

[KiLauncher](http://www.alandmoore.com/kilauncher/kilauncher.html) config to set up children's game/education machine.

## Requirements

This has been developed and tested on [Lubuntu](http://lubuntu.net/) 16.04. It's quite simple and will probably work on other distributions with minor changes.

## Installation

1. `sudo apt update && sudo apt -y install git && sudo git clone https://github.com/hillsy/kids-kilauncher.git /etc/kilauncher`
2. `sudo apt install -y $(cat /etc/kilauncher/pkglist)`
3. `sudo git clone https://github.com/alandmoore/KiLauncher.git /usr/local/share/kilauncher`

## Autostart at login

Lxsession can [autostart applications at login](https://wiki.lxde.org/en/LXSession#Autostarted_applications_using_lxsession). Global commands are in `/etc/xdg/lxsession/Lubuntu/autostart`, but other commands can be locally specified in `~/.config/lxsession/Lubuntu/autostart`. **If both files are present, only the entries in the local file will be executed.**

If your children have their own account(s), you can autostart KiLauncher for them while keeping normal access to your account:

1. Remove any local config files on the system (**careful!**): `sudo find /home -type f -name "autostart" -delete`
2. Create the global file: `sudo bash -c "echo '@/usr/local/share/kilauncher/kilauncher' >> /etc/xdg/lxsession/Lubuntu/autostart"` (`@` means relaunch if killed)
3. Create your own local config to override the global file: `touch ~/.config/lxsession/Lubuntu/autostart`
4. Test by logging out and back in, as both types of user.

## Other ways to administer the system

You can get a terminal for admin purposes: <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>T</kbd>
