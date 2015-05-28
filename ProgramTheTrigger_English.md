

# Programming menu cheat sheet #

## X7 Phenom ##
```
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

## X7 Classic ##
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



# Enter the programming menu #
  * Switch to safety
  * Press and hold the button in the trigger handle
  * Switch to "FA"
  * Continue to hold the button for at least 2 seconds
  * Release the button
  * You should now be in programming mode (one blinking orange light)

# Select Your Preset #
Upon entering the programming menu, you will be placed at the first preset.  To change to the second preset, pull and release the trigger once.  You should now see two blinking orange lights.  This indicates the second preset.  Pull and release the trigger again to get to the third preset.

To Select a preset, pull and hold the trigger for 2 seconds.

# Main Menu #

Once you've selected your preset, you are now at the Main Menu.  The first menu item is the firing mode.  To select any menu item, pull and hold the trigger for 2 seconds.  To change to the next menu item, pull and release the trigger in under 2 seconds.

Main menu items are indicated by the following chart:
  * Firing Mode (alternating green and red)
  * Firing Rate (flashing green)
  * Burst Size (Three red flashes)
  * Ammo Limit (Solid Red)
  * Safety Shots (Solid Green)

# Firing Mode #

Select the firing mode menu from the Main Menu but holding the trigger for 2 seconds.  The firing mode is indicated by alternating green and red lights.  Once the firing mode menu is selected, you will be shown blinking lights indicating your current firing mode.  To change modes, pull and release the trigger in under 2 seconds.  To select a firing mode, pull and hold the trigger for 2 seconds, then release.  The lights will turn solid orange for 2 seconds indicating success and return you to the Preset Menu.

Firing Modes are indicated by the following chart:
  * Full Auto (Flashing Red)
  * Burst Mode (Three green blinks)
  * Auto Response (Green flash, then red flash)
  * Semi-Auto (Solid Green)

# Firing Rate #

Firing Rate is the maximum balls per second the marker is allow to fire.  For Full Auto and Burst Mode, this is how many balls per second the marker will fire when the trigger is pulled.  For all other modes, this will limit the rate at which you pull the trigger down to the maximum balls per second.  This will ensure that pulling the trigger at 20 balls per second in Semi-Auto mode will not exceed a 15 balls per second firing rate (when the rate is set to 15); only 15 balls per second will be released in this case.

To select the firing rate menu item, pull the trigger, hold for 2 seconds, then release.  Once in the firing rate menu, green lights will blink indicating your current firing rate.  To set a new firing rate, pull the trigger as many times as your new firing rate (with at least 1 second between pulls).  For example, for a firing rate of 15, pull and release the trigger 15 times.  On the 16th pull, hold the trigger.  This will save your new firing rate and return you to the Preset Menu.  If you selected an invalid firing rate, you will see a red light after holding the trigger down.

# Burst Size #
Green lights will blink indicating your current burst size.  To set a new burst size, pull the trigger as many times as your new burst rate (with at least 1 second between pulls).  For example, for a burst size of 5, pull and release the trigger 5 times.  On the 6th pull, hold the trigger.  This will save your new burst size and return you to the Preset Menu.  If you selected an invalid burst size, you will see a red light after holding the trigger down.

# Ammo Limit #
Green lights will blink indicating your current ammo limit.  To set a new ammo limit, pull the trigger as many times as your new ammo limit (with at least 1 second between pulls).  For example, for an ammo limit of 10, pull and release the trigger 10 times.  On the 11th pull, hold the trigger.  This will save your new ammo limit and return you to the Preset Menu.  If you selected an invalid ammo limit, you will see a red light after holding the trigger down.

# Safety Shots #
Green lights will blink indicating your current number of safety shots.  To set a new safety shot value, pull the trigger as many times as the number of safety shots you require (with at least 1 second between pulls).  For example, for a safety shot size of 3, pull and release the trigger 3 times.  On the 4th pull, hold the trigger.  This will save your new safety shot size and return you to the Preset Menu.  If you selected an invalid safety shot size, you will see a red light after holding the trigger down.

# Advanced Programming #

In the advanced programming section, you are able to configure the DWELL and DEBOUNCE parameters.  To enter the Advanced Programming menu, use the following procedure:

  * Switch to safety
  * Press and hold the button in the trigger handle
  * Switch to "FA"
  * Continue to hold the button for at least 10+ seconds
  * Release the button
  * You should now be in programming mode (red blink green blink)

## DWELL ##

This is the first menu in the advanced programming section.  It is indicated by a single red blink immediately followed by a green blink, then a pause.  DWELL is the amount of time the Solenoid is powered.  The lower the DWELL the more battery is preserved, however, a lower DWELL may result in failure to fire properly.  The default value is 8ms and can be configured to anything between 2ms and 20ms.

## DEBOUNCE ##

The DEBOUNCE menu is indicated by a red blink immediately followed by a green blink, then repeated once more, before a pause (similar to DWELL, but a series of two blinks rather than one).  DEBOUNCE is the amount of time the trigger sensors need to be stable.  The default value is 20ms and can be configured anywhere between 5ms and 50ms.


# Exit programming #

## X7 phenom ##
Switch the selector switch to safety.

## X7 Classic ##
Push and hold the button in the trigger for 5+ seconds.  The board will power down.