# OpenOCD

Various CLI commands for OpenOCD as it regards to flashing things.

## Show the flash banks as understood by OpenOCD
```
> flash banks
#0 : stm32f103c8.flash (stm32f1x) at 0x08000000, size 0x00010000, buswidth 0, chipwidth 0
```

## Probe a specific flash bank. 
```
> flash probe 0
device id = 0x20036410
flash size = 64kbytes
flash 'stm32f1x' found at 0x08000000
```

## Show the target device that is detected by the OpenOCD interface

```
> targets
    TargetName         Type       Endian TapName            State       
--  ------------------ ---------- ------ ------------------ ------------
 0* stm32f103c8.cpu    hla_target little stm32f103c8.cpu    running
```

## Program a binary file to the flash bank address

```
> program generic_boot20_pc13.bin 0x08000000 verify reset
```

