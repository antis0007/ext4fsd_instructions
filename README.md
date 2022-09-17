# Ext4Fsd Instructions
Simple instructions on how to access a Linux filesystem through Windows

## Intro:
While searching for information on how to setup the latest version of the EXT4 file system driver for Windows, I found extremely cryptic posts, hyperlinks and vague instructions. It took me a few attempts to get this working, and I haven't tested it much, so perform this at your own risk. That said, it does allow me to access my entire linux filesystem from Windows 10 which is a godsend.

## Instructions:
1. Visit https://www.acc.umu.se/~bosse/ and download the latest beta version of their driver (Release 0.70 beta 3 (2021-02-02) as of writing this)
2. Open an elevated command prompt and run this command: "bcdedit /set testsigning on" (This allows for the filesystem driver to work, as it is testsigned)
3. Restart your computer
4. The program to configure your EXT4 drives and the driver is called "Ext2 Volume Manager", open it from the main menu
5. Navigate to [Tools > Service Management] and verify that Ext2Fsd has already started. If it hasn't, press start. If you didn't restart your computer after typing the command earlier it will say that it CANNOT start. This is because Windows 10 has blocked the driver from loading as it is unsigned. Please run that command and try again after restarting.
6. In the main pane, navigate to your EXT formatted drive, right click and assign/change drive letter if necessary. After this the drive should appear in File Explorer.

I will include a copy of the latest installer in this repository for archival reasons.


Credit to Bo Brantén
https://github.com/bobranten/ on Github

Original Repo:
https://github.com/bobranten/Ext4Fsd
