# MacroPadFrontier
A small RP2040-powered macropad for video and tabletop gaming productivity.
# Fair warning! This is a work in progress and not complete, be patient!

## Development

I set out to build this device because I wanted to improve the way that spaceflight controls worked in the Bethesda game Starfield. While keyboard control is fine, I wanted better controls for the power allocation element of the game. I figured that being able to switch power systems more quickly would allow for more interesting spaceflight and combat. The current vanilla control involves holding the ALT key and pressing WASD to select a system and change the power allocation. I did some drawings to lay out the capabilities I'd like, and came up with the following initial requirements:

* Arrow keys - 4 keys for directions which could be read as ALT + <WASD> to allow for easier toggling between flight systems and power allocation using the vanilla control scheme.
* Weapon system keys - keys to fire the 3 possible weapon assignments. There would just be bound to the standard keys.

I also had a couple of other requirements which went beyond Starfield:
* Audio control - I wanted an easy way of switching between my audio inputs quickly. I regularly use speakers, a DAC with headphones, and a gaming headset setup with microphone, and switching between on the fly can be a real pain.
* Function keys for switching between apps - at this point I hadn't really decided what I wanted these to be, but probably switching between discord, chrome and other apps. This functionality would be added later, but I wanted it considered while I was designing the hardware.
* DnD/TTRPG controls - having a set of keys to aid with macros and microphone control in a TTRPG setting would be really helpful, as I GM a SW5e game regularly over Discord and Foundry.
* I wouldn't ever be playing Starfield while also running a SW5e game, so having the ability to switch between two profiles would be great. 

To facilitate this I decided to build up an initial layout. It broadly broke down into four sections:
1. 3-pin 2-position toggle switch - This would allow me to switch between two states/profiles. I also added two 5mm LEDs to show which profile is active. 
2. Arrow keys - 4 keys in a + arrangement to control power allocation.
3. 3x3 grid - 9 keys for general functions, originally planned to be missile launch, boost, target, etc. but later changed.
4. 2x3 stack - 6 keys for audio control program launching.

In total this gave me 19 keys to play with and the option of adding two distinct profiles later on. I jumped on TinkerCad to come up with the enclosure to 3D print. I went with a two-part design, comprising a faceplate to which the switches would be attached as well as a main box which would hide the microcontroller and wires. I created hexagonal slots to be filled with M4 nuts and glued into place to allow the faceplate to be attached. I originally planned to have a slot for the RPico but in the end I left it loose inside the case. This isn't ideal, and could easily be fixed. I also put a little slot at the back of the case so that the USB cable could pass through. I intentionally left this quite wide as I wasn't sure which USB cable I wanted to use at this point, depending on the length. 

*Insert image of STL for faceplate*
*Insert image of STL for box*


# Hardware

Components:

* 1 Raspberry Pi Pico (non-WiFi version).
* 19 Cherry MX (or clone) switches.
* 22 awg stranded coated electrical wire (or similar).
* 1 3-pin 2-way toggle switch.
* 2 LEDs of any colour (preference only, optional).
* Resistors (appropriately valued to your LEDs).
* Micro-USB cable.

*Insert image of wiring diagram*

To Do (for readme):
* Upload code.py
* Upload STLs
* Software description
* Recommended additional software

To Do (for project):
* Fix faceplate bulging issue
* Design PCB
* Design Keycaps to print.
