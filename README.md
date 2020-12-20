# libsmserver

This is the companion tweak to my app, [SMServer](https://github.com/iandwelker/smserver). I would recommend just using the latest provided package under `packages`, since this requires some extra depdencies to build. The deb should always be up to date with the source code, but if you want to be safe, just follow the instructions below to build from source.

## Dependencies
 - libmryipc - A package that is available on a default repo. Make sure you install this, it is required for this tweak to work.

## Disclaimer
$\qquad$ Reminder that software this comes with **no warranty** and is provided **as is**. Although I do my best to prevent it from harming your device (feel free to contact me if you would like details on how I do this), I cannot ensure that it will do no harm, and I cannot be held liable if such damage occurs.

## To install:
1. Install libmryipc from your package manager (e.g. Cydia, Zebra, Sileo)
2. Get the `.deb` from under `/packages` on this repo
3. Install the deb however you normally would, whether that be scp & filza, airdrop & zebra, etc.

### To build from source:
1. Install libmryipc on your device
2. Copy libmryipc.dylib from your phone into $THEOS/lib (if libmryipc is installed on your iPhone: `scp -C root@$THEOS_DEVICE_IP:/usr/lib/libmryipc.dylib $THEOS/lib/`)
3. Copy the MRYIPC headers from [here](https://github.com/Muirey03/MRYIPC) and place them in $THEOS/include/
4. cd into the directory of the `Makefile` and run `make package install`
