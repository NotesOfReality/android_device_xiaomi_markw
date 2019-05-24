Copyright 2017 - 2019

# Device Tree for Xiaomi Redmi 4 Prime/wt88553 (MARKW) 

## Spec Sheet

=====================================================

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 2.0 GHz Cortex-A53
CHIPSET | Qualcomm MSM8953 Snapdragon 625
GPU     | Adreno 506
Memory  | 3 GB LPDDR3
Shipped Android Version | Android 6.0.1 with MIUI 8/9/10
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
LED | Yes (Awinic AW2013: 2 versions)
WIFI/BT/FM IC | WCN3660B (Dual-band 2.4 GHz and 5 GHz; IEEE802.11a/b/g/n)
Release Date | November 2016

## Device Picture

![Xiaomi Redmi 4 Prime](http://cdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-redmi-4-prime-2.jpg "Xiaomi Redmi 4 Prime")

* I suggest you to use this branch (lineage-15.1 or a branch based on it) instead of the "MiracleDROID" one if the ROM you want to build has the [lineage-sdk](https://github.com/LineageOS/android_lineage-sdk/tree/lineage-15.1) and [LineageParts]( https://github.com/LineageOS/android_packages_apps_LineageParts/tree/lineage-15.1) repos in its manifest/s repo (example of manifest/s repos:[MiracleDROID](https://github.com/MiracleDROID/android/tree/android-8.1/), [DirtyUnicorns](https://github.com/DirtyUnicorns/android_manifest/tree/o8x/), [crDroid](https://github.com/crdroidandroid/androidtree/8.1), [POSP](https://github.com/PotatoProject/manifest/tree/aligot-release) .
The main/fundamental reason of this suggestion are the [overlay/s](https://www.youtube.com/watch?v=O1IAmy_hnVU&t=8s) folder/s in these two branches.

| This Device Tree also has:|
| :---------------------- |
| -a custom "Ambient Display/Doze" package added from MiracleDroid-HnT (thanks @Razziell and @Hikari-no-Tenshi) |
| -a custom "Device Parts/Settings" package called "XiaomiParts" (thanks @Razziell and @Hikari-no-Tenshi) |

* If you're building LineageOS 15.1 (based on Android 8.1) you may very very probably have to cherry-pick the modifications I've committed in LineageOS-15.1 [frameworks_base](https://github.com/NotesOfReality/android_frameworks_base--DIFF/tree/lineage-15.1) and ["Settings" app](https://github.com/NotesOfReality/android_packages_apps_Settings/tree/lineage-15.1) repos in order to implement those two custom DT packages.


*Before the start of the ROM building process, check if your ROM has [this commit](https://github.com/MiracleDROID/android_system_sepolicy/commit/570ef945002a218a3da36fbe5c3bbe01a6d4b221) in its [system_sepolicy repo](https://github.com/DirtyUnicorns/android_system_sepolicy/tree/o8x) and if it doesn't (like DU), just cherry-pick it.
Doing so prevents a stupid "system_sepolicy"-related error and it's far far better and **safer** than just commenting out or deleting(/nuking) that ["external" error-causing line](https://github.com/DirtyUnicorns/android_system_sepolicy/blob/o8x/public/domain.te#L447) or the ["internal" one](https://github.com/NotesOfReality/android_device_xiaomi_markw/blob/DU-O___o8x-caf___Experimental/sepolicy/vendor/system_server.te#L4).*

A fast way to do it would be(starting a shell in the root of the android building environment):
```
cd system/sepolicy && git remote add MiracleDROID https://github.com/MiracleDROID/android_system_sepolicy/ && git fetch MiracleDROID && git cherry-pick 570ef945002a218a3da36fbe5c3bbe01a6d4b221
```
