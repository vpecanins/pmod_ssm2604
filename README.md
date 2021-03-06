# PMOD_SSM2604
Audio Codec PMOD board for FPGA

This is a small PMOD board that adds stereo ADC and DAC to your FPGA project. 
It is based around the SSM2604 audio codec from Analog Devices. The dimensions
of the board and connector pinout follow the rules for PMOD from Digilent.

[SSM2604 audio codec from Analog Devices](https://www.analog.com/en/products/ssm2604.html)

[How to design a PMOD - Digilent](https://blog.digilentinc.com/how-to-design-a-pmod-best-practices/)

## Specifications
- Two channel input ADC 24 bits
- Two channel output DAC 24 bits
- Sample rate configurable up to 96 kHz
- Onboard 12.288 master clock crystal oscillator
- Audio clock can be generated by FPGA changing R9/R10 solder bridges
- I2C configuration interface

## Status of the project

The board has been manufactured at PCBWay and successfully tested in MAX1000 FPGA board

## Pictures

![top](/pmod_audio_top.png "Top")
![bottom](/pmod_audio_bottom.png "Bottom")

## Pinout

Pinout is written on the bottom silk screen of the board.

![pinout](/pinout.png "pinout")

1. 3V3 supply for digital and analog circuits
2. 3V3 supply for digital and analog circuits
3. Ground
4. Ground
5. ADCDAT: ADC sample data provided by SSM2604 (I2S interface)
6. ADCLRC: ADC left/right clock provided by FPGA (I2S interface)
7. DACDAT: DAC sample data provided by FPGA (I2S interface)
8. DACLRC: DAC left/right clock provided by FPGA (I2S interface)
9. BCLK: Bit clock provided by FPGA (I2S interface) **Must be derived from AUDIO_CLK**
10. AUDIO_CLK: Master clock 12.288 MHz. Generated by SSM2604 oscillator.
11. SCLK: I2C interface SCL
12. SDIN: I2C interface SDA

Pin names keep the nomenclature from Analog Devices datasheet

## License
	
    Copyright (C) 2020  vpecanins

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.
    
   
