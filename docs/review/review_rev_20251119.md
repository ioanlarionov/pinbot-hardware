# review rev.20251119

## Power
- 5V from TYPE-C 2A fuse
- CC1,2 5.1k to GND
- 3V3 is used from RPIZ, 1A max
## ADC
- 820k/120k 1% divider + 6M Ohm input of ADS1015 gives together up to 4% error
  - *use smaller divider*
- RC filtering for AINx advised
  - *add caps after dividers*
- ALERT/RDY is not used, RPI drivers dont require to connect it

## Relays


## Digitla inputs
- **User should know that even if it's possible to use up to 24V for these inputs, it's not compatible with Industrial Digital Inputs (DI)** adhere to IEC 61131-2 standards, typically classified as Type 1 or Type 3, which define the voltage limits for switching between ON and OFF. Signal OFF (Low) Limits: Typically 0V to 5V. Signal ON (High) Limits: Typically 11V to 30V.



## resources
- [ADS1015](https://www.ti.com/lit/ds/symlink/ads1015.pdf)
- [RPI Zero 2W](https://pip-assets.raspberrypi.com/categories/584-raspberry-pi-zero-2-w/documents/RP-008360-DS-1-raspberry-pi-zero-2-w-reduced-schematics.pdf?disposition=inline) 
  - [step-down reg RPIZ](https://www.diodes.com/assets/Datasheets/PAM2306.pdf) 1A 3V3