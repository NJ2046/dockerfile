# Question
```
vnc
linux 桌面环境
qt xcb
```
# Solve
```
ssh -X user@RPi /path/to/your/Qt/app -platform xcb
ssh  -X root@172.17.7.152 /home/nj/nl/code/Company/ai-eng-ppocrlabel/P
addleOCR-dygraph/PPOCRLabel/PPOCRLabel.py -platform xcb
```
# PPL
```
docker run -i -t --name xfce1 -p 8866:5900 -e RESOLUTION=1400x900 vncppl:v1
Hie1ahzua6wu
更换连接的色彩
```
# Docker
```
docker run -i -t --name xfce1 -p 20466:5900 -e RESOLUTION=1400x900 172.16.1.10:8900/app/vnc:6.0
ssh login password: Ohk1aed6aeya


docker pull 172.16.1.10:8900/app/vnc:1.0
docker run -it --rm -p 5909:5901 -e USER=root 172.16.1.10:8900/app/vnc:1.0 \
    bash -c "vncserver :1 -geometry 1280x800 -depth 24 && tail -F /root/.vnc/*.log"

docker pull 172.16.1.10:8900/app/vnc:3.0
docker run -it -d -p 5901:5901 blacs30/dockerfile-ubuntu-gnome
pw:acoman

docker pull paopaorobot/ubuntu-xfce-vnc
docker pull 172.16.1.10:8900/app/vnc:6.0

docker run -i -t --name xfce1 -p 20466:5900 -e RESOLUTION=1400x900 172.16.1.10:8900/app/vnc:6.0
ssh login password: Ohk1aed6aeya
```
# Primary
```
vnc://172.17.7.152:5903
qazwsx
vnc://172.16.0.21:5903
qazwsx

apt-get install vnc4server
vnc4passwd
vnc4server -geometry 1400x900 :3
vnc4server -kill :3


nj
#!/bin/sh
unset SESSION_MANAGER
exec /etc/X11/xinit/xinitrc
[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
#xterm -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
#twm &
gnome-session &



21
#!/bin/sh
# Uncomment the following two lines for normal desktop:
# unset SESSION_MANAGER
# exec /etc/X11/xinit/xinitrc

[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
# x-terminal-emulator -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
# x-window-manager &

gnome-panel &
gnome-settings-daemon &
metacity &
nautilus &


21
#!/bin/sh
#
# Config requires following packages:
# gnome-panel nautilus gnome-terminal metacity
#


export XKL_XMODMAP_DISABLE=1

unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
    
[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey

gnome-session &
gnome-panel &

metacity &
gnome-terminal &


10
#!/bin/sh

export XKL_XMODMAP_DISABLE=1
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS

#exec sh /etc/Xll/xinit/xinitrc

[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources


gnome-session &
gnome-panel &
gnome-settings-daemon &
metacity &
nautilus &
gnome-terminal &

```

