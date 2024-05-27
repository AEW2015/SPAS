# Step 1: Platform Designer

## Open Platform Designer Tool
Tools -> Platform Designer

## Setup Blocks for simple config
This is a basic setup, but not the only options.
* Remove Clock source (doesn't follow Altera's new Tutorial)
* Add Clock Bridge from IP Catalog (search or Basic -> Bridge -> Clock)
  * Explicit clock rate: 50000000
* Add Reset Bridge from IP Catalog (search or Basic -> Bridge -> Reset)
  * Active low reset: yes
* Add Nios V/m Microcontroller from IP Catalog (search or Processors -> Embedded -> Nios V/m)
  * No changes (for now)
* Add On-Chip Memory from IP Catalog (search or Basic -> On-Chip -> On-Chip Mem)
  * Total memory size -> 131072 (TODO: need to figure to reduce)
  * TODO: Figure out Dual-port access
* Add JTAG UART from IP Catalog (search or Interface -> Serial -> JTAG)
  

## Add External Connections
This is the upper level IO for you Soft SoC:
* Clock Bridge -> in_clk -> Double-click Export Column
  * Name -> clk_in
* Reset Bridge -> in_reset -> Double-click Export Column
  * Name -> rst_n

## Add Internal Connections
This is how the clks, rsts, & buses are connected between the IP
* Clk, Click the clock circle for the following IP clk inputs
  * Reset Bridge
  * Nios V/m
  * On-Chip Mem
  * JTAG UART
* RST, Click the reset circle for the following IP clk inputs
  * Nios V/m
  * On-Chip Mem
  * JTAG UART
* IRQ , Click the irq circle for the JTAG UART IP
* Instruction Bus, Click the s1 circle for On-Chip Mem
* Data Bus, Click bus connections for the following IP:
  * On-Chip Mem
  * JTAG UART

## Setup Base Address
This is the basic Address map for your processor:
* System -> Assign Base Addresses
* Update Nios V/m reset vector:
  * View -> Parameters
  * Click Nios V/m instance
  * Vectors -> Reset Agent -> On-Chip Mem

## Save and Generate
The Final steps to export the Soft SoC to your Project
* File -> Save -> niosv_top.qsys (or ctrl-S)
* Geneate HDL... (bottom right of GUI)
  * Generate
* Add files to Project 
  * Assignments -> Settings -> Files (seems a weird path for this)
    * Add niosv_top.qsys
    * Add niosv_top/synthesis/niosv_top.qip

## Move to Step 2
