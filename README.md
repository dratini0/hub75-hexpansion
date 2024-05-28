# HUB75 hexpansion

As of yet untested

Drives an LED wall panel by a single SPI peripheral.
A single 74HC595 drives the line select lines, this is inserted before the panel.
Then, the serial stream goes through the shift registers in the panel, and it is fed back into the input of the panel from the daisy chain output.
This means that a panel that normally needs a 6-way parallel drive can now be driven with just a single SPI line.
The OE pin is broken out to the high speed IO for a good measure.

The order of the chain is as follows:
1. Shift register
2. R1
3. G1
4. B1
5. R2
6. G2
7. B2

## Acknowledgements

Uses the [hexpansion template from EMF](https://github.com/emfcamp/badge-2024-hardware/tree/main/hexpansion)

I have taken the idea of chaining an LED wall panel with itself from some Youtube video that I have seen years and years ago, and I can no longer locate.
