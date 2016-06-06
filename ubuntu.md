## Packages
### Initial install
```
sudo apt install git synaptic dconf-editor compizconfig-settings-manager compiz-plugins unity-tweak-tool build-essential vim mercurial meld curl htop xclip unzip gdebi preload bleachbit cifs-utils unace unrar zip p7zip-full p7zip-rar sharutils rar openssh-server libssl-dev lm-sensors font-manager sshfs mc
```
OR
```
sudo apt install git
```
##### GTK+-based graphical user interface for Advanced Packaging Tool (APT)
```
sudo apt install synaptic
```
##### Low-level key/value database designed for storing desktop environment settings.
```
sudo apt install dconf-editor
```
##### Compiz settings manager with plugins
```
sudo apt install compizconfig-settings-manager compiz-plugins
```
##### Unity tweak tool
```
sudo apt install unity-tweak-tool
```
##### Vim
```
sudo apt install vim
```
##### Mercurial (Free, distributed source control management tool)
```
sudo apt install mercurial
```
##### Meld (Visual diff and merge tool targeted at developers)
```
sudo apt install meld
```
##### cURL (A tool for client-side URL transfers)
```
sudo apt install curl
```
##### Htop (An interactive process viewer for Unix)
```
sudo apt install htop
```
##### XClip (Provides an interface to X selections from the command line)
```
sudo apt install xclip
```
##### Archive stuff
```
sudo apt install unace rar unrar zip unzip p7zip-full p7zip-rar
```
##### GDebi Package Installer
```
sudo apt install gdebi
```
##### Preload (Records statistics about usage of programs using Markov chains)
```
sudo apt install preload
```
##### BleachBit (Quickly frees disk space and tirelessly guards your privacy)
```
sudo apt install bleachbit
```
##### Set of user-space tools for in-kernel CIFS filesystem
```
sudo apt install cifs-utils
```
##### GNU Sharutils (Set of utilities to handle shell archives)
```
sudo apt install sharutils
```
##### OpenSSH
```
sudo apt install openssh-server libssl-dev
```
##### lm-sensors (Free and open-source application that provides tools and drivers for monitoring temperatures, voltage, and fans.)
```
sudo apt install lm-sensors
```
##### Font manager
```
sudo apt install font-manager
```
##### Secure SHell FileSystem
```
sudo apt install sshfs
```
##### Midnight Commander
```
sudo apt install mc
```
##### build-essential
```
sudo apt install build-essential
```
##### Zsh & OhMyZsh
```
sudo apt install zsh
chsh -s /bin/zsh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### Multimedia
##### Codecs
```
sudo apt install ubuntu-restricted-extras
```
##### Encrypted DVD playback
```
sudo apt install libdvd-pkg
sudo dpkg-reconfigure libdvd-pkg
```
##### SMPlayer
```
sudo add-apt-repository ppa:rvm/smplayer
sudo apt update
sudo apt install smplayer smtube smplayer-themes smplayer-skins
```
##### DeadBeef
```
sudo add-apt-repository ppa:starws-box/deadbeef-player
sudo apt update
sudo apt install deadbeef
```
##### Mpd & Cantata
```
sudo add-apt-repository ppa:ubuntuhandbook1/cantata-qt 
sudo apt update 
sudo apt install mpd cantata
```
### Internet & Network
##### Tools
```
sudo apt install whois traceroute nmap
```
##### TeamViever
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
sudo apt -f install
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
##### Telegram
```
sudo add-apt-repository ppa:atareao/telegram
sudo apt update
sudo apt install telegram
```
##### Skype
```
sudo apt install skype
sudo apt -f install
sudo apt install sni-qt:i386
```
##### Skype wrapper
```
sudo add-apt-repository ppa:skype-wrapper/ppa
sudo apt update
sudo apt install skype-wrapper
```
##### Pidgin
```
sudo apt install pidgin
```
##### Telegram Purple plugin for Pidgin
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install telegram-purple
```
##### Dropbox
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
##### Google Chrome
```
sudo sh -c 'echo "deb [arch=amd64] http://dl-ssl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo apt update
sudo apt install google-chrome-stable
```
##### Chromium & PepperFlash
```
sudo add-apt-repository ppa:canonical-chromium-builds/stage
sudo apt update
sudo apt install chromium-browser pepperflashplugin-nonfree
```
##### Opera
##### Opera Dev
##### Vivaldi
[How to use H.264, MP3 and AAC support ln Vivaldi for Linux, via an alternative FFMpeg library](https://gist.github.com/ruario/bec42d156d30affef655)
##### Firefox Development Edition
### Games
#### NES
##### FCEUX
```
sudo apt install fceux
```
##### Higan
```
sudo apt install higan
```
#### SNES
#### Sega Gen
##### GENS/GS
```
wget http://segaretro.org/images/7/75/Gens_2.16.7_i386.deb
sudo dpkg -i Gens_2.16.7_i386.deb
sudo apt install -f
```
##### Kega Fusion
```
wget http://www.carpeludum.com/download/kega-fusion_3.63-2_i386.deb
sudo dpkg -i kega-fusion_3.63-2_i386.deb
sudo apt install -f
```
### Office
##### Okular
```
sudo apt install okular
sudo apt install okular-extra-backends 
```
##### Libre Office
```
sudo apt install libreoffice-style-sifr
```
##### MComix
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install mcomix
```
### Development
##### Ubuntu Make
```
sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make
sudo apt update
sudo apt install ubuntu-make
```
##### Sublime text 3
```
wget https://download.sublimetext.com/sublime-text_build-3114_amd64.deb
sudo dpkg -i sublime-text_build-3114_amd64.deb
sudo apt -f install
```
##### IntelliJ IDEA
##### Java
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
sudo apt install openjdk-8-jdk
```

```
sudo update-alternatives --config java
```
##### NodeJS (nvm)
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
```
```
source ~/.profile  => (.profile to .zshrc)
```
```
nvm ls-remote
nvm install ...
nvm alias default ...
nvm use default
```

##### Python
```
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
```
```
nano .zshrc
export PATH="/home/auvarov/miniconda3/bin:$PATH"
source ~/.zshrc
```
```
conda update conda
```
##### Ruby (rvm)
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
```
```
\curl -sSL https://get.rvm.io | bash -s stable
```
```
rvm requirements 
rvm list known
rvm install ...
rvm use ...
```
###### /home/user/.rvm/scripts/cli:314: parse error near `apt'

I had the same problem until I put [[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" into a .zshenv file instead of the .zshrc file.

##### LAMP
###### Apache
```
sudo apt install apache2
```
Enable mod_rewrire
```
sudo a2enmod rewrite
```
###### MySQL
```
sudo apt install mysql-client mysql-server
sudo mysql_secure_installation
```
###### PHP
```
sudo apt install php libapache2-mod-php php-mcrypt php-mysql php-cli php-curl php-gd php-sqlite3 php-tidy php-xmlrpc php-imagick php-mbstring php-gettext
```

###### PHPMyAdmin
```
sudo apt install phpmyadmin
```

After the installation has completed, add phpmyadmin to the apache configuration.
```
sudo nano /etc/apache2/apache2.conf
```
Add the phpmyadmin config to the file.

```
Include /etc/phpmyadmin/apache.conf
```
```
sudo service apache2 restart
```
###### DBeaver (Free Universal Database Manager)
```
wget http://dbeaver.jkiss.org/files/dbeaver-ce_latest_amd64.deb
sudo dpkg -i dbeaver-ce_latest_amd64.deb
sudo apt install -f
```
###### MyCLI ([A Terminal Client for MySQL with AutoCompletion and Syntax Highlighting](https://github.com/dbcli/mycli))
```
pip install mycli
```
OR
```
condo install mycli
```
###### Composer
```
curl -s https://getcomposer.org/installer | php
sudo mv composer.phar /usr/local/bin/composer
```
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
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/test.loc.conf
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
    <Directory /var/www/test.loc>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Order allow,deny
        allow from all
    </Directory>
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
## Configuration
#### Generating SSH key
```
ssh-keygen -t rsa -C "your_email@example.com"
```
#### Setup git defaults
```
git config --global user.name your name
git config --global user.email your@email.com
```
## Customization
##### Ubuntu Tweak
```
wget http://archive.getdeb.net/ubuntu/pool/apps/u/ubuntu-tweak/ubuntu-tweak_0.8.7-1~getdeb2~xenial_all.deb
sudo dpkg -i ubuntu-tweak_0.8.7-1~getdeb2~xenial_all.deb
sudo apt install -f
```
##### Grub customizer
```
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt update
sudo apt install grub-customizer
```
##### GTK engines (needed for Skype)
```
sudo apt install gtk2-engines-murrine:i386 gtk2-engines-pixbuf:i386
```
##### My Weather Indicator
```
sudo add-apt-repository ppa:atareao/atareao
sudo apt update
sudo apt install my-weather-indicator
```
##### Caffeine
```
sudo apt install caffeine
```
##### Show username on panel
```
gsettings set com.canonical.indicator.session show-real-name-on-panel true
```
##### Change datetime format on panel

```
dcong-editor
```
Go to com/canonical/indicator/datetime:
```
%a, %e %b %Y %H:%M:%S 
```
##### Minimize apps on click
```
gsettings set org.compiz.unityshell:/org/compiz/profiles/unity/plugins/unityshell/ launcher-minimize-window true
```
##### Move The Unity Launcher
```
gsettings set com.canonical.Unity.Launcher launcher-position Bottom
```
## Other 
## Troubleshooting
### Error:  Diskfilter writes are not supported ([link](http://askubuntu.com/questions/468466/diskfilter-writes-are-not-supported-what-triggers-this-error))

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

### Fix time differences between ubuntu and windows ([link](http://www.webupd8.org/2014/09/dual-boot-fix-time-differences-between.html))

To fix the UTC / local time difference between Ubuntu and Windows from Ubuntu by making Ubuntu use local time.

##### For Ubuntu 16.04 and newer
```
timedatectl set-local-rtc 1
```
##### For Ubuntu versions older than 16.04
```
sudo sed -i 's/UTC=yes/UTC=no/' /etc/default/rcS
```
  And reboot.
  
##### Windows

Fixing this from Windows (it should work with Vista SP2, Windows 7, Server 2008 R2 and Windows 8/8.1), by making it use UTC instead of local time, download [THIS](https://help.ubuntu.com/community/UbuntuTime?action=AttachFile&do=get&target=WindowsTimeFixUTC.reg) Windows registry file and simply double click it.

Then, to disable the Windows Time service (which still writes local time to RTC regardless of the registry setting above, on shutdown), run Command Prompt as Administrator and paste this command:
```
sc config w32time start= disabled
```
And reboot.

##### Reverting changes
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







