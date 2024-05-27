# Step 2: Bitstream Generation

## Analysis & Synthesis
Some basic setup for Timing and IO:
* right-click niosv_top.qsys and set as Top
* File -> New -> Synopsys Design Constraints File
  * Add timing Constraint for input Clk:
  * `create_clock -name clk -period 20.0 [get_ports clk_in_clk]`
* Run Analysis & Synthesis
* Open Pin Assign tool (or use contraint file)
  * Analysis & Synthesis -> I/O Assignment Analysis -> Pin Planner
  * Set clk_in_clk as Location = PIN_M8 and I/O Standard = 2.5
  * Set rst_n_reset_n as Location = PIN_H21 and I/O Standard = 1.5
  * File -> Close
* Run Fitter & Assembler (just click Assembler)


## Move to Step 3