Building LithRom
========
Possible devices:

    Lunch menu... pick a combo:
     1. aosp_arm-eng
     2. aosp_x86-eng
     3. aosp_mips-eng
     4. vbox_x86-eng
     5. aosp_manta-userdebug
     6. aosp_flo-userdebug
     7. aosp_tilapia-userdebug
     8. aosp_grouper-userdebug
     9. aosp_deb-userdebug
     10. mini_x86-userdebug
     11. mini_mips-userdebug
     12. mini_armv7a_neon-userdebug
     13. aosp_mako-userdebug
     14. aosp_hammerhead-userdebug
     
Now build:

    repo init -u https://github.com/LithRom/manifest.git -b master
    cd device/lge/mako
    ./extract-files.sh
    cd ../../../
    . build/envsetup.sh
    lunch aosp_mako-userdebug
    time make -j$(grep -c /proc/cpuinfo ^processor) otapackage
    
These are the quick and dirty, over the next few days code will be added and this process will decrease. If there is an issue, please let me know so I can fix it. Thanks!
