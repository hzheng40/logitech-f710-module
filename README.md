# logitech-f710-module
Support for Logitech F710 game controller on NVIDIA Jetson Xavier NX and Jetson AGX Xavier Developer Kits.

Installs hid-logitech module with F710 game controller enabled. The module uses the local name 4.9.201-tegra which is the default image local name.

The repository also provides an outline script to generate the module from the kernel sources.

### install-module
To install the provided hid-logitech.ko module:
```
$ ./install-module.sh
```
After installation, cold boot the machine.

### build-module
This is the outline script to build the Logitech kernel module. The script expects kernel sources to be in /usr/src
```
./build-module.sh
```
This script is provided as an example on how to turn on the LOGITECH_FF module on and build the module.

After the build, the module will be in /usr/src/kernel/kernel-4.9/drivers/hid/hid-logitech.ko


## Testing

After installation, to test:

```
$ sudo apt-get install jstest-gtk
# By default, the logitech F710 is on /dev/input/js0
# for example:
$ jstest /dev/input/js0
```

## Notes
### Release v1.1
* February, 2021
* JetPack 4.5 - L4T 32.5.0

### Release v1.0
* July 2020
* JetPack 4.4 - L4T 32.4.3
* Initial Release
### Release v0.5
* July 2020
* JetPack 4.4 DP - L4T 32.4.2
* Developer Preview Release



