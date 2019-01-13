Copyright 2017 - LineageOS

# Device Tree for Xiaomi Redmi 4 Prime/wt88553 (MARKW) 

## Spec Sheet

| Feature                 | Specification                     |
| :---------------------- | :-------------------------------- |
| CPU                     | Octa-core 2.0 GHz Cortex-A53      |
| Chipset                 | Qualcomm MSM8953 Snapdragon 625   |
| GPU                     | Adreno 506                        |
| RAM                     | 3 GB                              |
| Shipped Android Version | 6.0.1 with MIUI 8/9               |
| ROM                     | 32 GB                             |
| MicroSD                 | Up to 256 GB                      |
| Battery                 | 4100 mAh (non-removable)          |
| Dimensions              | 141 x 69.6 x 8.9 mm               |
| Display                 | 1920x1080 pixels, 5" IPS          |
| Rear Camera             | 13 MP - s5k3l8                    |
| LED flash               | Yes                               |
| Front Camera            | 5 MP - ov5670                     |
| Release Date            | November 2016                     |

## Device Picture

![Xiaomi Redmi 4 Prime](http://cdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-redmi-4-prime-2.jpg "Xiaomi Redmi 4 Prime")

I suggest you to use this branch (MiracleDROID) instead of the "lineage-15.1" one if the ROM you want to build doesn't have the "lineage-sdk" https://github.com/LineageOS/android_lineage-sdk/tree/lineage-15.1 and "LineageParts" https://github.com/LineageOS/android_packages_apps_LineageParts/tree/lineage-15.1 repos in its manifests repo https://github.com/MiracleDROID/android/tree/android-8.1/ / https://github.com/DirtyUnicorns/android_manifest/tree/o8x/ .
The main/fundamental reason of this suggestion are the overlay/s folder/s in these two branches.

| This Device Tree also has:|
| :---------------------- |
| -a custom "Ambient Display/Doze" package added from MiracleDroid-HnT (thanks @Razziell and @Hikari-no-Tenshi) |
| -a custom "Device Parts/Settings" package called "XiaomiParts" (thanks @Razziell and @Hikari-no-Tenshi) |

If you're building MiracleDroid Oreo 8.1 you don't need any kind of adaptation to implement these two latest packages/build modules, otherwise you should look at the modification I've done to AICP-O_8.1 https://github.com/NotesOfReality/android_frameworks_base--DIFF/tree/AICP-O___o8.1/ and https://github.com/NotesOfReality/android_packages_apps_Settings/tree/AICP-O___o8.1/ .
