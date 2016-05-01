### System tools
###### Git
```
sudo apt install git
```
###### Synaptic
```
sudo apt install synaptic
```
###### dconf-editor
```
sudo apt install dconf-editor
```
###### Compiz config & plugins
```
sudo apt install compizconfig-settings-manager compiz-plugins
```
###### Unity Tweak Tool
```
sudo apt install unity-tweak-tool
```
###### Ubuntu Tweak
```
wget http://archive.getdeb.net/ubuntu/pool/apps/u/ubuntu-tweak/ubuntu-tweak_0.8.7-1~getdeb2~xenial_all.deb
sudo dpkg -i ubuntu-tweak_0.8.7-1~getdeb2~xenial_all.deb
sudo apt install -f
```
###### Grub customizer
```
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt update
sudo apt install grub-customizer
```
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
### Customizing
###### GTK engines (needed for Skype)
```
sudo apt install gtk2-engines-murrine:i386 gtk2-engines-pixbuf:i386
```
####### My Weather Indicator
```
sudo add-apt-repository ppa:atareao/atareao
sudo apt update
sudo apt install my-weather-indicator
```
###### Caffeine
```
sudo apt install caffeine
```

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

### Internet
###### Telegram
```
sudo add-apt-repository ppa:atareao/telegram
sudo apt update
sudo apt install telegram
```
###### Skype
```
sudo apt install skype
sudo apt -f install
sudo apt install sni-qt:i386
```
###### Skype wrapper
```
sudo add-apt-repository ppa:skype-wrapper/ppa
sudo apt update
sudo apt install skype-wrapper

```

###### Pidgin
```
sudo apt install pidgin
```
###### Telegram Purple plugin for Pidgin
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install telegram-purple
```
###### Dropbox
```
sudo sh -c 'echo "deb http://linux.dropbox.com/ubuntu $(lsb_release -sc) main" >> /etc/apt/sources.list.d/dropbox.list'
sudo apt-key adv --keyserver pgp.mit.edu --recv-keys 1C61A2656FB57B7E4DE0F4C1FC918B335044912E
sudo apt update 
sudo apt install dropbox
```
or download .deb package from here
```
https://www.dropbox.com/ru/install?os=lnx
```
###### Google Chrome
```
sudo sh -c 'echo "deb [arch=amd64] http://dl-ssl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo apt update
sudo apt install google-chrome-stable
```
###### Chromium & PepperFlash
```
sudo add-apt-repository ppa:canonical-chromium-builds/stage
sudo apt update
sudo apt install chromium-browser pepperflashplugin-nonfree
```
###### Opera
###### Opera Dev
###### Vivaldi
[How to use H.264, MP3 and AAC support ln Vivaldi for Linux, via an alternative FFMpeg library](https://gist.github.com/ruario/bec42d156d30affef655)
###### Firefox Development Edition
### Games
###### NES
###### SNES
###### Sega Gen

### Office

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
###### Sublime text 3
###### IntelliJ IDEA
###### Java
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
###### NodeJS
###### Python
###### Ruby
###### LAMP
###### Apache Virtual Hosts ([link](https://www.vultr.com/docs/apache-virtual-hosts-on-ubuntu-14-04-lts))
```
sudo mkdir /var/www/test.loc
```
```
sudo chown -R $USER:$USER /var/www/test.loc
```
```
sudo chmod -R 755 /var/www
```
```
nano /var/www/test.loc/index.html
```
```
<html>
  <head>
    <title>test.loc</title>
  </head>
  <body>
    <h1>test.loc virtual host !</h1>
  </body>
</html>
```
```
sudo cp /etc/apache28/sites-available/000-default.conf /etc/apache2/sites-available/test.loc.conf
```
```
sudo nano /etc/apache2/sites-available/test.loc.conf
```
```
<VirtualHost *:80>
    ServerAdmin admin@test.loc
    ServerName test.loc
    ServerAlias www.test.loc
    DocumentRoot /var/www/test.loc
</VirtualHost>
```
```
sudo a2ensite test.loc.conf
```
```
sudo nano /etc/hosts
127.0.0.1 test.loc
```
```
sudo service apache2 restart
```
### Configuration
###### Generating SSH key
```
ssh-keygen -t rsa -C "your_email@example.com"
```
###### Setup git defaults
```
git config --global user.name your name
git config --global user.email your@email.com
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
