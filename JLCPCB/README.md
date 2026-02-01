# JLCPCB Production Files

There are two folders - one for the Gerber files for the controller itself, and the other for the status lights PCB Gerber files. You can skip the latter if you own an SSK or a Terminal model with no ability to display any status LEDs.

Both these folders contain the same files I used for the first production run of this PCB, in January 2026. Read the main README.md file for information on the run's outcomes and how the PCBs fared in my testing.

### Controller PCB

- Expected to be PCBA. 
- Uses SMD components wherever possible. You are expected to mandatorily solder the ribbon connector receptacles, I didn't hold my breath for JLCPCB having them in their components library. 
- All solenoid parts (except for the solenoid JST) are also through-hole, as I was not sure about which ones to use to make the solenoid work when I placed the order.
- The STM32 microcontroller chip will come with the USB-based bootloader in my experience when ordered from JLCPCB, but the board lacks exposed serial debug pins which you need in case you don't have a controller with the required bootloader, requiring you to solder some wires to the chip directly (tricky business).
- All the settings are all the defaults from JLCPCB that automatically populate when you upload the production files archive, except for the surface finish (I went with lead-free HASL, although that limits you on colour choices).


### Status lights
- Expected not PCBA, but you will have to solder the JST yourself if not. If money is no object, you can pay the hefty fees to solder one (1) singular component on this board through the assembly service. 
- All other parts are THT and trivial to assemble yourself. You can pick your status LEDs and read their datasheets for knowing what resistance would be best to work with.
- All default JLCPCB settings. 


More information will be added as I can add it based on my own experiences with this PCB.