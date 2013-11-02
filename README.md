Building LithRom
========
Possible devices:

    aosp_mako-userdebug
     
Now build:

    repo init -u https://github.com/LithRom/manifest.git -b master
    cd device/lge/mako
    ./extract-files.sh
    cd ../../../
    . build/envsetup.sh
    lunch aosp_mako-userdebug
    time make -j$(grep -c ^processor /proc/cpuinfo) otapackage
    
These are the quick and dirty, over the next few days code will be added and this process will decrease. If there is an issue, please let me know so I can fix it. Thanks!
