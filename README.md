# tylermwells-TAB-Impementation

## Purpose

The sole purpose of this repository is to make it easier to implement the TAB protocol. 

## Getting Started

The first step will be to re-flashing the ta-expt board before moving it over to serial setup. You will need to flash it with the flight-401-blr.c. Use the following:

```bash
cd ../../scripts/
source sourcefile.txt
cd ../software/flight-401-blr/
make
st-flash write flight-401-blr.bin 0x8000000
```






