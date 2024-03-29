# Xplorer64 -  Cheat Cartridge Resources

Information and resources on the Xplorer64 Cheat Cartridge for the Nintendo 64.

After obtaining one of these cartridges, and being a massive fan of its PSX counterpart.. I thought it time that the Xplorer64 got some love.

Looking around on the internet there is very little information on them at all.

Ive started to gather information on the cartridge itself, pinouts, tools and anything else I can lay my hands on. Much of this information is either missing, never been documented publically or currently hosted on old websites and forums and I wish to preserve this for future generations of N64 fans.

Update Jan 2024 - As you can see from the comments in issues - Modman has made major progress in reverse engineering the obfuscation and also some of the IO ports as well as adding support to the Sanni cart reader. There will be a massive update to this repository shorly. However for more info on the obfuscation etc see here https://github.com/RWeick/FCD-0003.1S-Xplorer64/tree/main


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
FCD-0003.1S |PAL English Model (Red Label)   | ATF1508AS CPLD, AT90S1200A MCU, 2 x SST 29EE010 EEPROM

## Known Software Versions

This is where I need YOUR HELP. If you have one of these carts and use it, can you check the software version (press X in the menu). If it differs in any way to the below please let me know and I will add the detail here. If you have any beta/alpha/test versions of this software - please get in touch, youd make a grown man very very happy :)

I have 4 carts - 3x1.067E, 1x1.00

Version|Dumped|Commands                    |Notes                                        |MD5/Notes2
-------|------|----------------------------|---------------------------------------------|----------------------
1.000  | No   | 0x55, 0x57, 0x58           | Found on a cart - green label               |Undumped 
1.066  | No   | Unknown                    | Discussed in an Assemblergames forum post   |Undumped
1.067G | Yes  | 0x55, 0x57, 0x58           | Version found in GoodN64 Set /Nesworld etc  |9137129a586e1bcab6ae81bac6b01275
1.067E | No   | 0x55, 0x57, 0x58           | Found on my cart - green label              |see /roms

### Commands

This column shows the commands that seem to be working via the command handler. The commands seem to follow the same format as used by the PSX versions of the cart (makes sense).

0x55 is Upload Firmware & Flash, 0x57 is Status (v1.000 & v1.067 return 0x36) and 0x58 seems to be upload bin to addr & call addr (SetMem&Exec). I have successfully tested uploading & executing which works perfectly using a small test program from one of PeterLemons N64 Assembly examples.

For more infomation on the commands see here https://psx-spx.consoledev.net/cheatdevices/#cheat-devices-xplorer-db25-parallel-port-function-summary
Xplorer low level protocol information can also be found on this same page.

## xp64 - Flash/Update Utility for RaspberryPi

I am writing a utility, xp64 that replaces the need to use xkiller or the original DOS update utility.

It uses a RaspberryPi single board computer to communicate with the Xplorer64 using the GPIO header.
That will probably be limited to flash updating and nothing else.. so at least you should be able to flash a rom with a new cheatlist if needed.

I have started writing the code for the flash update, I just need to socket the EEPROMs on my cart before testing it.

## Thanks & Shouts

Modman/RWeick - amazing work on xplorer64 reverse engineering - 
Tim Schuerewegen - for xflash/xkiller and being super helpful with information that saved me a hell of a lot of time.
Martin Korth/noca$h - for the psx-spex documents - especially the xplorer sections
Nicolas Noble - for bringing psx-spex to github and converting to MD

Last and by no means least, Squaresoft74 for the very kind donation of a Xplorer64 - many thanks and very much appreciated!

Shoutouts to N64brew & #PSXDev Discord
