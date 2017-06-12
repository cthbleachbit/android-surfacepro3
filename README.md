Android x86 patch sets for surface pro 3
========================================

Tested on marshmallow on 2017 May 31.

Building
--------

Refer to [Android x86 build instructions](http://www.android-x86.org/getsourcecode) to prepare and download sources. The `${ANDROID_DIR}` refers to the directory where you prepared a working tree of source codes. There is no need to use `lunch`, copy `buildspec.mk` over is enough. Apply any patches you want and build with `make iso_img` with no trailing variables.

Files list
----------

* `buildspec.mk`

An specification for automated building, copy to `${ANDROID_DIR}`

* `rtc-as-utc`

Regarding hardware clock problems if you use multi-boot. See README.md in that folder for more details.

* `kernel`

Linux kernel 4.4 configuration and patches for use with the specific hardware: Microsoft Surface Pro 3. See README.md in that folder for more details.

