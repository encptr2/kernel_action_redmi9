# Kernel Build Action For Lancelot & Merlin

## Usage
> After successful build, it will upload AnyKernel3 in `Action`, which has turned off device check, please flash to phone in Twrp.

First fork this repository to your repository and edit config.env as follows, then click `Star` or `Action`, you will see `Build Kernel` option on the left side, click it and you will see `Run workflows` on the top of the big dialog box on the right side, click it and it will start the build.

### KERNEL_SOURCE

Type your kernel link

e.g. https://github.com/Jbub5/android_kernel_xiaomi_mt6768

### KERNEL_SOURCE_BRANCH

Type your kernel branch

e.g. kernel-tree

### KERNEL_DEFCONFIG

Type your kernel defconfig

e.g. lancelot_defconfig

### TARGET_ARCH

e.g. arm64

### KERNEL_FILE

Type in the image you need, usually the same as BOARD_KERNEL_IMAGE_NAME in your aosp-device tree.

e.g. Image.gz-dtb

### EXTRA_BUILD_COMMAND
Some kernels require some build commands to be typed in manually in order to build properly, so please don't type them in if you don't need to.
Separate commands with spaces.

e.g. LLVM=1 LLVM_IAS=1

### USE_KERNELSU

Adds KernelSU 1.0.1 support

### KSU_HOOKS_PATCH

Adds hooks for KernelSU, useful if they have not already been included in the kernel

### SUPPORT_APATCH

Adds APatch support, installation instructions: https://apatch.dev/install.html

### NEED_DTBO

If your kernel also needs to be flashed with DTBO image, set it to true.

### MAKE_BOOT_IMAGE
> Merge from build_boot_image.yml

Set to true, boot.img will be Make, you need to provide `Source boot image`

## Credits

- [AnyKernel3](https://github.com/osm0sis/AnyKernel3)
- [AOSP](https://android.googlesource.com)
- [KernelSU](https://github.com/tiann/KernelSU)
- [xiaoxindada](https://github.com/xiaoxindada)
- [xiaoleGun](https://github.com/xiaoleGun)
- [Shas45558](https://github.com/Shas45558)
- [WuXing90](https://github.com/WuXing90)
