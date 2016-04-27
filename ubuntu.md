### Initial
```
sudo apt update
sudo apt upgrade
```

### Customization


### Multimedia
* Codecs
```
sudo apt install ubuntu-restricted-extras
```
* Encrypted DVD playback
```
sudo apt install libdvd-pkg
sudo dpkg-reconfigure libdvd-pkg
```

### System tools

#### Java
###### Oracle Java ([link](http://www.webupd8.org/2012/09/install-oracle-java-8-in-ubuntu-via-ppa.html))
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt update
sudo apt install oracle-java8-installer
```
```
sudo apt install oracle-java8-set-default
```
###### OpenJDK (patched with font fixes) ([link](http://www.webupd8.org/2013/06/install-openjdk-patched-with-font-fixes.html))
```
sudo add-apt-repository ppa:no1wantdthisname/openjdk-fontfix
sudo apt update
sudo apt install in openjdk-8-jdk
```

```
sudo update-alternatives --config java
```

### Applications
#### Internet
###### TeamViever
```
sudo apt install libxtst6:i386 libxrandr2:i386
```
```
wget http://download.teamviewer.com/download/teamviewer_i386.deb
```
```
sudo dpkg --add-architecture i386
sudo apt update
```
```
sudo dpkg -i teamviewer_linux*.deb
apt-get -f install
```

Commands
- Show current status of the TeamViewer daemon
```
sudo teamviewer --daemon status
```
- Start TeamViewer daemon
```
sudo  --daemon start
```
- Stop TeamViewer daemon
```
sudo teamviewer --daemon stop
```
- Restart TeamViewer daemon
```
sudo teamviewer --daemon restart
```
- Disable TeamViewer daemon - don't start daemon on system startup
```
sudo teamviewer --daemon disable
```
- Enable TeamViewer daemon - start daemon on system startup (default)
```
sudo teamviewer --daemon enable
```
###### Telegram
```
sudo add-apt-repository ppa:atareao/telegram
sudo apt update
sudo apt install telegram
```
#### Office
###### Okular
```
sudo apt install okular
sudo apt install okular-extra-backends 
```

### Development
###### Ubuntu Make
```
sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make
sudo apt update
sudo apt install ubuntu-make
```
### Fixes & Hacks
###### Unity Tweak Tool
```
sudo apt install unity-tweak-tool
```

### Troubleshooting
#### Error:  Diskfilter writes are not supported ([link](http://askubuntu.com/questions/468466/diskfilter-writes-are-not-supported-what-triggers-this-error))

This is a bug that occurs in the most recent version of Ubuntu Server LTS (Ubuntu Server 14.04 LTS), when you create the boot partition (or the root partition, when the boot partition doesn't exists) inside a LVM or a RAID partition.

The correct solution should consider disable the save_env statements when GRUB is inside LVM or RAID partitions.

* Download
```
wget https://gist.githubusercontent.com/rarylson/da6b77ad6edde25529b2/raw/99f266a10e663e1829efc25eca6eddb9412c6fdc/00_header_patched
```
* Apply
```
mv /etc/grub.d/00_header /etc/grub.d/00_header.orig
mv 00_header_patched /etc/grub.d/00_header
```
* Disable the old script and enable the new one
```
chmod -x /etc/grub.d/00_header.orig
chmod +x /etc/grub.d/00_header
```
* Update Grub
```
update-grub
```

#### Fix time differences between ubuntu and windows ([link](http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html))

To fix the UTC / local time difference between Ubuntu and Windows from Ubuntu by making Ubuntu use local time.

###### For Ubuntu 16.04 and newer
```
timedatectl set-local-rtc 1
```
###### For Ubuntu versions older than 16.04
```
sudo sed -i 's/UTC=yes/UTC=no/' /etc/default/rcS
```
  And reboot.
  
###### Windows

Fixing this from Windows (it should work with Vista SP2, Windows 7, Server 2008 R2 and Windows 8/8.1), by making it use UTC instead of local time, download [THIS](https://help.ubuntu.com/community/UbuntuTime?action=AttachFile&do=get&target=WindowsTimeFixUTC.reg) Windows registry file and simply double click it.

Then, to disable the Windows Time service (which still writes local time to RTC regardless of the registry setting above, on shutdown), run Command Prompt as Administrator and paste this command:
```
sc config w32time start= disabled
```
And reboot.

###### Reverting changes
```
timedatectl set-local-rtc 0
```
or
```
sudo sed -i 's/UTC=no/UTC=yes/' /etc/default/rcS
```
or
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]
"RealTimeIsUniversal"=-
```
```
sc config w32time start= demand
```
And reboot.
