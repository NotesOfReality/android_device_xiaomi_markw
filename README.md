Copyright 2017 - LineageOS

# Device Tree for Xiaomi Redmi 4 Prime/wt88553 (MARKW) 

## Spec Sheet

=====================================================

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 2.0 GHz Cortex-A53
CHIPSET | Qualcomm MSM8953 Snapdragon 625
GPU     | Adreno 506
Memory  | 3 GB
Shipped Android Version | Android 6.0.1 with MIUI 8
Storage | 32 GB (Samsung RX1BMB)
MicroSD | Up to 256 GB (Hybrid)
Battery | 4100 mAh (non-removable) (Coslight/Feimaotui)
Dimensions | 141.3 x 69.6 x 8.9 mm
Display | 1080 x 1920 pixels, 5.0" IPS (Tianma r63350/EBBG nt35521s/EBBG nt35596)
Touchscreen | FOCALTECH FT5346 (for Tianma)/ATMEL A308U (for EBBG)
Rear Camera  | 13.0 MP, Dual LED flash (Samsung S5K3L8/OmniVision OV13853)
Front Camera | 5.0 MP (OmniVision OV5670)
FingerPrint | Yes (FPC 1020/Goodix GF3208)
Accelerometer | Yes (Bosch BMI160)
Magnetometer | Yes (Yamaha YAS537)
Als/ps | Yes (Liteon LTR55X)
LED | Yes (Awinic AW2013)
Release Date | November 2016

## Device Picture

![Xiaomi Redmi 4 Prime](http://cdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-redmi-4-prime-2.jpg "Xiaomi Redmi 4 Prime")

I suggest you to use this branch (MiracleDROID) instead of the "lineage-15.1" one if the ROM you want to build doesn't have the "lineage-sdk" https://github.com/LineageOS/android_lineage-sdk/tree/lineage-15.1 and "LineageParts" https://github.com/LineageOS/android_packages_apps_LineageParts/tree/lineage-15.1 repos in its manifests repo https://github.com/MiracleDROID/android/tree/android-8.1/ / https://github.com/DirtyUnicorns/android_manifest/tree/o8x/ .
The main/fundamental reason of this suggestion are the overlay/s folder/s in these two branches.

| This Device Tree also has:|
| :---------------------- |
| -a custom "Ambient Display/Doze" package added from MiracleDroid-HnT (thanks @Razziell and @Hikari-no-Tenshi) |
| -a custom "Device Parts/Settings" package called "XiaomiParts" (thanks @Razziell and @Hikari-no-Tenshi) |

If you're building MiracleDroid Oreo 8.1 you don't need any kind of adaptation to implement these two latest packages/build modules, otherwise you should look at the modification I've done to AICP-O_8.1 https://github.com/NotesOfReality/android_frameworks_base--DIFF/tree/AICP-O___o8.1/ and https://github.com/NotesOfReality/android_packages_apps_Settings/tree/AICP-O___o8.1/ .
