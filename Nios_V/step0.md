# Step 0: Setup Project

## Basic Project setup
 Open Quartus Lite:
 * Project name -> niosv_top 
 * Empty project
 * No files to add at the moment
 * Device
   * Family: MAX 10
   * Device: MAX 10 DA
   * Package: FPGA
   * Pin count: 484
   * Core speed grade: 6
   * 10M50DAF484C6GES
 *  Or use Board Arrow MAS 10 DECA config
 *  EDA Tools (pick your choice):
    *  Synthesis -> Precision Synthesis
    *  Simulation Questa Intel FPGA (Not used in guide)
    *  Verilog HDL

## Special MAX 10 memory init setting
This is needed to properly do the Fitter:
* Assignments -> Device
* Device and Pin Options...
* Configuration Mode -> Single Uncompressed Image with Memory Initalization
* OK
* OK

## Move to Step 1
