Bootloader which uses BBOS functionality to boot.

The bootloader looks at the following address for:
0x1FD:  StartSector
0x1FE:  SectorCount
0x1FF:  Magic value (0x55AA)

As such, when bootable media is created, the words
indicated above should be set to appropriate values.

The bootloader loads from sector 'StartSector' onwards
to address 0 onwards, and then sets execution to address 0.

The magic value is not used by the bootloader, however it
is required for BBOS to recognize us as bootable.
