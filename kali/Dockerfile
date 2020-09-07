FROM kalilinux/kali-rolling

MAINTAINER qeeqbox

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y aircrack-ng amap amass apt-utils arping arp-scan axel bash-completion binwalk bsdmainutils bulk-extractor cewl commix crackmapexec creddump7 crunch cryptcat curl dirb dirbuster dmitry dnschef dnsenum dnsrecon dnsutils dos2unix enum4linux ethtool exiv2 expect exploitdb fierce fping ftp gcc git gobuster golang hashcat hashdeep hashid hash-identifier hotpatch hping3 hydra iputils-ping john joomscan kpcli lbd libffi-dev magicrescue make man-db masscan metasploit-framework mimikatz mlocate nasm nbtscan ncat ncrack netcat netcat-traditional netmask netsniff-ng net-tools ngrep nikto nmap nodejs npm onesixtyone oscanner passing-the-hash patator php powershell powersploit proxychains proxychains4 ptunnel pwnat python2 python3 python3-pip python3-setuptools python-dev python-setuptools rebind recon-ng responder ruby-dev samba samdump2 seclists set sipvicious skipfish sleuthkit smbclient smbmap smtp-user-enum snmp snmpcheck socat spike sqlmap ssh-audit sslscan sslsplit sslyze statsprocessor stunnel4 swaks tcpdump tcpick tcpreplay testssl.sh theharvester tnscmd10g tor udptunnel uniscan unix-privesc-check upx-ucl vim voiphopper wafw00f webshells weevely wfuzz wget whatweb whois windows-binaries winexe wordlists wpscan yersinia firefox-esr gosu armitage

RUN apt-get update && \
    apt-get install -y --no-install-recommends evince file-roller gnome-themes-standard gpicview gtk2-engines-pixbuf ttf-ubuntu-font-family xfce4 xfce4-whiskermenu-plugin xorg xserver-xorg xfce4-indicator-plugin xfce4-terminal numix-icon-theme numix-icon-theme-circle

RUN apt-get install -y xrdp locales supervisor sudo ibus ibus-mozc dbus dbus-x11

RUN locale-gen en_US && \
    apt-get install -y git tigervnc-standalone-server && \
    git clone https://github.com/novnc/noVNC.git /root/noVNC && \
    git clone https://github.com/novnc/websockify.git /root/noVNC/utils/websockify

RUN mkdir -p /var/run/dbus 

RUN sed -i -e 's/LogLevel=DEBUG/LogLevel=CORE/g' /etc/xrdp/xrdp.ini && \
    sed -i -e 's/SyslogLevel=DEBUG/SyslogLevel=CORE/g' /etc/xrdp/xrdp.ini && \
    sed -i -e 's/EnableSyslog=true/EnableSyslog=false/g' /etc/xrdp/xrdp.ini && \
    sed -i -e 's/LogLevel=DEBUG/LogLevel=CORE/g' /etc/xrdp/sesman.ini && \
    sed -i -e 's/SyslogLevel=DEBUG/SyslogLevel=CORE/g' /etc/xrdp/sesman.ini && \
    sed -i -e 's/EnableSyslog=true/EnableSyslog=false/g' /etc/xrdp/sesman.ini

RUN useradd -m -s /bin/bash -G sudo xuser

COPY Adwaita-dark-Xfce-with-Qbox-mw4 /usr/share/themes/Adwaita-dark-Xfce-with-Qbox-mw4
COPY xfce-perchannel-xml /etc/xdg/xfce4/xfconf/xfce-perchannel-xml
COPY xfce-perchannel-xml /home/xuser/.config/xfce4/xfconf/xfce-perchannel-xml
COPY helpers.rc /etc/xdg/xfce4/helpers.rc

RUN ln -s /root/noVNC/vnc_lite.html /root/noVNC/index.html && \
    ln -s /usr/share/icons/Numix-Circle /usr/share/icons/KXicons && \ 
    chown -R xuser /usr/share/themes/Adwaita-dark-Xfce-with-Qbox-mw4 && \
    chown -R xuser /usr/share/icons/KXicons && \
    chown -R xuser /etc/xdg/xfce4/xfconf/xfce-perchannel-xml

RUN echo "xfce4-session" > /etc/skel/.xsession
    
RUN apt-get install -y xfce4-taskmanager mousepad wget

RUN wget https://www.kali.org/wp-content/uploads/2014/06/kali-wp-june-2014_1920x1080_C.png -O /usr/share/backgrounds/xfce/default.jpg

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY entrypoint.sh .
RUN chmod +x entrypoint.sh
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
ENTRYPOINT ["./entrypoint.sh"]
