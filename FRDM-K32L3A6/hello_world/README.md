# Multicore Hello World project

The Multicore Hello World demo for FRDM-K32L3A6 board. See more details in [readme.txt](./readme.txt).

## Prerequisites

### Tools:
 - [CMSIS-Toolbox 1.3.0](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/releases/tag/1.3.0) or later
 - Arm Compiler 6.18 or later

### Packs:
 - Required packs are listed in the file [`HelloWorld.csolution.yml`](./HelloWorld.csolution.yml)

## Building

1. Use the `csolution` command to create `.cprj` project files.
   ```
   > csolution convert -s HelloWorld.csolution.yml

2. Use the `cbuild` command to create executable files.
   ```
   > cbuild cm0plus/HelloWorld_cm0plus.Debug+FRDM-K32L3A6.cprj
   > cbuild cm4/HelloWorld_cm4.Debug+FRDM-K32L3A6.cprj
   ```

## Programming

Use a programmer to download both images (`cm0plus` and `cm4`) to the target.
>Note: The built-in DAPLink can be used for programing. 
 Drag-and-drop the hex image for `cm0plus` and then for `cm4`.

## Running

Open a serial terminal with the following settings:
 - 115200 baud rate
 - 8 data bits
 - No parity
 - One stop bit
 - No flow control

The primary core (`cm4`) prints the "Hello World from the Primary Core!" to the terminal 
and then releases the secondary core (`cm0plus`) from the reset. 
The secondary core toggles an on-board LED indicating that the secondary core is running.
