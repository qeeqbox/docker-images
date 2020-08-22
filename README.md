<p align="center"> <img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/docker-images.png"></p>

#
[![Generic badge](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/qeeqbox/docker-images/master/info&label=version&query=$.version&colorB=blue)

Custom security focused images accessible via VNC, RDP or web. The images were customized with a minimal GUI and different settings to support the remote access. 

## Kali
<img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/kali.png" style="max-width:768px"/>

## Parrot
<img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/parrot.png" style="max-width:768px"/>

## Current builds
- Kali (qeeqbox/kali:1.0) 				2GB 
- Parrot (qeeqbox/parrot:1.0) 			5GB

## Running
```console 
docker run --privileged -it qeeqbox/kali:1.0
...
...
Successfully built 7c36ab06e878
Successfully tagged qeeqbox/kali:1.0

https://github.com/qeeqbox/docker-images

Custom Kali distro accessible via VNC, RDP or web browser

root pass -> EmBNjt^Zea
VNC pass  -> fjw#8fAwVC
VNC web   -> http://172.20.0.3:6080/index.html

```

## Changing resolution
- RDP (Change it using the clint app)
- VNC (Change it using `xrandr -s ...`)
- Web browser (Change it using `xrandr -s ...`)

## Installed tools
locales supervisor sudo xrdp ibus ibus-mozc dbus dbus-x11 software-properties-common evince firefox file-roller gnome-themes-standard gpicview gtk2-engines-pixbuf leafpad ttf-ubuntu-font-family xfce4 xfce4-whiskermenu-plugin xorg xserver-xorg xfce4-indicator-plugin xfce4-terminal numix-icon-theme numix-icon-theme-circle noVNC websockify Adwaita-dark-Xfce Qbox-wm4 websockify noVNC tigervnc-standalone-server git

## Roadmap
- Optimize big images
- Add self hosted registry (maybe)
- Convert my own LXD images to docker images

## Official images (Not custom ones)
- [kali](https://breakdance.github.io/breakdance/) 
- [Parrot OS](https://www.parrotsec.org/download/) 
- [BlackArch](https://blackarch.org/downloads.html/) 

## Licncess
- https://www.kali.org/EULA.txt
- https://hub.docker.com/u/kalilinux
- https://docs.parrotlinux.org/
- https://hub.docker.com/u/parrotsec
- https://github.com/BlackArch/blackarch/blob/master/COPYING

## Disclaimer\Notes
- Do not forget to visit Kali, Parrot OS and BlackArch websites for awesome resources or leaving feedback
- Do not use these images in deployment (These images are very larage..)
