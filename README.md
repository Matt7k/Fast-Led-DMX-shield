# Fast-Led-DMX-shield
WS2812B tape with map controlled by dmx

GOAL: Control the mapping of a WS2812B led tape through a DMX shield, using only a single channel of dmx from a small console.
PROBLEM: The LEDs are flickering.

Software Version: Arduino 1.8.5, FastLED 3.1.6, Conceptinetics_RDM_alpha3

Parts: 
1x - Arduino Uno R3 
1x - CITC-DRA-10-R2 (Dmx shield by Conceptinetics)
1x - WS2812B, one meter, 60 leds
1x - 5v 20a power supply
1x - Baxter pocket console, 8 faders, patched 1:1

Additional details:
The console provides the control data into the shield in the form of dmx. The shield is set to Slave, TX-uart, & RX-uart. Only one channel of control is needed, dmx address 001. All devices have a common ground, and the tape has been tested previously both on this arduino and elsewhere. It is undamaged and seems to be functioning properly outside of this application. I have also swapped the console out for a DMXcat (City Theatrical) so that I could affect the refresh rate of the DMX. This didn't offer a solution. The FastLED library is being utilized and provides the functionality for the mapping. The effect I am trying to create is, as the fader goes up, more of the led tape fills. When channel 001 is at full (255) the led tape should be fully lit. With the fader at half, (128) the tape should be lit half way through, the other half being dark/off.




