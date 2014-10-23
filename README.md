SAURON CONFIG:


##INSTALL SUDO
```bash
$ su
$ apt-get install sudo
$ adduser sauron sudo
$ exit
```


## Static IP (NOT WORKING ATM)

```bash
$ sudo nano /etc/network/interfaces

iface eth0 inet static
    address 10.0.0.10
    netmask 255.255.255.0
    network 10.0.0.0
    broadcast 10.0.0.255
    gateway 10.0.0.1

$ sudo nano /etc/resolv.conf

nameserver 8.8.8.8
nameserver 10.0.0.1



$ sudo /etc/init.d/networking restart

```



##Install rtorrent + rutorrent with [rtorrent auto install](https://github.com/Kerwood/rtorrent.auto.install)
```bash
$ cd /tmp
$ wget https://raw.github.com/Kerwood/rtorrent.auto.install/master/rtorrent.auto.install-NEWEST-VERSION
$ chmod +x rtorrent.auto.install-NEWEST-VERSION
$ sudo ./rtorrent.auto.install-NEWEST-VERSION

* Choose all plugins
* Change the theme to oblivion @ rutorrent settings


TODO CHANGE RTORRENT CONFIG
```


##Install Plex Media Server: [PLEX INSTALL GUIDE](https://forums.plex.tv/index.php/topic/51427-plex-media-server-for-debian/)
```bash
$ sudo apt-get install curl
$ echo "deb http://shell.ninthgate.se/packages/debian squeeze main" | sudo tee -a /etc/apt/sources.list.d/plexmediaserver.list
$ sudo curl http://shell.ninthgate.se/packages/shell-ninthgate-se-keyring.key | sudo apt-key add -
$ sudo apt-get update
$ sudo apt-get install plexmediaserve
``

##Install ZSH And oh-my-zsh
```bash
$ sudo apt-get install zsh
$ git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
$ cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
$ sudo chsh -s /bin/zsh sauron
```

