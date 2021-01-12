# Xplorer64 -  Cheat Cartridge Resources

Information and resources on the Xplorer64 Cheat Cartridge for the Nintendo 64.

After obtaining one of these cartridges, and being a massive fan of its PSX counterpart.. I thought it time that the Xplorer64 got some love.

Looking around on the internet there is very little information on them at all.

Ive started to gather information on the cartridge itself, pinouts, tools and anything else I can lay my hands on. Much of this information is either missing, never been documented publically or currently hosted on old websites and forums and I wish to preserve this for future generations of N64 fans.

Once I have got my head around exactly what the CPLD is doing, I will then endeavour to recreate this old hardware using modern parts that are in production.

What you will find here :-

Folder    |Notes 
----------|--------------------------------------
3rdparty | third party xplorer64 applications
images | images of hardware.
roms | dumped Xplorer64 firmware images
updates | released updates from Blaze/FCD - packaged as they were
xp64 |  xp64 - RPi Xplorer64 comms utility

## Known PCB Versions

Version     |Info                            | Notes
------------|--------------------------------|------------
FCD-0003.1  |PAL English Model (Green Label) | ATF1508AS CPLD, AT90S1200A MCU, 2 x SST 29LE010 EEPROM

## Known Software Versions

This is where I need YOUR HELP. If you have one of these carts and use it, can you check the software version (press X in the menu). If it differs in any way to the below please let me know and I will add the detail here. If you have any beta/alpha/test versions of this software - please get in touch, youd make a grown man very very happy :)

Version|Dumped|Commands                    |Notes                                        |MD5/Notes2
-------|------|----------------------------|---------------------------------------------|----------------------
1.000  | No   | Unknown                    | Early version discussed in a forum post     |Undumped ( see https://assemblergames.org/viewtopic.php?t=60584 )
1.066  | No   | Unknown                    | Discussed in a forum post                   |Undumped ( see https://assemblergames.org/viewtopic.php?t=60584 )
1.067G | Yes  | Unknown                    | Version found in GoodN64 Set /Nesworld etc  |9137129a586e1bcab6ae81bac6b01275
1.067E | No   | 0x55, 0x57, 0x58           | Found on my cart - green label              |Undumped

### Commands

This column shows the commands that seem to be working via the command handler. The commands seem to follow the same format as used by the PSX versions of the cart (makes sense).

0x55 is Upload Firmware & Flash, 0x57 is Status (Menu/Game etc) and 0x58 seems to be upload bin & flash but this needs checking.

For more infomation on the commands see here https://github.com/psx-spx/psx-spx.github.io/blob/master/cheatdevices.md#xplorer-parallel-port-commands-from-pc-side
Xplorer low level protocol information can also be found on this same page.

## xp64 - Flash/Update Utility for RaspberryPi

I am writing a utility, xp64 that replaces the need to use xkiller or the original DOS update utility.

It uses a RaspberryPi single board computer to communicate with the Xplorer64 using the RaspberryPi GPIO inputs/outputs.
That will probably be limited to flash updating and nothing else.. so at least you should be able to flash a rom with a new cheatlist if needed.

I have started writing the code for the flash update, I just need to socket the EEPROMs on my cart before testing it.

