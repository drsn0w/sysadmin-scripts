# sysadmin-scripts
## by drsn0w

This is a collection of handwritten scripts that I use on my various machines to make day-to-day system administration tasks significantly easier and more streamlined.

## sysupgrade2
`sysupgrade2` is a simple script for (but not limited to) Arch Linux on BTRFS installations. It checks for updates, and if found, takes a snapshot using Snapper, rebuilds the initramfs, and regenerates the Grub configuration file.

```
usage: sysupgrade2 [-h] [-s] [-sN] [-m] [-mN] [-g] [-gN]
                   [--cpio-preset MKINITCPIO_PRESET]
                   [--grub-cfg GRUB_CFG_PATH]

Performs a system upgrade after a snapper snapshot, and regenerates initramfs
and grub configuration, if enabled

optional arguments:
  -h, --help            show this help message and exit
  -s                    enable Snapper snapshots
  -sN                   disable Snapper snapshots
  -m                    enable rebuilding the initramfs
  -mN                   disable rebuilding the initramfs
  -g                    enable generating the GRUB configuration file
  -gN                   disable generating the GRUB configuration file
  --cpio-preset MKINITCPIO_PRESET
                        override name of mkinitcpio preset
  --grub-cfg GRUB_CFG_PATH
                        override GRUB configuration file path
```
