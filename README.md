# Beaglebone Black Gadget Snap

This repository contains the source for an Ubuntu Core gadget snap
for the Beaglebone Black. Building it with snapcraft will
automatically pull, configure, patch and build the git.denx.de/u-boot.git
upstream source for `aam335x_boneblack_config` at release `v2017.01` and produce
a bootable gadget snap with the resulting binaries.

## Gadget Snaps

Gadget snaps are a special type of snaps that contain device specific support
code and data. You can read more about them in the snapd wiki
https://github.com/snapcore/snapd/wiki/Gadget-snap

## Building

### Natively on armhf

To build the gadget snap locally on a native armhf system just run `snapcraft`
in the toplevel of the tree.

### Cross on x86 systems

Copy the crossbuild-snapcraft.yaml over snapcraft.yaml and run `snapcraft`

```
cp crossbuild-snapcraft.yaml snapcraft.yaml
snapcraft
```
