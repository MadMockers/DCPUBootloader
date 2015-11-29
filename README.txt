Bootloader which uses BBOS functionality to boot.

The bootloader looks at the following address for:
0x1FD:  StartSector
0x1FE:  SectorCount

As such, when bootable media is created, the words
indicated above should be set to appropriate values.

The bootloader loads from sector 'StartSector' onwards
to address 0 onwards, and then sets execution to address 0.
