## Packages
### Initial install
##### Some libs & soft
```
sudo apt install build-essential dpkg-dev gnupg2 gcc cmake libpcre3 libpcre3-dev zlib1g zlib1g-dev openssl libssl-dev lsb-release ca-certificates apt-transport-https software-properties-common lm-sensors gnome-nettools git dconf-editor curl wget htop mc zsh openssh-server unace rar unrar zip unzip p7zip-full p7zip-rar ubuntu-restricted-extras
```
##### XClip (Provides an interface to X selections from the command line)
```
sudo apt install xclip
```
##### Set of user-space tools for in-kernel CIFS filesystem
```
sudo apt install cifs-utils
```
##### Font manager
```
sudo apt install font-manager
```
##### Secure SHell FileSystem
```
sudo apt install sshfs
```
##### OhMyZsh
```
chsh -s /bin/zsh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
##### Double Commander
```
sudo add-apt-repository ppa:alexx2000/doublecmd
sudo apt-get update
sudo apt-get install doublecmd-gtk
```
### Multimedia
##### Mpd & Cantata
```
sudo add-apt-repository ppa:ubuntuhandbook1/cantata-qt 
sudo apt update 
sudo apt install mpd cantata
```
### Internet & Network
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
sudo apt install telegram-desktop
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
##### Vivaldi
[How to use H.264, MP3 and AAC support ln Vivaldi for Linux, via an alternative FFMpeg library](https://gist.github.com/ruario/bec42d156d30affef655)
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
##### MComix
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install mcomix
```
### Development
##### PHPStorm EAP
Go to [https://confluence.jetbrains.com/display/PhpStorm/PhpStorm+Early+Access+Program](https://confluence.jetbrains.com/display/PhpStorm/PhpStorm+Early+Access+Program)
```
wget http://download.jetbrains.com/webide/PhpStorm-EAP-162.646.18.tar.gz
tar xvf PhpStorm-EAP-162.646.18.tar.gz
sudo mv PhpStorm-162.646.18 /opt/phpstorm
sudo ln -s /opt/phpstorm/bin/phpstorm.sh /usr/local/bin/phpstorm

```

##### Java
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
##### MongoDB
```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
```
```
echo "deb [ arch=amd64,arm64 ] http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list
```
```
sudo apt-get update
```
```
sudo apt-get install -y mongodb-org
```
```
sudo service mongod start
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
###### /home/user/.rvm/scripts/cli:314: parse error near 'apt'

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
###### PHP 8.1
Add repository
```
sudo add-apt-repository ppa:ondrej/php
```
Updating
```
sudo apt update
```
Installing php and commonly used extensions
```
sudo apt install php8.1
sudo apt install php8.1-{bcmath,xml,fpm,mysql,zip,intl,ldap,gd,cli,bz2,curl,mbstring,pgsql,opcache,soap,cgi}
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
##### (Alternative) Configure Nginx as a Reverse Proxy for Apache ([link](https://www.digitalocean.com/community/tutorials/how-to-configure-nginx-as-a-reverse-proxy-for-apache))

##### Apache
```
sudo apt-get install apache2
```
```
sudo nano /etc/apache2/ports.conf
```
```
NameVirtualHost 127.0.0.1:8080
Listen 127.0.0.1:8080
```
```
sudo cp /etc/apache2/sites-available/default /etc/apache2/sites-available/test.loc
```
```
sudo nano /etc/apache2/sites-available/test.loc
```
```
<VirtualHost *:8080>
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
sudo a2ensite test.loc
```
```
sudo service apache2 restart
```
##### PHP
```
sudo apt install php libapache2-mod-php php-mcrypt php-mysql php-cli php-curl php-gd php-sqlite3 php-tidy php-xmlrpc php-imagick php-mbstring php-gettext
```
##### Nginx (from source with brotli https://github.com/pepelsbey/playground/blob/main/56/1-server.md)
```
sudo curl -L https://nginx.org/keys/nginx_signing.key | apt-key add -
```
```
sudo nano /etc/apt/sources.list.d/nginx.list

deb http://nginx.org/packages/ubuntu/ focal nginx
deb-src http://nginx.org/packages/ubuntu/ focal nginx
sudo apt update -y
```
```
cd /usr/local/src
sudo apt source nginx
```
```
sudo apt build-dep nginx -y
```
```
sudo git clone --recursive https://github.com/google/ngx_brotli.git
```
```
cd /usr/local/src/nginx-*/
sudo nano debian/rules

Add --add-module=/usr/local/src/ngx_brotli in configure
```
```
sudo dpkg-buildpackage -b -uc -us
```
```
sudo dpkg -i /usr/local/src/*.deb
```
```
sudo nano /etc/nginx/nginx.conf
```
```
user www-data;
worker_processes auto;
pid /var/run/nginx.pid;

events {
    worker_connections 768;
}

include /etc/nginx/sites-enabled/*.stream;

http {

    # Basic

    sendfile on;
    tcp_nopush on;
    tcp_nodelay on;
    types_hash_max_size 2048;
    server_tokens off;
    ignore_invalid_headers on;

    # Decrease default timeouts to drop slow clients

    keepalive_timeout 40s;
    send_timeout 20s;
    client_header_timeout 20s;
    client_body_timeout 20s;
    reset_timedout_connection on;

    # Hash sizes

    server_names_hash_bucket_size 64;

    # Mime types

    default_type  application/octet-stream;
    include /etc/nginx/mime.types;

    # Logs

    log_format main '$remote_addr - $remote_user [$time_local] "$request" $status $bytes_sent "$http_referer" "$http_user_agent" "$gzip_ratio"';
    access_log /var/log/nginx/access.log main;
    error_log /var/log/nginx/error.log warn;

    # Limits

    limit_req_zone  $binary_remote_addr  zone=dos_attack:20m   rate=30r/m;

    # Gzip

    gzip on;
    gzip_disable "msie6";
    gzip_vary off;
    gzip_proxied any;
    gzip_comp_level 5;
    gzip_min_length 1000;
    gzip_buffers 16 8k;
    gzip_http_version 1.1;
    gzip_types
        application/atom+xml
        application/javascript
        application/json
        application/ld+json
        application/manifest+json
        application/rss+xml
        application/vnd.geo+json
        application/vnd.ms-fontobject
        application/x-font-ttf
        application/x-web-app-manifest+json
        application/xhtml+xml
        application/xml
        font/opentype
        image/bmp
        image/svg+xml
        image/x-icon
        text/cache-manifest
        text/css
        text/plain
        text/vcard
        text/vnd.rim.location.xloc
        text/vtt
        text/x-component
        text/x-cross-domain-policy;

    # Brotli

    brotli on;
    brotli_comp_level 6;
    brotli_types
        text/xml
        image/svg+xml
        application/x-font-ttf
        image/vnd.microsoft.icon
        application/x-font-opentype
        application/json
        font/eot
        application/vnd.ms-fontobject
        application/javascript
        font/otf
        application/xml
        application/xhtml+xml
        text/javascript
        application/x-javascript
        text/$;

    # Virtual Hosts

    include /etc/nginx/sites-enabled/*;

    # Configs

    include /etc/nginx/conf.d/*.conf;
    include /usr/share/nginx/modules/*.conf;

}
```
```
sudo mkdir -p /etc/nginx/sites-available/
sudo mkdir -p /etc/nginx/sites-enabled/
```
```
sudo mkdir -p /var/www/example.com/html
```
```
sudo nano /etc/nginx/sites-available/example.com.conf
```
```
server {
    listen 80;
    listen [::]:80;

    server_name example.com www.example.com;
    root /var/www/example.com/html;
    index index.html index.xml;

    location ~ \.php$ {
        #NOTE: You should have "cgi.fix_pathinfo = 0;" in php.ini
        include fastcgi_params;                
        fastcgi_intercept_errors on;
        fastcgi_pass unix:/run/php/php8.1-fpm.sock;
        fastcgi_param SCRIPT_FILENAME $document_root/$fastcgi_script_name;
    }

}

```
```
sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/
```
```
sudo systemctl restart nginx
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
#### Personal Access Token (https://stackoverflow.com/questions/46645843/where-to-store-my-git-personal-access-token)
Store PAT permanently in a file with git commands ```git config credential.helper store``` (don't use --global). This is NOT ENCRYPTED. You can open the file and read it. (e.g., If someone gets access to your laptop they can pretty much read the Password using a bootable USB (assuming your whole system is not encrypted)).

## Customization
##### Grub customizer
```
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt update
sudo apt install grub-customizer
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

### Fix tearing on NVIDIA 
```
sudo nano /usr/share/lightdm/lightdm.conf.d/50-xserver-command.conf
```

```
xserver-command=X *-bs* -core
```

```
sudo service lightdm restart
```

### How to diagnose/fix very slow boot on Ubuntu 18.04

1. Edit the file /etc/default/grub file so that the string noresume is included in the GRUB_CMDLINE_LINUX_DEFAULT line, for example:

```
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash noresume"
```

2. Run this command to update GRUB:

```
sudo update-grub
```

3. Reboot the computer


## Usefull commands
### Search package by name and version
```
sudo apt-cache show package | grep -i version
```










