# Setting up Windows To Go
Windows To Go was a new feature introduced in Windows 8 which allows Windows to be installed on a USB drive and booted from.  
This how-to aims to make a simple-enough tutorial on how to set one up and get started  
### Requirements
* a "Fixed" drive
  * will not work if Windows recognizes it as a "Removable" drive
  * external hard drives will also work 
  * you can tell on Linux by running this in a terminal: <pre><code>dmesg | grep "Attached SCSI" | tail -n 1</code></pre>
    the result will either contain "Attached SCSI Disk" or "Attached SCSI removable disk" and only applies to the last drive inserted
* an install ISO for Windows 8 or later (so 8, 8.1, 10, but no 7, XP, etc)
  * download links: 
    * [Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)
    * 
  
### 


#### Further Reading and Help
* http://www.admin-magazine.com/Articles/Putting-Windows-8-on-a-USB-Drive
* http://www.howtogeek.com/196817/how-to-create-a-windows-to-go-usb-drive-without-the-enterprise-edition/
