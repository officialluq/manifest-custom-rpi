# Preparing Workspace
```
mkdir rpi-yocto
cd rpi-yocto
```
# Downloading sources 
```
repo init -u https://github.com/officialluq/manifest-custom-rpi -b main -m custom-test-1.0.0.xml
repo sync
```

# Build sources

```
source sources/poky/oe-init-build-env
bitbake-layers add-layer ${LAYER} # It is necessary to add every layer here
DISTRO=XXX MACHINE=YYY bitbake ZZZ
# XXX is distro name
# YYY is machine name
# ZZZ is image/recipe name
```
