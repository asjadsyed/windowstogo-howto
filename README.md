Setting up Windows To Go
========================

Windows To Go was a new feature introduced in Windows 8 which allows Windows to be installed on a USB drive and booted from.  
This how-to aims to make a simple-enough tutorial on how to set one up and get started  
### Requirements
* a "Fixed" drive
  * follow the instructions in the [Linux](#checkfixeddrivelinux) and [Windows](#checkfixeddrivewindows) sections to check if your drive will work with Windows To Go 
  * most external hard drives and some thumb drives will work 
* an install ISO for Windows 8 or later (so 8, 8.1, 10, but no 7, XP, etc)
  * download links: 
    * [Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)
    * [How-To Geek also maintains a list of where to get copies of Windows ISOs legally](http://www.howtogeek.com/186775/how-to-download-windows-7-8-and-8.1-installation-media-legally/) 
  
### How to check if your drive is a Fixed drive, from Linux <a name="checkfixeddrivelinux"></a>
run this in a terminal: 
```
dmesg | grep "Attached SCSI"
``` 
the result will either contain "Attached SCSI Disk" or "Attached SCSI removable disk" 

### How to check if your drive is a Fixed drive, from Windows <a name="checkfixeddrivewindows"></a>
right-click your drive in File Explorer  
if the menu has a Format option but not an Eject option, then it is a Fixed drive 


### Converting an install.esd file to an install.wim file


### Imaging your drive, from Linux

### Imaging your drive, from Windows

#### Further Reading and Help
* [Admin Magazine Guide](http://www.admin-magazine.com/Articles/Putting-Windows-8-on-a-USB-Drive)
* [How-To Geek Guide](http://www.howtogeek.com/196817/how-to-create-a-windows-to-go-usb-drive-without-the-enterprise-edition/)
* [ingramator's post on the Neowin forum](http://www.neowin.net/forum/topic/1134268-tutorialwindows-8-to-go-without-enterprise-edition/)
