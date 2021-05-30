# XRDP-OVER-UBUNTU-20.04-

### for ubuntu18.04 :

  sudo apt-get install xorg

  sudo apt-get install xserver-xorg-core

  sudo apt-get install xorgxrdp
  

sudo apt install xfce4

sudo apt install ubuntu-desktop

sudo apt install xrdp

sudo adduser xrdp ssl-cert

sudo ufw allow 3389

sudo ufw reload

# change desktop :

sudo update-alternatives --config x-session-manager

choose your environment

sudo systemctl restart xrdp

# in case of blank screen :

$ sudo vim /etc/xrdp/startwm.sh

Add these lines just before the lines that test & execute Xsession

unset DBUS_SESSION_BUS_ADDRESS

unset XDG_RUNTIME_DIR

# save

sudo systemctl restart xrdp
