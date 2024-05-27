# Step 4: RISC-V IDE Cmake

## Make Hello.elf
This is currently using the Ashling IDE from Quartus Pro 24.1 w/ NO license
* Open Ashling RiscFree IDE
* Select \<project\>\sw as workspace
* File -> Import Nios V CMake based Project
  * Project name -> bsp
  * Nios V CMake project location -> \<project\>\sw\bsp
* File -> Import Nios V CMake based Project
  * Project name -> app
  * Nios V CMake project location -> \<project\>\sw\app
* Right-click app -> build project (TODO: look at gcc flags)
* Under CDT Build Console [app] notice size for hello.elf
  * `94.45 KB - Program size (code + initialized data).` (way too big)
  * `27.33 KB - Free for stack + heap.` 
    * (Dynamic Stack/Heap size based on remaing size)
* Ready to Simulate or Execute 

## Move to Step 5