# Model M Controller, by HBB

This is a drop-in replacement controller for the IBM Model M with QMK and VIAL support. I designed this for myself, and my own Models M, as well as some that I have sold/gifted to friends in the custom keyboard community, which is why this is designed only for the Models M that I own (the 101 key ANSI version, and the Space Saving Keyboard).

**Status (01-02-2026):** PCBA produced via JLCPCB and delivered. Tested successfully for basic operation. JST connector assembly in progress (I don't have a hot air soldering station).

## TODO:

1. Testing status lights and buzzer operation.
2. Uploading QMK and VIAL source to their respective repos.
3. BOM list availability in README (this file).
4. Fitment issue resolution due to USB-C port being too low for the existing cutout.
5. Figuring out solenoid operation and components required.
6. Pictures.

## Specs

- Based on the STM32F072CBT6 microcontroller, wide availability and great pedigree with QMK and VIAL. Works over USB-C.
- Like said, QMK and VIAL compatibility (firmware push and merge pending but it'll be there).
- Buzzer and Solenoid compatibility (optional, WIP). The exact parts needed for the solenoid are TBD and testing is required to be done first.
- Custom Status Lights PCB for adding LEDs in the colours of your choosing (standard DIP LEDs only), for the variants that have the possibility of adding such lights.
- Compatible with the 101-key and SSK Models M, Terminal or PS/2, both ANSI and ISO* versions.

*I need help with the firmware, as I don't own an ISO Model M to test it on.

## Why a new controller?

The "replacement Model M Controller" idea has already been implemented by many projects, with them already doing the work on understanding how the controller can be made in the first place, and the dimensions of a board that will fit the space voided by the original controller, that would be necessary to know how to place the components on my replacement. With that in mind, I would like to specifically highlight the [Ctrl-M](https://github.com/nuess0r/ctrl-M) and the [Model H](https://github.com/jhawthorn/modelh) projects, as they both provided me a sanity check of the dimensions of the PCB that I needed to design, separate from my own measurements of the several OEM controllers I now own.

While the above two are perfectly capable equivalents of my own creation, and I'm sure many would find either more suited for their own use cases, I found some limitations with the both of them that were disqualifying for my own use. Here is what I needed:

1. USB-C. All my other keyboards work off the same USB-C cable that I can detach from the keyboard end and swap the keyboard on my desk with another. While the Model H had this ability with the right Pro Micro controller, the Ctrl-M did not.
2. PCBA. It's significantly more expensive to produce this PCB via JLCPCB, with or without their assembly service. It's also almost conventional to expect a vintage keyboard replacement part to use a more "period-accurate" part selection, with through-hole componentry wherever possible, but I wanted something more modern that resembled a keyboard PCB you would get with a custom keyboard today. An entirely vain addition.
3. Additional bells and whistles. A keyboard with a solenoid is something I always wanted to add to my collection. While there are modern boards that will provide that to you, they are superseded, in my opinion, by a roomy plastic chassis, from a time when keyboards were normally significantly louer. Neither of the existing modules could provide that to me without a significant modification, so I decided to start from scratch.

Note: As a starting point for the solenoid and buzzer, I took directly from the [M122ion Control](https://github.com/dcpedit/mission-control) project, although the end result will use different components for the switching circuit.

All the above are fulfilled by this controller. This is also my first PCB design, and I enjoyed working on it. 

**As a disclaimer, however,** I don't claim this to be an extremely competent component, and I would advise anyone thinking of ordering a production run of this PCB to do their due diligence first. This is a hobbyist project first of all. Nonetheless, don't hesitate to reach out to me on @hardbodybrain on Discord, or on my personal email ID, yatharthsood00 [at] gmail [dot] com for any questions or clarifications, as well as if you want to share your experiences with this PCB, if you chose to get one of your own!