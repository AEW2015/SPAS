# Nios V Altera/Intel Soft Processor
This is the RISC-V soft processor provided by Altera/Intel.  It comes with 3 variations:
* Nios V/c -> Compact Microcontroller (No JTAG Debug)
* Nios V/m -> Microcontroller (Target Example)
* Nios V/g -> General Purpose Processor (Future Examples)


## Prereqs for Guide
These are the basic prereqs that should be done first:
* Use Intel Self-licensing tool (Requires Microsoft account)
  * Get NIOS V (c/m/g) license locked for you PC
* Install Quartus Lite (23.1)
  * Include Ashling RISC-V IDE
* Instal Quartus Pro (24.1), No license needed
  * Only Install Ashling RISC-V IDE
* Setup License so its points to License File

## Steps in Guide
The steps to guide a basic Speedrun:
* Step 0: Setup Project
* Step 1: Platform Designer
* Step 2: Bitstream Generation
* Step 3: HAL BSP Generation (Copy/Paste Hello world?)
* Step 4: RISC-V IDE Cmake
* Step 5: Load HW and Execute SW

TODO: Add Pictures when useful

## Scripts to Demo Guide (TODO)

## Future Issues to Address (TODO)
I would like to optimize and stream line the guide with these ideas:
* 23.1 only tutorial for Quartus lite (current steps use Ashling IDE from pro 24.1 install)
* GDB breakpoints not working with current guide
* Split Instruction and Data bus for local mem (BSP errors out)
* HAL BSP is too big for Max 10 (64% for 10M50)
* Elf2Hex tutorial to load elf file into Bitstream
* Tutorial for FSBL to load from flash to external DDR memory
* Nios V/g tutorials plus yocto/buildroot builds