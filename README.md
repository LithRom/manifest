Building LithRom
========

    repo init -u https://github.com/LithRom/manifest.git -b master
    cd device/lge/mako
    ./extract-files.sh
    cd ../../../
    . build/envsetup.sh
    lunch (choose mako device)
    time make -j$(grep -c /proc/cpuinfo ^processor) otapackage
    
These are the quick and dirty, over the next few days code will be added and this process will decrease. If there is an issue, please let me know so I can fix it. Thanks!
