# Flashing the Tippmann X7 Classic #


---


# How to write to the chip #
First things first, you're going to have to buy an ISP programmer.  A common/cheap programmer that will work for this is the USBasp, though you can use any programmer as long as it's compatible with avrdude (see http://www.ladyada.net/learn/avr/avrdude.html for a list of compatible programmers).

Next, you will need to download and install avrdude.  I would suggest you download and install WinAVR from http://winavr.sourceforge.net/  This will include avrdude and will make things easier in the long run.

Once you have avrdude installed (test from the command line by typing avrdude -?), you'll need to hookup your ISP.  This is the hard part.  Using the pinout from your programmer, you should see 6 important pins.  Know where these pins are on your programmer.  The chart below shows the name of the 6 pins.  You will need to match each of these pins to your etrigger.

Hopefully your programmer will supply voltage to the chip.  If so, you need to verify that it supplies 5v.  If you purchased or built a USBasp, chances are you're good to go.  Otherwise, consult your programmer's manual and/or online for more instructions on how/where to get 5v.

With that out of the way, you'll need to connect each pin to the Phenom's appropriate pin.  Examples:

| **Programmer** | **Phenom** |
|:---------------|:-----------|
| Vcc            | Vcc (Pin 1) |
| GND            | GND (Pin 14) |
| RESET          | RESET (Pin 4) |
| MOSI           | MOSI (Pin 7) |
| MISO           | MISO (Pin 8) |
| SCK            | SCK (Pin 9) |

To connect to the Phenom pins, I held one set of leads in my left hand and the other set in my right and pressed them carefully against the appropriate pins on the phenom chip, and used either another person or some other random appendage (nose, toe, etc) to press the enter key for the command.

http://phenomx7-etrigger.googlecode.com/svn/wiki/phenomPinOut.JPG

`*` **Please note that this chip was desoldered and placed on a breadboard for debugging purposes only.  You will not be required to solder or desolder anything to implement this code.**

### ISP Programmer I used ###
http://www.amazon.com/SainSmart-Programmer-ATMEL-ATMega-ATTiny/dp/B0051SRZWC/ref=sr_1_1?ie=UTF8&qid=1338268631&sr=8-1

**Driver for usbasp:**
http://www.fischl.de/usbasp/

**Pin out for USBasp:**
![http://wiki.mad-phenom.googlecode.com/git/usbaspPinout.jpg](http://wiki.mad-phenom.googlecode.com/git/usbaspPinout.jpg)

Though there are cheaper (just as compatible) versions available.  Just search eBay for ISP programmer and find one that is compatible with your operating system, supported by avrdude, and supplies 5v.  You should be able to find one for under $10 USD.

### Recommended Purchase ###
http://www.amazon.com/Breadboard-jumper-wire-70pcs-pack/dp/B0040DEI9M/ref=pd_sim_t_3

# AVRDUDE command to write HEX to chip #
First start by downloading the latest version of our programming:

http://mad-phenom.googlecode.com/files/x7classic-etrigger-0.1.2.hex

Then execute the following commands at your command prompt:

Run this command and verify that the Device signature is 0x1e9207
```
avrdude -pt44 -cusbasp
```

If your device signature does not match the above.  Please post a comment to the wiki or to the YouTube videos.

Run these commands to write the software to your chip:
```
avrdude -F -e -v -pt44 -cusbasp -D -Uflash:w:"C:\tmp\x7classic-etrigger-0.1.2.hex":i
avrdude -cusbasp -pt44 -U lfuse:w:0xE2:m
avrdude -cusbasp -pt44 -U hfuse:w:0xDF:m
avrdude -cusbasp -pt44 -U efuse:w:0xFF:m
```

# Programming your new eTrigger #

## Phenom Programming Part 1 ##
This video will show you how to install the code on your eTrigger.

Video Link: http://www.youtube.com/watch?v=ukOMqf9Xon8

<a href='http://www.youtube.com/watch?feature=player_embedded&v=ukOMqf9Xon8' target='_blank'><img src='http://img.youtube.com/vi/ukOMqf9Xon8/0.jpg' width='425' height=344 /></a>

## Phenom Programming Part 2 ##
This video is part 2 and will show you the software portion of installing the new programming on your eTrigger.

Video Link: http://www.youtube.com/watch?v=U5SsedGsSBo

<a href='http://www.youtube.com/watch?feature=player_embedded&v=U5SsedGsSBo' target='_blank'><img src='http://img.youtube.com/vi/U5SsedGsSBo/0.jpg' width='425' height=344 /></a>

## Using the new programming ##

## There have been some modifications to the menu (added presets and Ammo Limit): ##
```
Selector (1 Red blink for F, 2 Red blinks for FA)
    Preset (Orange blink indicating the preset you are about to edit)
        Firing Mode (alternating green and red)
            Full Auto (Flashing Red)
            Burst Mode (Three green blinks)
            Auto Response (Green flash, then red flash)
            Semi-Auto (Solid Green)
        Firing Rate (flashing green)
            1 - 40
        Burst Size (Three red flashes)
            2 - 10
        Ammo Limit (Solid Red)
            0 - 250
        Safety Shots (Solid Green)
            0 - 5
```

## Pins from MCU to Phenom ##
| **Programmer** | **Phenom** |
|:---------------|:-----------|
| Pin 3          | Push Button |
| Pin 5          | Trigger sensor 1 |
| Pin 6          | Solenoid   |
| Pin 7          | Trigger sensor 2 |
| Pin 11         | Green LED  |
| Pin 12         | Red LED    |


---


# Experimental #
### Programming with Diamex DX ISP in Windows ###

First you will need to find which com port the Diamex DX ISP is hooked up to.  This can be found in the Windows Device Manager.

Test your programmer with the following command (replace COM3 with whichever COM port your programmer is hooked up to):
```
avrdude -pt44 -cstk500v2 -P\\.\COM10 -b9600
```

Program the chip:
```
avrdude -F -e -v -pt44 -cstk500v2 -P\\.\COM10 -b9600 -D -Uflash:w:"C:\tmp\x7classic-etrigger-0.1.2.hex":i
avrdude -cstk500v2 -pt44 -P\\.\COM10 -b9600 -U lfuse:w:0xE2:m
avrdude -cstk500v2 -pt44 -P\\.\COM10 -b9600 -U hfuse:w:0xDF:m
avrdude -cstk500v2 -pt44 -P\\.\COM10 -b9600 -U efuse:w:0xFF:m
```