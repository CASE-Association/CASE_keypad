# CASE keypad
2x3 Keypad kit

## Assembly instructions
This kit requires SMD soldering of 0805 components and a QFP microcontroller.
Recommended soldering order:
  - Diodes 
  - Resistors/Capacitors
  - Pushbutton
  - Microcontroller
  - USB-C 
  - Crystal 
  - Switches/Encoder (Test and flash before soldering!)
	
<img src="https://raw.githubusercontent.com/CASE-Association/CASE_keypad/main/img/diode.png" width="500">

`Diodes have to be soldered in correct orientation. White line facing downwards.`

![mcu](https://raw.githubusercontent.com/CASE-Association/CASE_keypad/main/img/mcu.png)

`Dot on microcontroller should align with white dot on PCB.`

Rest of the components can be soldered in arbitrary orientation.

The keypad can be tested and flashed after soldering the crystal.

 - Plug in to computer
 - Check device manager for ATmega32u2
 - Keypad is working and ready for flashing if ATmega32u2 is detected
 - Proceed to flashing

## Flashing
  - Download and open QMK Toolbox
  - Select the provided .HEX file
  - Choose ATMega32u4 as microcontroller
  - Push reset button on board and then press flash button in toolbox
  
Keypad should be flashed and ready to test. 
Use a jumper wire or tweezers to short the switch pins. 
The keypad should print numbers 1 to 6.

You can now solder the switches/encoder. Encoder is optional and can only be soldered in either top corner (ONLY ONE).
  
## Keybinds
  - Download and install VIA Configurator
  - Open VIA and go to File->Import Keymap
  - Select the keymap.json file
  - Plug in the keypad

The keybinds can now be configured.


	
	
	




