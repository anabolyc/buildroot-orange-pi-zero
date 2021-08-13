## Buildroot scripts for OrangePi Zero

### Tutorial

This is part of [OrangePi Zero network boot tutorial](https://hackaday.io/project/181169-orange-pi-zero-native-network-boot). By going through that tutorial you'd be able to build and deploy network boot configuration for Orange Pi Zero based on buildroot.

### Hot to build

Open solution in vscode

1. Run 'init submodule' task once to pull buildroot repo
1. Run 'make defconfig' taks to initialize default Orange Pi Zero config
1. Run 'make menuconfig' if you need to do some adjustments into default settings, like root password and stuff
1. You might want to adjust usertable in orangepi-zero/usertable file
1. Run 'make' task to run build itself. It will take a while

When build will finish, you will find below resources

- buildroot\output\staging - root filesystem that can be exported via NFS
- buildroot\output\images - kernel and dts files required for boot
- buildroot\output\images - sd-card images that you can write to SD using dd and boot directly from it

### Links

- [www.orangepi.org/orangepizero](http://www.orangepi.org/orangepizero/)
- [github.com/buildroot](https://github.com/buildroot/buildroot)
- [network boot tutorial](https://hackaday.io/project/181169-orange-pi-zero-native-network-boot)

