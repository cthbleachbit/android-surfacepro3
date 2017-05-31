Files for kernel 4.4.x
======================

* `patches`

Credit to [linux-surfacepro3](https://aur.archlinux.org/packages/linux-surfacepro3) on archlinux user repository.

apply patches in directory `${ANDROID_DIR}/kernel`, ignore reversed patches

* `sp3_defconfig`

Kernel 4.4 configuration for Surface Pro 3, copy to `${ANDROID_DIR}/kernel/arch/x86/configs`

* Replacing existing installation

Replace `kernel`, `initrd.img`, `system/lib/modules` and `system/lib/firmware` with self built ones.