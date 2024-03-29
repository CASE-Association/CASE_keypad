# CASE keypad
2x3 Keypad kit

## Assembly instructions
This kit requires SMD soldering of 0805 components and a QFP microcontroller. [See this for quick guide in hand-soldering SMD components](https://www.youtube.com/watch?v=EW9Y8rDm4kE)
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
  - Download and open [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases)
  - Select the provided [.HEX file](https://github.com/CASE-Association/CASE_keypad/releases/download/keypad-release/case_keypad_via.hex) 
  - Choose ATMega32u2 as microcontroller
  - Push reset button on board and then press flash button in toolbox
  
Keypad should be flashed and ready to test. 
Use a jumper wire or tweezers to short the switch pins. 
The keypad should print numbers 1 to 6.

If flashing does not work, try using v0.0.21 of QMK toolbox 

You can now solder the switches/encoder. Encoder is optional and can only be soldered in either top corner (ONLY ONE).
  
## Keybinds
  - Download and install [VIA Configurator](https://github.com/the-via/releases/releases) (select .exe for windows)
  - Open VIA and go to File->Import Keymap
  - Select the file [via.json](https://github.com/CASE-Association/CASE_keypad/releases/download/keypad-release/via.json)
  - Plug in the keypad

The keybinds can now be configured.

## Troubleshooting
### Unknown USB device
This is a common problem. Plug in the keyboard and open the device manager. The keyboard should show up as ATmega32U2, if it instead shows up as unknown device, something is wrong. Follow these steps: 
 - Check that the USB-C connector has no shorts and all pads are connected. It can be good to retouch the connection even if no obvious problem can be found.
 - Do the same thing for the microcontroller chip. 
 - Also check that the resistors are soldered properly.
 - Check the rest of the components.

