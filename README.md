# EDK2 for Motorola One Action

Based on fxsheep's port for Xiaomi Mi 6 (sagit) (https://github.com/fxsheep/edk2-sagit/).

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core 2.2 GHz
CHIPSET | Samsung Exynos 9609
GPU     | Mali G72 MP3
Memory  | 4GB
Shipped Android Version | 9.0 (Pie)
Storage | 128GB
Battery | 3500 mAh
Dimensions | 160.1 x 71.2 x 9.2 mm
Display | 1080 x 2520 pixels, 6.3" LTPS IPS LCD
Rear Camera  | 12 MP (f/1.8) + 16 MP (f/2.2) + 5 MP (f/2.2)
Front Camera | 12 MP (f/2.0)

![Device Picture](https://fdn2.gsmarena.com/vv/pics/motorola/motorola-one-action-aqua-teal-1.jpg)

## Status 

What works:
- Display
- UEFI Shell

What does not work:
- Clocks
- eMMC (SdccDxe requires Clocks)
...

Anyway, if anyone is willing to help, please join our Discord server [DanctNIX](https://discord.gg/AvtdRJ3).

## Building
Tested on Ubuntu 18.04.

First, clone EDK2.

```
cd ..
git clone https://github.com/tianocore/edk2.git --recursive
git clone https://github.com/tianocore/edk2-platforms.git
```

You should have all three directories side by side.

Next, install dependencies:

18.04:

```
sudo apt install build-essential uuid-dev iasl git nasm python3-distutils gcc-aarch64-linux-gnu abootimg
```

Also see [EDK2 website](https://github.com/tianocore/tianocore.github.io/wiki/Using-EDK-II-with-Native-GCC#Install_required_software_from_apt)

Finally, ./build.sh.

Then `fastboot flash boot uefi.img`.

# Credits

This is based on fxsheep's [Mi6 port](https://github.com/fxsheep/edk2-sagit/), which is based on zhuowei's [edk2-pixel3](https://github.com/Pixel3Dev/edk2-pixel3).  
SimpleFbDxe screen driver is from imbushuo's [Lumia950XLPkg](https://github.com/WOA-Project/Lumia950XLPkg).  
Special thanks to @lemon1ice and @imbushuo for guidance.
