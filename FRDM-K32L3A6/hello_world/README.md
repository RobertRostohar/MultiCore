# Multicore Hello World project

The Multicore Hello World demo for FRDM-K32L3A6 board. See more details in [readme.txt](./readme.txt).

## Prerequisites

### Tools:
 - [CMSIS-Toolbox 1.3.0-dev1](https://github.com/brondani/cmsis-toolbox/releases/tag/1.3.0-dev1) or higher
 - Arm Compiler 6.18 or higher

### Packs:
 - Required packs are listed in the file [`HelloWorld.csolution.yml`](./HelloWorld.csolution.yml)

## Building

1. Use the `csolution` command to create `.cprj` project files.
   ```
   > csolution convert -s HelloWorld.csolution.yml

2. Use the `cbuild` command to create executable files.
   ```
   > cbuild HelloWorld_cm0plus.Debug+FRDM-K32L3A6.cprj
   > cbuild HelloWorld_cm4.Debug+FRDM-K32L3A6.cprj
   ```
