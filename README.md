WHAT IS THIS?
=============

A WIP custom Linux Kernel source code for the devices:
* bq aquaris X5


BUILD INSTRUCTIONS?
===================

Specific sources are separated by branches and each version is tagged with it's corresponding number. First, you should
clone the project:

        $ git clone https://github.com/Darkmet98/GlowKernel.git

Download a UBER Toolchains

        https://bitbucket.org/UBERTC/arm-eabi-4.8/downloads
		$ mkdir arm-eabi-4.8
		And extract it

Create KERNEL_OUT dir:

        $ mkdir KERNEL_OUT

Your directory tree should look like this:
* GlowKernel_MM
* arm-eabi-4.8
* KERNEL_OUT

Finally, build the kernel according the next table of product names:

| device                    | product                 |
| --------------------------|-------------------------|
| bq aquaris X5             | GlowKernel              |


        $ make -C GlowKernel_MM  O=../KERNEL_OUT  ARCH=arm CROSS_COMPILE=../arm-eabi-4.8/bin/arm-eabi- GlowKernel_defconfig
        $ make O=../KERNEL_OUT/ -C GlowKernel_MM ARCH=arm  CROSS_COMPILE=../arm-eabi-4.8/bin/arm-eabi-                       
    
You can specify "-j CORES" argument to speed-up your compilation, example:

        $ make O=../KERNEL_OUT/ -C GlowKernel_MM ARCH=arm  CROSS_COMPILE=../arm-eabi-4.8/bin/arm-eabi- -j 8
		
CREDITS
=============
-Darkmet98
-Faux123 (For the FastCharging)

