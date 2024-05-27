# Step 3: HAL BSP Generation

## Create Folder Directors
This is the folder that will be used for you SW and the Ashling IDE
* Make SW directory in project -> \<projcet\>\sw
* Make BSP directory in project -> \<projcet\>\sw\bsp
* Make Application directory in project -> \<projcet\>\sw\app
* Create hello.c in \<projcet\>\sw\app
```
#include <stdio.h>
#include <unistd.h>
void looper() {
 for (int i = 0; i < 1000; ++i) {
 printf("Hello world, this is the Nios V/m cpu checking in %d...\n",
i);
 }
}
int main() {
 looper();
 usleep(1000000);
 printf("Bye world!\n");
 fflush(stdout);
 return 0;
}
```

## Generate BSP files and Cmake files
This is the BSP generation for Quartus Lite (23.1):
* Open Nios V Command Shell (Quartus Lite 23.1)
* change directory with cd to \<projcet\>
* Generate BSP files
  * `niosv-bsp -c -s=niosv_top.sopcinfo -t=hal sw/bsp/settings.bsp`
* Generate Hello.elf Cmake files
  * `niosv-app --bsp-dir=sw/bsp --app-dir=sw/app --srcs=sw/app/hello.c --elf-name=hello.elf`


## Move to Step 4