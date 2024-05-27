# Step 5: Load HW and Execute SW



## Program FPGA
This will use the programmer from Quartus Lite:
* Program Device from Quartus Lite Tasks menu
  * Start
  * 100% Successful
  
## Setup Elf Run Configuration
This will target the Nios V/m in the DECA FPGA:
* (in Ashling IDE) Right-click app -> Run as -> Ashling RISC-V HW Debugging
  * hello.elf
* Go to Debugger Tab
  * Auto-detect Scan Chain
  * Should see `Nios V (0xXXXXXXXX)` in Core Selection
* Apply
* Run

## Setup JTAG UART Util
This is the JTAG UART Util (Can open outside of IDE)
* Run -> External Tools -> External Tools Configurations
* Double-click Program
* Name -> JTAG UART
* Location -> Browse File System...
  * \<Quartus Lite Install\>\quartus\bin64\juart-terminal.exe (expecting windows)
* Arguments -> `-c 1 -d 0 -i 0`
* Apply
* Run
  * May have to rerun hello.elf run


## Example Output

```
juart-terminal: connected to hardware target using JTAG UART on cable
juart-terminal: "Arrow MAX 10 DECA [USB-1]", device 1, instance 0
juart-terminal: (Use the IDE stop button or Ctrl-C to terminate)

Hello world, this is the Nios V/m cpu checking in 0...
Hello world, this is the Nios V/m cpu checking in 1...
Hello world, this is the Nios V/m cpu checking in 2...
Hello world, this is the Nios V/m cpu checking in 3...
Hello world, this is the Nios V/m cpu checking in 4...
Hello world, this is the Nios V/m cpu checking in 5...
Hello world, this is the Nios V/m cpu checking in 6...
Hello world, this is the Nios V/m cpu checking in 7...
Hello world, this is the Nios V/m cpu checking in 8...
Hello world, this is the Nios V/m cpu checking in 9...
Hello world, this is the Nios V/m cpu checking in 10...
...
Hello world, this is the Nios V/m cpu checking in 999...
Bye world!
```