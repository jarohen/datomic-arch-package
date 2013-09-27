# Datomic Arch-Linux package

An attempt to package up Datomic for installing on Arch Linux machines.

## Usage

Mostly follows the usual Arch packaging process:

* Git clone the repo
* `makepkg`
  * `makepkg -si` if you want to install it immediately
* `sudo systemctl start datomic-free` to start the service immediately
* `sudo systemctl enable datomic-free` to start the service on system
  startup (multi-user mode)

## Feedback?

Yes please! Via the usual Github routes, or tweet
[@jarohen](https://twitter.com/jarohen) would be much appreciated!
