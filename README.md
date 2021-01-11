# Xplorer64 - Nintendo Cheat Cartridge Resources

Information and resources on the Xplorer64 Cheat Cartridge for the Nintendo 64.

After obtaining one of these cartridges, and being a massive fan of its PSX counterpart.. I thought it time that the Xplorer64 got some love.

Looking around on the internet there is very little information on them at all.

Ive started to gather on the cartridge itself, pinouts, tool and other information. Much of this information is either missing, never been documented publically or currently hosted on old websites and forums to see what capabilities it has and what it is capable of.

## Known Hardware Versions

FCD-0003.1 - PAL English Model (Green Label) - ATF1508AS CPLD, AT90S1200A MCU & 2 x 29LE010 Flash

## Known Software Versions

This is where I need YOUR HELP. If you have one of these carts and use it, can you check the software version (press X in the menu). If it differs in any way to the below please let me know and I can try and add the detail here. If you have any beta/alpha/test versions of this software - please get in touch, youd make a grown man very very happy :)

Version|Dumped|Commands                    |Notes
-------|------|----------------------------|--------------
1.067G | Yes  | Unknown                    | Update seems to have originated from the German Blaze website. 
1.067E | No   | 0x55, 0x57, 0x58           | Found on my cart - green label     


## xp64 - Flash/Update Utility for RaspberryPi

I am writing a utility, xp64 that replaces the need to use xkiller or the original DOS update utility.

It uses a RaspberryPi single board computer to communicate with the Xplorer64 using the RaspberryPi GPIO inputs/outputs.
That will probably be limited to flash updating and nothing else.. so at least you should be able to flash a rom with a new cheatlist if needed.

I have started writing the code for the flash update, I just need to socket the EEPROMs on my cart before testing it.

