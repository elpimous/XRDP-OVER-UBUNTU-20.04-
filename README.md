# XRDP-OVER-UBUNTU-20.04-

### for ubuntu18.04 :

    sudo apt-get install xorg

    sudo apt-get install xserver-xorg-core

    sudo apt-get install xorgxrdp
  
----

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

# in case of "could-not-acquire-name-on-session-bus" white pannel :
> sudo nano /etc/xrdp/startwm.sh

#!/bin/sh
# xrdp X session start script (c) 2015 mirabilos
# publié sous la licence MirOS

if test -r /etc/default/locale; alors
. /etc/default/locale
test -z "${LANG+x}" || export LANG
test -z "${LANGUAGE+x}" || export LANGUE
test -z "${LC_ADDRESS+x}" || export LC_ADDRESS
test -z "${LC_ALL+x}" || exporter LC_ALL
test -z "${LC_COLLATE+x}" || exporter LC_COLLATE
test -z "${LC_CTYPE+x}" || export LC_CTYPE
test -z "${LC_IDENTIFICATION+x}" || export LC_IDENTIFICATION
test -z "${LC_MEASUREMENT+x}" || exporter le
test LC_MESURE -z "
test -z "${LC_MONETARY+x}" || export LC_MONETARY
test -z "${LC_NAME+x}" || exporter le
test LC_NAME -z "${LC_NUMERIC+x}" || exporter LC_NUMERIC
test -z "${LC_PAPER+x}" || exporter LC_PAPER
test -z "${LC_TELEPHONE+x}" || export LC_TELEPHONE
test -z "${LC_TIME+x}" || export LC_TIME
test -z "${LOCPATH+x}" || export LOCPATH
fi

unset DBUS_SESSION_BUS_ADDRESS

exec mate-session

#test -x /etc/X11/Xsession && exec /etc/X11/Xsession

#exec /bin/sh /etc/X11/Xsession
https://www.taringa.net/+ubuntuparataringeros/aporte-xrdp-could-not-acquire-name-on-session-bus_widb0
