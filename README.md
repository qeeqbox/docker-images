<p align="center"> <img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/docker-images.png"></p>

#
[![Generic badge](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/qeeqbox/docker-images/master/info&label=Custom%20Kali%20Linux&query=$.Custom_Kali_Linux&colorB=blue)](https://github.com/qeeqbox/docker-images/blob/master/changes.md) [![Generic badge](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/qeeqbox/docker-images/master/info&label=Custom%20Parrot%20OS&query=$.Custom_Parrot_OS&colorB=blue)](https://github.com/qeeqbox/docker-images/blob/master/changes.md)
[![Generic badge](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/qeeqbox/docker-images/master/info&label=Android%20Tools&query=$.Android_Tools&colorB=blue)](https://github.com/qeeqbox/docker-images/blob/master/changes.md)

Custom security focused images accessible via VNC, RDP or web. The images were customized with a minimal GUI and different settings to support the remote access. 

## Kali
<img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/kali.png" style="max-width:768px"/>

## Parrot
<img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/parrot.png" style="max-width:768px"/>

## Android Tools
<img src="https://raw.githubusercontent.com/qeeqbox/docker-images/master/readme/android-tools.png" style="max-width:768px"/>

## Current builds
- Kali (qeeqbox/kali:1.0) 				              2GB 
- Parrot (qeeqbox/parrot:1.0) 			            5GB
- Android Tools (qeeqbox/android-tools:1.0)     1.7GB

## Running
#### Kali
```console 
docker run -it --cap-add=NET_ADMIN qeeqbox/kali:1.0
...
...
Successfully built 7c36ab06e878
Successfully tagged qeeqbox/kali:1.0

https://github.com/qeeqbox/docker-images

Custom Kali distro accessible via VNC, RDP or web browser

root pass -> EmBNjt^Zea
-----------------------
Username  -> xuser
Password  -> xTk#gV8ig*
VNC pass  -> fjw#8fAwVC

http://172.17.0.2:6080/index.html
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
- [kali](https://www.kali.org) 
- [Parrot OS](https://www.parrotsec.org/download/) 
- [BlackArch](https://blackarch.org/downloads.html/) 

## Resources
- https://docs.xfce.org/
- Please let me know if i missed a resource or dependency

## Licncess
- https://www.kali.org/EULA.txt
- https://hub.docker.com/u/kalilinux
- https://docs.parrotlinux.org/
- https://hub.docker.com/u/parrotsec
- https://github.com/BlackArch/blackarch/blob/master/COPYING
- https://developer.android.com/studio

## Disclaimer\Notes
- Do not deploy without proper configuration
- Setup some security group rules and remove default credentials
- Do not forget to visit Kali, Parrot OS and BlackArch websites for awesome resources or leaving feedback

## Other Projects
[![](https://github.com/qeeqbox/.github/blob/main/data/social-analyzer.png)](https://github.com/qeeqbox/social-analyzer) [![](https://github.com/qeeqbox/.github/blob/main/data/analyzer.png)](https://github.com/qeeqbox/analyzer) [![](https://github.com/qeeqbox/.github/blob/main/data/chameleon.png)](https://github.com/qeeqbox/chameleon) [![](https://github.com/qeeqbox/.github/blob/main/data/osint.png)](https://github.com/qeeqbox/osint) [![](https://github.com/qeeqbox/.github/blob/main/data/honeypots.png)](https://github.com/qeeqbox/honeypots) [![](https://github.com/qeeqbox/.github/blob/main/data/url-sandbox.png)](https://github.com/qeeqbox/url-sandbox) [![](https://github.com/qeeqbox/.github/blob/main/data/mitre-visualizer.png)](https://github.com/qeeqbox/mitre-visualizer) [![](https://github.com/qeeqbox/.github/blob/main/data/woodpecker.png)](https://github.com/qeeqbox/woodpecker) [![](https://github.com/qeeqbox/.github/blob/main/data/seahorse.png)](https://github.com/qeeqbox/seahorse) [![](https://github.com/qeeqbox/.github/blob/main/data/rhino.png)](https://github.com/qeeqbox/rhino) [![](https://github.com/qeeqbox/.github/blob/main/data/raven.png)](https://github.com/qeeqbox/raven)
