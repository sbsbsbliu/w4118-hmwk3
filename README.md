Implementations of a locking primitive based on Android's accelerometer sensor events.
==
Copyright (C) 2014 V. Atlidakis, G. Koloventzos, A. Papancea

COMS-W4118 Columbia University

## MODIFIED/ADDED FILES:

- acceleration_d/Makefile
  customized Makefile for simple daemon operation or motion
  support with debug information

- acceleration_d/acceleration.h
  defined user space dev_acceleration struct and set_acceleration syscall

- acceleration_d/accelerationd.c
  daemon that polls acceleration from the device and writes it into the kernel

- flo-kernel/arch/arm/include/asm/unistd.h
  defined syscalls at positions 378 through 382

- flo-kernel/arch/arm/kernel/calls.S
  added syscalls to syscall table at positions 378 through 382

- flo-kernel/include/linux/acceleration.h
  defined kernel space dev_acceleration struct and set_acceleration syscall

- flo-kernel/include/linux/accevt.h
  defined acc_motion struct and accevt_create/wait/signal/destroy syscall

- flo-kernel/kernel/Makefile
  added acceleration and accevt binaries to the kernel compilation

- flo-kernel/kernel/acceleration.c
  set_acceleration syscall implementation

- flo-kernel/kernel/accevt.c
  accevt_create/wait/signal/destroy syscall implementation

- test/Makefile
  Makefile for shake.c test exercise

- test/acceleration.h
  defined acc_motion struct

- test/shake.c
  exercise 4 test implementation

- utils/our_checkpatch.pl
  custom script that mass-checkpacks our repository

## RESOURCES USED:

1. Linux Cross Reference
   http://lxr.free-electrons.com

2. Linux Kernel Development (3rd Edition)

3. Operating Systems: Principles and Practice (2nd Edition)
