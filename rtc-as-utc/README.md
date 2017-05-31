Files for fixing time zone
======================

* Rationale

Your computer has a built-in RTC (real time clock) that keeps track of current time either in local timezone or UTC. On linux, the default behavior is RTC as UTC while Windows defaults to RTC as local time. This creates time difference if you use windows and linux on the same computer.

It is possible to ask both operating system to use the other scheme. On windows, the switch is a flippable registry key. On linux, it's the job of the init system to tell the kernel that RTC is in local time zone during an early stage of booting.

Android is also linux, but obviously the init and android framework isn't well prepared to handle this...

* Patches

Apply patches in directory `${ANDROID_DIR}` if you want to treat RTC as UTC. To ask windows 8+ to do the same, refer to [this article](https://wiki.archlinux.org/index.php/time#UTC_in_Windows).

**EXPECT TIME INCONSISTENCY AFTER COMPILING WITH THIS PATCH! IT IS SUPPOSED TO HAPPEN!** An internet time sync will set RTC to correct time in UTC timezone.

* Replacing existing installation

Replace `ramdisk.img` with the built one.