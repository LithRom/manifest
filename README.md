Building LithRom
========
Possible devices:

    aosp_hammerhead-userdebug
    aosp_mako-userdebug
     
Now build:

    repo init -u https://github.com/Lithoca/manifest.git -b master
    cd device/lge/mako
    ./extract-files.sh
    cd ../../../
    . build/envsetup.sh
    lunch aosp_hammerhead-userdebug
    time make -j$(grep -c ^processor /proc/cpuinfo) otapackage
    
These are the quick and dirty, over the next few days code will be added and this process will decrease. If there is an issue, please let me know so I can fix it. Thanks!
