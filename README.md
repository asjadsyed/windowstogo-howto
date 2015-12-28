Setting up Windows To Go
========================

Windows To Go was a new feature introduced in Windows 8 which allows Windows to be installed on a USB drive and booted from.  
This how-to aims to make a simple-enough tutorial on how to set one up and get started  
### Requirements
* a "Fixed" drive
  * follow [these instructions](#checkfixeddrive) to check if your drive will work with Windows To Go  
  * most external hard drives and some thumb drives will work  
* an install ISO for Windows 8 or later (so 8, 8.1, 10, but no 7, XP, etc)  
  * download links:  
    * [Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)
    * [How-To Geek also maintains a list of where to get copies of Windows ISOs legally](http://www.howtogeek.com/186775/how-to-download-windows-7-8-and-8.1-installation-media-legally/)  
 * a working Linux or Windows machine
 * 


--------------------------------

## How to check if your drive is a Fixed drive <a name="checkfixeddrive"></a>
#### Linux
run this in a terminal: 
```
dmesg | grep "Attached SCSI"
``` 
the result will either contain "Attached SCSI Disk" or "Attached SCSI removable disk" 

#### Windows
right-click your drive in File Explorer  
if the menu has a Format option but not an Eject option, then it is a Fixed drive 

--------------------------------

## Extracting the install.wim file


## Converting an install.esd file to an install.wim file
some Windows ISOs (like the 8.1 ones) will have an install.esd file instead of an install.wim file  
to convert an esd file to a wim file, open a Command Prompt as an Administrator and navigate to your Windows To Go files like so:  
```
X:
cd WindowsToGo\
```
from there, running this will start the conversion:
```
dism /Export-Image /SourceImageFile:install.esd /SourceIndex:1 /DestinationImageFile:install.wim /Compress:recovery /CheckIntegrity
```
if you don't have the DISM commandline program, see the [section on getting the WAIK and ADK tools](#gettingwaikandadktools)  
and then replace "dism" with the full path of the exe (e.g. "X:\WindowsToGo\ADK_6\amd64\Dism\dism.exe")  

--------------------------------

## Imaging your drive
#### Linux
#### Windows

--------------------------------

## Getting the Windows Automated Installation Kit (WAIK) and Assessment and Deployment Kit (ADK) tools <a name="gettingwaikandadktools"></a>
the simplest way to get them is with GetWaikTools  
[RMPrepUSB has a link](http://www.rmprepusb.com/tutorials/getwaiktools) to download the application, although the application was originally hosted on [a forum post on The Oven](http://theoven.org/index.php?topic=287.)  
this method will download the tools you need, nothing more and nothing less  
the other method involves downloading, extracting, and installing huge packages from Microsoft just to get just a couple of commandline programs  
  
the two checkboxes you want to select are Dism and ADK Tools for your version of Windows  
the tools will be downloaded into folders like so: \\[Version of Windows]\\[Architecture]\\[Program Name]\\  

| Architecture       | Folder             |
|--------------------|--------------------|
| 64-bit             | amd64              |
| 32-bit             | x86                |

| Version of Windows | Folder             |
|--------------------|--------------------|
| Windows 10         | ADK_6              |
| Windows 8.1        | ADK_5              |
| Windows 8          | ADK_4              |
| Windows 7          | ADK_3              |

--------------------------------

#### Further Reading and Help
* [Admin Magazine Guide](http://www.admin-magazine.com/Articles/Putting-Windows-8-on-a-USB-Drive)
* [How-To Geek Guide](http://www.howtogeek.com/196817/how-to-create-a-windows-to-go-usb-drive-without-the-enterprise-edition/)
* [ingramator's post on the Neowin forum](http://www.neowin.net/forum/topic/1134268-tutorialwindows-8-to-go-without-enterprise-edition/)
