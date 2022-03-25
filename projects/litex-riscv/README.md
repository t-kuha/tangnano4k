# Risc V MCU with LiteX

## Building HW & SW

```shell-session
# install litex-boards
$ git clone https://github.com/litex-hub/litex-boards.git
$ cd litex-boards/
$ git checkout eb8657f515fe63ced13c487f7da537451d89d993
$ python3 setup.py install

# build & program device
$ python3 -m litex_boards.targets.sipeed_tang_nano_4k --cpu-variant=minimal --build --flash 
```

## Run

```shell-session
        __   _ __      _  __
       / /  (_) /____ | |/_/
      / /__/ / __/ -_)>  <
     /____/_/\__/\__/_/|_|
   Build your hardware, easily!

 (c) Copyright 2012-2022 Enjoy-Digital
 (c) Copyright 2007-2015 M-Labs

 BIOS built on Mar 23 2022 21:45:36
 BIOS CRC passed (f39e5017)

 Migen git sha1: 25fb9a6
 LiteX git sha1: 25fb9a6

--=============== SoC ==================--
CPU:            VexRiscv_Min @ 27MHz
BUS:            WISHBONE 32-bit @ 4GiB
CSR:            32-bit data
ROM:            32KiB
SRAM:           8KiB
FLASH:          4096KiB

--========== Initialization ============--

Initializing W25Q32 SPI Flash @0x00000000...
SPI Flash clk configured to 13 MHz
Memspeed at 0 (Sequential, 4.0KiB)...
   Read speed: 283.5KiB/s
Memspeed at 0 (Random, 4.0KiB)...
   Read speed: 2.6KiB/s

--============== Boot ==================--
Booting from serial...
Press Q or ESC to abort boot completely.
sL5DdSMmkekro
             Timeout
No boot medium found

--============= Console ================--

litex>  
```

- Type ``help`` for available commands
