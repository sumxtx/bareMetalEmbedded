## Bare Metal Embedded ARM-Cortex M4 / STM32 ##

- [x] ToolChain Installation
- [x] Understand compilation process of a C program for an embedded target without using and IDE 
- [x] Write microcontroller startup file for STM32F4 MCU 
- [x] Write your own C startup code ( code which runs before main())
- [x] Understand the different sections of the relocatable object files (.o files)
- [x] Write Linker scripts file from scratch and understand section placements
- [x] Link Multiple .o files using linker script and generate application executables (.elf, bin, hex)
- [x] Load the final executable on target using OpenOCD and GDB Client

### ToolChain Installation ###

** (Arch Linux - pacman/AUR - may differ on other distros) **

- [x] extra/arm-none-eabi-binutils
    A set of programs to assemble and manipulate binary and object files for the ARM EABI (bare-metal) target
- [x] extra/arm-none-eabi-gcc
    The GNU Compiler Collection - cross compiler for ARM EABI (bare-metal) target
- [x] extra/arm-none-eabi-gdb
    The GNU Debugger for the ARM EABI (bare-metal) target
- [x] extra/arm-none-eabi-newlib
    A C standard library implementation intended for use on embedded systems (ARM bare metal)
- [x] extra/stlink
    Firmware programmer for STM32 STLINK v1/v2 protocol
- [x] OpenOcd

### Some Debug commands ###
[openOCD General-Commands](https://openocd.org/doc/html/index.html)
[
* make load 
* arm-none-eabi-gdb
* target remote localhost:port
* monitor reset init
* monitor flash write_image erase final.elf
* monitor reset halt
* monitor resume
* -> Memory Access Commands <-
    * monitor mdw 0x20000000 4
    * ...
* monitor bp [address len [hw] ]
* quit
