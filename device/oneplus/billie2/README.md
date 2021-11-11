# TWRP 10 for OnePlus Nord N100

### How to build ###

```bash
# Create dirs
$ mkdir tw; cd tw

# Init repo
$ repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-10.0

# Clone guam repo
$ git clone https://github.com/ters55/android_device_oneplus_billie2 -b twrp-10.0 device/oneplus/billie2

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ source build/envsetup.sh; lunch omni_billie2-eng; mka recoveryimage
```

## Credits
* betaxab/contributors: For ```ginna``` device tree base
