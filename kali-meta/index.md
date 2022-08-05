---
Title: kali-meta
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/kali-meta
Architectures: any all
Version: 2022.3.12
Metapackages: kali-linux-arm kali-linux-core kali-linux-default kali-linux-everything kali-linux-firmware kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-bluetooth kali-tools-crypto-stego kali-tools-database kali-tools-exploitation kali-tools-forensics kali-tools-fuzzing kali-tools-gpu kali-tools-hardware kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-reporting kali-tools-reverse-engineering kali-tools-rfid kali-tools-sdr kali-tools-sniffing-spoofing kali-tools-social-engineering kali-tools-top10 kali-tools-voip kali-tools-vulnerability kali-tools-web kali-tools-windows-resources kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### kali-desktop-core
 
  This metapackage depends on Kali packages that should be installed on all
  desktop installations of Kali Linux.
   
  This metapackage is a dependency of all kali-desktop-* packages.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-core`  
 
 {{< spoiler "Dependencies:" >}}
 * dbus-user-session
 * firefox-esr | firefox | www-browser
 * fonts-noto-color-emoji
 * haveged
 * kali-archive-keyring
 * kali-debtags
 * kali-defaults-desktop
 * kali-grant-root
 * kali-menu
 * kali-themes
 * xdg-utils
 * xserver-xorg-legacy
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-e17
 
  This metapackage installs a minimalistic
  Enlightenment E17 desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-e17`  
 
 {{< spoiler "Dependencies:" >}}
 * enlightenment
 * kali-desktop-base
 * kali-desktop-core
 * libeet-bin
 * lightdm
 * qt5ct
 * suckless-tools
 * terminology
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-gnome
 
  This metapackage installs a minimalistic GNOME desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-gnome`  
 
 {{< spoiler "Dependencies:" >}}
 * eog
 * evince
 * file-roller
 * gdm3
 * gedit
 * gir1.2-ayatanaappindicator3-0.1
 * gnome-calculator
 * gnome-control-center
 * gnome-menus
 * gnome-session
 * gnome-shell
 * gnome-shell-extension-appindicator
 * gnome-shell-extension-dashtodock
 * gnome-shell-extension-desktop-icons-ng
 * gnome-shell-extension-proxyswitcher
 * gnome-shell-extensions
 * gnome-system-monitor
 * gnome-terminal
 * gnome-tweaks
 * kali-desktop-core
 * nautilus
 * network-manager-gnome
 * qt5ct
 * totem
 * xdg-user-dirs-gtk
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-i3
 
  This metapackage installs a
  minimalistic I3 desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-i3`  
 
 {{< spoiler "Dependencies:" >}}
 * conky
 * i3
 * kali-desktop-base
 * kali-desktop-core
 * qt5ct
 * suckless-tools | dmenu
 * xorg
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-i3-gaps
 
  This metapackage installs a
  minimalistic I3-gaps desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-i3-gaps`  
 
 {{< spoiler "Dependencies:" >}}
 * betterlockscreen
 * conky
 * i3-gaps
 * i3-gaps-dotfiles
 * kali-desktop-base
 * kali-desktop-core
 * qt5ct
 * suckless-tools | dmenu
 * xorg
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-kde
 
  This metapackage installs a minimalistic KDE desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-kde`  
 
 {{< spoiler "Dependencies:" >}}
 * ark
 * gwenview
 * kali-desktop-core
 * kate
 * kcalc
 * kde-plasma-desktop
 * kde-spectacle
 * konsole
 * kwin-style-kali
 * okular
 * plasma-nm
 * plasma-systemmonitor
 * sddm
 * sddm-theme-breeze
 * vlc
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-live
 
  This metapackage depends on generic packages that should be installed on an
  official Kali live image.
   
  They provide features that are not directly related to penetration testing but
  that are intended to make the image more useful and usable for a wide set of
  users.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-live`  
 
 {{< spoiler "Dependencies:" >}}
 * alsa-tools
 * console-setup
 * cryptsetup-initramfs
 * locales-all
 * lvm2
 * onboard
 * zerofree
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-lxde
 
  This metapackage installs a minimalistic LXDE desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-lxde`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-desktop-base
 * kali-desktop-core
 * lxde
 * lxterminal
 * qt5ct
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-mate
 
  This metapackage installs a minimalistic MATE desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-mate`  
 
 {{< spoiler "Dependencies:" >}}
 * atril
 * engrampa
 * eom
 * kali-desktop-base
 * kali-desktop-core
 * lightdm
 * mate-calc
 * mate-desktop-environment
 * mate-system-monitor
 * mate-terminal
 * mate-utils
 * network-manager-gnome
 * parole
 * pluma
 * qt5ct
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-desktop-xfce
 
  This metapackage installs a minimalistic Xfce desktop on your Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-desktop-xfce`  
 
 {{< spoiler "Dependencies:" >}}
 * atril
 * engrampa
 * kali-desktop-core
 * lightdm
 * mate-calc
 * mousepad
 * network-manager-gnome
 * parole
 * policykit-1-gnome
 * qt5ct
 * qterminal
 * ristretto
 * thunar-archive-plugin
 * xcape
 * xdg-user-dirs-gtk
 * xfce4
 * xfce4-cpugraph-plugin
 * xfce4-genmon-plugin
 * xfce4-power-manager-plugins
 * xfce4-screenshooter
 * xfce4-taskmanager
 * xfce4-whiskermenu-plugin
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-arm
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on applications that are particularly interesting
  to run on ARM devices.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-arm`  
 
 {{< spoiler "Dependencies:" >}}
 * abootimg
 * aircrack-ng
 * cewl
 * cgpt
 * crunch
 * dnsrecon
 * ethtool
 * exploitdb
 * fake-hwclock
 * hydra
 * initramfs-tools
 * john
 * kali-linux-core
 * libnfc-bin
 * medusa
 * metasploit-framework
 * mfoc
 * ncrack
 * nmap
 * passing-the-hash
 * proxychains4
 * recon-ng
 * sqlmap
 * tcpdump
 * theharvester
 * tshark
 * u-boot-tools
 * usbutils
 * vboot-kernel-utils
 * vboot-utils
 * windows-binaries
 * winexe
 * wpscan
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-core
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the packages that are installed by default
  on any Kali system.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-core`  
 
 {{< spoiler "Dependencies:" >}}
 * ftp
 * kali-defaults
 * netcat-traditional
 * openssh-client
 * openssh-server
 * parted
 * sudo
 * tasksel
 * tcpdump
 * tmux
 * vim-tiny | vim | vim-nox
 * zsh
 * zsh-autosuggestions
 * zsh-syntax-highlighting
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-default
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the applications that are included in
  official Kali Linux images.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-default`  
 
 {{< spoiler "Dependencies:" >}}
 * autopsy
 * cherrytree
 * cutycapt
 * dirbuster
 * faraday
 * fern-wifi-cracker
 * gparted
 * guymager
 * hydra-gtk
 * kali-linux-headless
 * kali-tools-top10
 * king-phisher
 * legion
 * ophcrack
 * ophcrack-cli
 * rdesktop
 * recordmydesktop
 * sqlitebrowser
 * tightvncserver
 * xtightvncviewer
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-everything
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all other specific purpose metapackages and
  some more applications. Beware, this will install a lot of stuff!
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-everything`  
 
 {{< spoiler "Dependencies:" >}}
 * airgeddon
 * altdns
 * android-sdk
 * apple-bleee
 * arjun
 * assetfinder
 * b374k
 * berate-ap
 * bettercap-ui
 * bing-ip2hosts
 * bloodhound
 * bruteforce-salted-openssl
 * bruteforce-wallet
 * bruteshark
 * brutespray
 * capstone-tool
 * certgraph
 * changeme
 * chaosreader
 * chisel
 * cloud-enum
 * cloudbrute
 * cmseek
 * cntlm
 * crack
 * crowbar
 * cupid-hostapd
 * cupid-wpasupplicant
 * de4dot
 * defectdojo
 * dirsearch
 * dislocker
 * dnscat2
 * dnsgen
 * dnstwist
 * dnsx
 * dscan
 * dufflebag
 * dumpsterdiver
 * dwarf2json
 * eaphammer
 * email2phonenumber
 * emailharvester
 * evil-ssdp
 * exploitdb-bin-sploits
 * exploitdb-papers
 * faraday-cli
 * feroxbuster
 * finalrecon
 * freeradius
 * gdb-peda
 * getallurls
 * gitleaks
 * godoh
 * golang-github-binject-go-donut
 * goldeneye
 * goofile
 * gospider
 * gtkhash
 * hashrat
 * hb-honeypot
 * hcxtools
 * hostapd-mana
 * hosthunter
 * hostsman
 * htshells
 * httprobe
 * httpx-toolkit
 * hurl
 * ibombshell
 * ident-user-enum
 * inspy
 * instaloader
 * ipv6-toolkit
 * ismtp
 * ivre
 * joplin
 * jsp-file-browser
 * kali-community-wallpapers
 * kali-legacy-wallpapers
 * kali-linux-arm
 * kali-linux-core
 * kali-linux-default
 * kali-linux-headless
 * kali-linux-large
 * kali-tools-802-11
 * kali-tools-bluetooth
 * kali-tools-crypto-stego
 * kali-tools-database
 * kali-tools-exploitation
 * kali-tools-forensics
 * kali-tools-fuzzing
 * kali-tools-gpu
 * kali-tools-hardware
 * kali-tools-information-gathering
 * kali-tools-passwords
 * kali-tools-post-exploitation
 * kali-tools-reporting
 * kali-tools-reverse-engineering
 * kali-tools-rfid
 * kali-tools-sdr
 * kali-tools-sniffing-spoofing
 * kali-tools-social-engineering
 * kali-tools-top10
 * kali-tools-voip
 * kali-tools-vulnerability
 * kali-tools-web
 * kali-tools-windows-resources
 * kali-tools-wireless
 * kerberoast
 * knocker
 * koadic
 * lapsdumper
 * linux-exploit-suggester
 * maltego-teeth
 * maryam
 * massdns
 * merlin-agent
 * merlin-server
 * multiforcer
 * naabu
 * name-that-hash
 * nbtscan-unixwiz
 * nextnet
 * nmapsi4
 * nuclei
 * o-saft
 * odat
 * osrframework
 * owl
 * pacu
 * parsero
 * payloadsallthethings
 * peirates
 * phishery
 * photon
 * phpggc
 * phpsploit
 * pnscan
 * pocsuite3
 * pompem
 * poshc2
 * princeprocessor
 * prism
 * proxify
 * proxmark3
 * pskracker
 * pwncat
 * quark-engine
 * redsnarf
 * rev-proxy-grapher
 * ridenum
 * robotstxt
 * ropper
 * routerkeygenpc
 * routersploit
 * ruby-pedump
 * s3scanner
 * sentrypeer
 * shed
 * shellfire
 * sherlock
 * silenttrinity
 * sliver
 * snmpenum
 * snowdrop
 * sparrow-wifi
 * spray
 * sprayingtoolkit
 * spraykatz
 * sslstrip
 * stegcracker
 * subfinder
 * subjack
 * sublist3r
 * teamsploit
 * testssl.sh
 * trufflehog
 * tundeep
 * unhide.rb
 * websploit
 * wgetpaste
 * whatmask
 * wifiphisher
 * wifipumpkin3
 * wig
 * wig-ng
 * witnessme
 * wmi-client
 * wordlistraider
 * wotmate
 * wpa-sycophant
 * zonedb
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-firmware
 
  This metapackage depends on a curated list of firmware packages that
  should be installed by default for better hardware support in Kali Linux.
   
  Some firmware packages are excluded. Many reasons can explain those
  exclusions: they are too big, they are only useful for uncommon hardware, they
  require click-through licenses, they are for hardware that is not really
  relevant in the context of Kali, etc.
 
 **Installed size:** `24 KB`  
 **How to install:** `sudo apt install kali-linux-firmware`  
 
 {{< spoiler "Dependencies:" >}}
 * bluez-firmware
 * firmware-amd-graphics
 * firmware-atheros
 * firmware-brcm80211
 * firmware-intel-sound
 * firmware-iwlwifi
 * firmware-libertas
 * firmware-linux
 * firmware-misc-nonfree
 * firmware-realtek
 * firmware-sof-signed
 * firmware-ti-connectivity
 * firmware-zd1211
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-headless
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the applications that are included in
  official Kali Linux images and that don't require X11/GUI.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-headless`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * amass
 * apache2
 * arp-scan
 * arping | iputils-arping
 * atftpd
 * axel
 * bind9-dnsutils
 * binwalk
 * bluez
 * bluez-hcidump
 * bulk-extractor
 * bully
 * cadaver
 * cewl
 * chntpw
 * cifs-utils
 * clang
 * commix
 * crackmapexec
 * creddump7
 * crunch
 * cryptcat
 * cryptsetup
 * cryptsetup-initramfs
 * cryptsetup-nuke-password
 * curlftpfs
 * davtest
 * dbd
 * default-mysql-server
 * dirb
 * dmitry
 * dns2tcp
 * dnschef
 * dnsenum
 * dnsrecon
 * dos2unix
 * enum4linux
 * ethtool
 * evil-winrm
 * exe2hexbat
 * exiv2
 * expect
 * exploitdb
 * ffuf
 * fierce
 * fping
 * gdisk
 * git
 * gpp-decrypt
 * hash-identifier
 * hashcat
 * hashcat-utils
 * hashdeep
 * hashid
 * hotpatch
 * hping3
 * hydra
 * i2c-tools
 * ifenslave
 * ike-scan
 * impacket-scripts
 * inetsim
 * iodine
 * iw
 * john
 * kali-linux-core
 * kismet
 * laudanum
 * lbd
 * libimage-exiftool-perl
 * macchanger
 * magicrescue
 * maskprocessor
 * masscan
 * metasploit-framework
 * mimikatz
 * minicom
 * miredo
 * mitmproxy
 * msfpc
 * multimac
 * nasm
 * nbtscan
 * ncrack
 * ncurses-hexedit
 * netdiscover
 * netmask
 * netsed
 * netsniff-ng
 * nfs-common
 * ngrep
 * nikto
 * nmap
 * onesixtyone
 * openvpn
 * p7zip-full
 * passing-the-hash
 * patator
 * pdf-parser
 * pdfid
 * php
 * php-mysql
 * pipal
 * pixiewps
 * plocate | mlocate
 * powershell
 * powershell-empire
 * powersploit
 * proxychains4
 * proxytunnel
 * ptunnel
 * pwnat
 * python-is-python3
 * python3-impacket
 * python3-pip
 * python3-scapy
 * python3-virtualenv
 * qsslcaudit
 * radare2
 * rake
 * reaver
 * rebind
 * recon-ng
 * redsocks
 * responder
 * rfkill
 * rsmangler
 * sakis3g
 * samba
 * samdump2
 * sbd
 * scalpel
 * screen
 * scrounge-ntfs
 * sendemail
 * set
 * skipfish
 * sleuthkit
 * smbmap
 * snmp
 * snmpcheck
 * snmpd
 * socat
 * spiderfoot
 * spike
 * spooftooph
 * sqlmap
 * ssldump
 * sslh
 * sslscan
 * sslsplit
 * sslyze
 * statsprocessor
 * stunnel4
 * swaks
 * tcpick
 * tcpreplay
 * telnet
 * testdisk
 * tftp
 * thc-ipv6
 * thc-pptp-bruter
 * theharvester
 * traceroute
 * udptunnel
 * unix-privesc-check
 * unrar | unar
 * upx-ucl
 * vboot-kernel-utils
 * vboot-utils
 * vim | vim-nox
 * vlan
 * voiphopper
 * vpnc
 * wafw00f
 * wce
 * webshells
 * weevely
 * wfuzz
 * whatweb
 * whois
 * wifite
 * windows-binaries
 * winexe
 * wordlists
 * wpscan
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-labs
 
  These applications are meant to be insecure & vulnerable to help users
  experiment in a controlled manner.
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the packages containing vulnerable environments
  for safe testing.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-labs`  
 
 {{< spoiler "Dependencies:" >}}
 * dvwa
 * juice-shop
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-large
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage installs the applications which are included by default in
  official Kali Linux images and adds many more on top of those.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-large`  
 
 {{< spoiler "Dependencies:" >}}
 * 0trace
 * afflib-tools
 * amap
 * apache-users
 * apktool
 * armitage
 * arpwatch
 * asleap
 * backdoor-factory
 * bed
 * beef-xss
 * bluelog
 * blueranger
 * bluesnarfer
 * braa
 * btscanner
 * bytecode-viewer
 * cabextract
 * caldera
 * cgpt
 * chirp
 * chkrootkit
 * cisco-auditing-tool
 * cisco-global-exploiter
 * cisco-ocs
 * cisco-torch
 * cloud-enum
 * cmospwd
 * code-oss | code
 * copy-router-config
 * cowpatty
 * cymothoa
 * darkstat
 * dbeaver
 * dc3dd
 * dcfldd
 * ddrescue
 * dex2jar
 * dhcpig
 * dnsmap
 * dnstracer
 * dnswalk
 * doona
 * dotdotpwn
 * dradis
 * driftnet
 * dsniff
 * dumpzilla
 * eapmd5pass
 * edb-debugger
 * enumiax
 * ettercap-graphical | ettercap-text-only
 * ewf-tools
 * extundelete
 * fcrackzip
 * fiked
 * foremost
 * fragrouter
 * framework2
 * ftester
 * galleta
 * gdb
 * ghidra
 * gobuster
 * hackrf
 * hamster-sidejack
 * hexinject
 * httrack
 * iaxflood
 * intrace
 * inviteflood
 * irpas
 * jadx
 * javasnoop
 * jboss-autopwn
 * johnny
 * joomscan
 * jsql-injection
 * kali-linux-core
 * kali-linux-default
 * kismet-logtools
 * libfindrtp
 * libfreefare-bin
 * libhivex-bin
 * libnfc-bin
 * lynis
 * maltego
 * mc
 * mdbtools
 * mdk3
 * medusa
 * memdump
 * mercurial
 * mfcuk
 * mfoc
 * mfterm
 * missidentify
 * ncat-w32
 * netwag
 * nipper-ng
 * nishang
 * ohrwurm
 * ollydbg
 * oscanner
 * p0f
 * pack
 * padbuster
 * paros
 * pasco
 * perl-cisco-copyconfig
 * pev
 * photon
 * plecost
 * polenum
 * protos-sip
 * pst-utils
 * rainbowcrack
 * rcracki-mt
 * recoverjpeg
 * redfang
 * reglookup
 * regripper
 * rifiuti
 * rifiuti2
 * rtpbreak
 * rtpflood
 * rtpinsertsound
 * rtpmixsound
 * safecopy
 * sctpscan
 * seclists
 * sfuzz
 * sidguesser
 * siege
 * siparmyknife
 * sipcrack
 * sipp
 * sipvicious
 * smali
 * smtp-user-enum
 * sniffjoke
 * spectools
 * sqldict
 * sqlninja
 * sqlsus
 * sslsniff
 * starkiller
 * subversion
 * sucrack
 * t50
 * tcpflow
 * termineter
 * tftpd32
 * thc-ssl-dos
 * tlssled
 * tnscmd10g
 * truecrack
 * twofi
 * unicornscan
 * uniscan
 * urlcrazy
 * vim-gtk3
 * vinetto
 * wapiti
 * webacoo
 * webscarab
 * wifi-honey
 * xprobe
 * xspy
 * xsser
 * yersinia
 * zaproxy
 * zerofree
 * zim
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-linux-nethunter
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the applications that a Kali Linux
  NetHunter system should have installed.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-linux-nethunter`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * apache2
 * armitage
 * autoconf
 * autossh
 * backdoor-factory
 * beef-xss
 * bettercap
 * bind9-dnsutils
 * binutils-arm-none-eabi
 * burpsuite
 * dbd
 * device-pharmer
 * dnsmasq
 * dsniff
 * ettercap-text-only | ettercap-graphical
 * exe2hexbat
 * exploitdb
 * florence
 * g++
 * gcc
 * gcc-arm-none-eabi
 * gpsd
 * hostapd
 * isc-dhcp-server
 * iw
 * kali-defaults
 * kali-desktop-xfce
 * kali-linux-core
 * kismet
 * kismet-plugins
 * libapache2-mod-php
 * libbz2-dev
 * libffi-dev
 * libncurses5-dev
 * libnewlib-arm-none-eabi
 * libreadline6-dev
 * libssl-dev
 * libtool
 * libxml2-dev
 * macchanger
 * make
 * mdk3
 * metasploit-framework
 * mfoc
 * mitmproxy
 * msfpc
 * nethunter-utils
 * nishang
 * nmap
 * openssh-server
 * openvpn
 * p0f
 * php
 * pixiewps
 * postgresql
 * ptunnel
 * python3-dnspython
 * python3-lxml
 * python3-m2crypto
 * python3-mako
 * python3-netaddr
 * python3-pcapy
 * python3-pip
 * python3-setuptools
 * python3-twisted
 * recon-ng
 * rfkill
 * socat
 * sox
 * sqlmap
 * sslsplit
 * tcpdump
 * tcptrace
 * tigervnc-standalone-server
 * tinyproxy
 * tshark
 * wifite
 * wipe
 * wireshark
 * wpasupplicant
 * zip
 * zlib1g-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-802-11
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the 802.11 attack tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-802-11`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * airgeddon
 * asleap
 * bully
 * cowpatty
 * eapmd5pass
 * fern-wifi-cracker
 * freeradius-wpe
 * hashcat
 * hostapd-wpe
 * iw
 * kismet
 * macchanger
 * mdk3
 * mdk4
 * pixiewps
 * reaver
 * wifi-honey
 * wifite
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-bluetooth
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the bluetooth attack tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-bluetooth`  
 
 {{< spoiler "Dependencies:" >}}
 * bluelog
 * blueranger
 * bluesnarfer
 * bluez
 * bluez-hcidump
 * btscanner
 * crackle
 * redfang
 * spooftooph
 * ubertooth
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-crypto-stego
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the Cryptography and Steganography tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-crypto-stego`  
 
 {{< spoiler "Dependencies:" >}}
 * aesfix
 * aeskeyfind
 * ccrypt
 * outguess
 * steghide
 * stegsnow
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-database
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the database assessment tools that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-database`  
 
 {{< spoiler "Dependencies:" >}}
 * jsql-injection
 * mdbtools
 * oscanner
 * sidguesser
 * sqldict
 * sqlitebrowser
 * sqlmap
 * sqlninja
 * sqlsus
 * tnscmd10g
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-exploitation
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the exploitation tools that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-exploitation`  
 
 {{< spoiler "Dependencies:" >}}
 * armitage
 * beef-xss
 * exploitdb
 * metasploit-framework
 * msfpc
 * set
 * shellnoob
 * sqlmap
 * termineter
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-forensics
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the forensic tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-forensics`  
 
 {{< spoiler "Dependencies:" >}}
 * afflib-tools
 * apktool
 * autopsy
 * binwalk
 * bulk-extractor
 * bytecode-viewer
 * cabextract
 * chkrootkit
 * creddump7
 * dc3dd
 * dcfldd
 * ddrescue
 * dumpzilla
 * edb-debugger
 * ewf-tools
 * exifprobe
 * exiv2
 * ext3grep
 * ext4magic
 * extundelete
 * fcrackzip
 * firmware-mod-kit
 * foremost
 * forensic-artifacts
 * forensics-colorize
 * galleta
 * gdb
 * gpart
 * gparted
 * grokevt
 * guymager
 * hashdeep
 * inetsim
 * jadx
 * javasnoop
 * libhivex-bin
 * lime-forensics
 * lvm2
 * lynis
 * mac-robber
 * magicrescue
 * md5deep
 * mdbtools
 * memdump
 * metacam
 * missidentify
 * myrescue
 * nasm
 * nasty
 * ollydbg
 * p7zip-full
 * parted
 * pasco
 * pdf-parser
 * pdfid
 * pev
 * plaso
 * polenum
 * pst-utils
 * python3-capstone
 * python3-dfdatetime
 * python3-dfvfs
 * python3-dfwinreg
 * python3-distorm3
 * radare2
 * radare2-cutter
 * recoverdm
 * recoverjpeg
 * reglookup
 * regripper
 * rephrase
 * rifiuti
 * rifiuti2
 * rkhunter
 * rsakeyfind
 * safecopy
 * samdump2
 * scalpel
 * scrounge-ntfs
 * sleuthkit
 * smali
 * sqlitebrowser
 * ssdeep
 * tcpdump
 * tcpflow
 * tcpick
 * tcpreplay
 * truecrack
 * undbx
 * unhide
 * unrar | unar
 * upx-ucl
 * vinetto
 * wce
 * winregfs
 * wireshark
 * xmount
 * xplico
 * yara
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-fuzzing
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the fuzzing attack tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-fuzzing`  
 
 {{< spoiler "Dependencies:" >}}
 * afl++
 * sfuzz
 * spike
 * wfuzz
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-gpu
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the GPU tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-gpu`  
 
 {{< spoiler "Dependencies:" >}}
 * oclgausscrack
 * truecrack
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-hardware
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the hardware attack tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-hardware`  
 
 {{< spoiler "Dependencies:" >}}
 * binwalk
 * cutecom
 * flashrom
 * minicom
 * openocd
 * qemu-system-x86
 * qemu-user
 * radare2
 * radare2-cutter
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-information-gathering
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the Information Gathering tools that
  Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-information-gathering`  
 
 {{< spoiler "Dependencies:" >}}
 * 0trace
 * arping | iputils-arping
 * braa
 * dmitry
 * dnsenum
 * dnsmap
 * dnsrecon
 * dnstracer
 * dnswalk
 * enum4linux
 * fierce
 * firewalk
 * fping
 * fragrouter
 * ftester
 * hping3
 * ike-scan
 * intrace
 * irpas
 * lbd
 * legion
 * maltego
 * masscan
 * metagoofil
 * nbtscan
 * ncat
 * netdiscover
 * netmask
 * nmap
 * onesixtyone
 * p0f
 * qsslcaudit
 * recon-ng
 * smbmap
 * smtp-user-enum
 * snmpcheck
 * ssldump
 * sslh
 * sslscan
 * sslyze
 * swaks
 * thc-ipv6
 * theharvester
 * tlssled
 * twofi
 * unicornscan
 * urlcrazy
 * wafw00f
 * xprobe
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-passwords
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the password cracking tools that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-passwords`  
 
 {{< spoiler "Dependencies:" >}}
 * cewl
 * chntpw
 * cisco-auditing-tool
 * cmospwd
 * crackle
 * creddump7
 * crunch
 * fcrackzip
 * freerdp2-x11
 * gpp-decrypt
 * hash-identifier
 * hashcat
 * hashcat-utils
 * hashid
 * hydra
 * hydra-gtk
 * john
 * johnny
 * kali-tools-gpu
 * maskprocessor
 * medusa
 * mimikatz
 * ncrack
 * onesixtyone
 * ophcrack
 * ophcrack-cli
 * pack
 * passing-the-hash
 * patator
 * pdfcrack
 * pipal
 * polenum
 * rainbowcrack
 * rarcrack
 * rcracki-mt
 * rsmangler
 * samdump2
 * seclists
 * sipcrack
 * sipvicious
 * smbmap
 * sqldict
 * statsprocessor
 * sucrack
 * thc-pptp-bruter
 * truecrack
 * twofi
 * wordlists
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-post-exploitation
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the post exploitation tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-post-exploitation`  
 
 {{< spoiler "Dependencies:" >}}
 * backdoor-factory
 * cymothoa
 * dbd
 * dns2tcp
 * exe2hexbat
 * iodine
 * laudanum
 * mimikatz
 * miredo
 * nishang
 * powersploit
 * proxychains4
 * proxytunnel
 * ptunnel
 * pwnat
 * sbd
 * shellter
 * sslh
 * stunnel4
 * udptunnel
 * veil
 * webacoo
 * weevely
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-reporting
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the reporting tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-reporting`  
 
 {{< spoiler "Dependencies:" >}}
 * cutycapt
 * dradis
 * eyewitness
 * faraday
 * maltego
 * metagoofil
 * pipal
 * recordmydesktop
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-reverse-engineering
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the reverse engineering tools that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-reverse-engineering`  
 
 {{< spoiler "Dependencies:" >}}
 * apktool
 * bytecode-viewer
 * clang
 * dex2jar
 * edb-debugger
 * jadx
 * javasnoop
 * jd-gui
 * metasploit-framework
 * ollydbg
 * radare2
 * radare2-cutter
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-rfid
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the RFID tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-rfid`  
 
 {{< spoiler "Dependencies:" >}}
 * gnuradio
 * libfreefare-bin
 * libnfc-bin
 * mfcuk
 * mfoc
 * mfterm
 * proxmark3
 * rfdump
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-sdr
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the SDR tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-sdr`  
 
 {{< spoiler "Dependencies:" >}}
 * chirp
 * gnuradio
 * gqrx-sdr
 * gr-air-modes
 * gr-iqbal
 * gr-osmosdr
 * hackrf
 * inspectrum
 * kalibrate-rtl
 * multimon-ng
 * rtlsdr-scanner
 * uhd-host
 * uhd-images
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-sniffing-spoofing
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the sniffing & spoofing tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-sniffing-spoofing`  
 
 {{< spoiler "Dependencies:" >}}
 * bettercap
 * darkstat
 * dnschef
 * driftnet
 * dsniff
 * ettercap-graphical | ettercap-text-only
 * fiked
 * hamster-sidejack
 * hexinject
 * isr-evilgrade
 * macchanger
 * mitmproxy
 * netsniff-ng
 * rebind
 * responder
 * sniffjoke
 * sslsniff
 * sslsplit
 * tcpflow
 * tcpreplay
 * wifi-honey
 * wireshark
 * yersinia
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-social-engineering
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the social engineering tools
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-social-engineering`  
 
 {{< spoiler "Dependencies:" >}}
 * backdoor-factory
 * beef-xss
 * maltego
 * msfpc
 * set
 * veil
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-top10
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on the 10 most important applications that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-top10`  
 
 {{< spoiler "Dependencies:" >}}
 * aircrack-ng
 * burpsuite
 * crackmapexec
 * hydra
 * john
 * metasploit-framework
 * nmap
 * responder
 * sqlmap
 * wireshark
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-voip
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the VoIP tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-voip`  
 
 {{< spoiler "Dependencies:" >}}
 * enumiax
 * iaxflood
 * inviteflood
 * libfindrtp
 * nmap
 * ohrwurm
 * protos-sip
 * rtpbreak
 * rtpflood
 * rtpinsertsound
 * rtpmixsound
 * sctpscan
 * siparmyknife
 * sipcrack
 * sipp
 * sipvicious
 * voiphopper
 * wireshark
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-vulnerability
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the Vulnerability Analysis tools that
  Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-vulnerability`  
 
 {{< spoiler "Dependencies:" >}}
 * afl++
 * bed
 * cisco-auditing-tool
 * cisco-global-exploiter
 * cisco-ocs
 * cisco-torch
 * copy-router-config
 * dhcpig
 * enumiax
 * gvm
 * iaxflood
 * inviteflood
 * legion
 * lynis
 * nikto
 * nmap
 * ohrwurm
 * peass
 * protos-sip
 * rtpbreak
 * rtpflood
 * rtpinsertsound
 * rtpmixsound
 * sctpscan
 * sfuzz
 * siege
 * siparmyknife
 * sipp
 * sipsak
 * sipvicious
 * slowhttptest
 * spike
 * t50
 * thc-ssl-dos
 * unix-privesc-check
 * voiphopper
 * yersinia
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-web
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the webapp assessment tools that Kali Linux
  provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-web`  
 
 {{< spoiler "Dependencies:" >}}
 * apache-users
 * apache2
 * beef-xss
 * burpsuite
 * cadaver
 * commix
 * cutycapt
 * davtest
 * default-mysql-server
 * dirb
 * dirbuster
 * dotdotpwn
 * eyewitness
 * ftester
 * hakrawler
 * hamster-sidejack
 * heartleech
 * httprint
 * httrack
 * hydra
 * hydra-gtk
 * jboss-autopwn
 * joomscan
 * jsql-injection
 * laudanum
 * lbd
 * maltego
 * medusa
 * mitmproxy
 * ncrack
 * nikto
 * nishang
 * nmap
 * oscanner
 * owasp-mantra-ff
 * padbuster
 * paros
 * patator
 * php
 * php-mysql
 * plecost
 * proxychains4
 * proxytunnel
 * qsslcaudit
 * redsocks
 * sidguesser
 * siege
 * skipfish
 * slowhttptest
 * sqldict
 * sqlitebrowser
 * sqlmap
 * sqlninja
 * sqlsus
 * ssldump
 * sslh
 * sslscan
 * sslsniff
 * sslsplit
 * sslyze
 * stunnel4
 * thc-ssl-dos
 * tlssled
 * tnscmd10g
 * uniscan
 * wafw00f
 * wapiti
 * watobo
 * webacoo
 * webscarab
 * webshells
 * weevely
 * wfuzz
 * whatweb
 * wireshark
 * wpscan
 * xsser
 * zaproxy
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-windows-resources
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the Windows resources
  that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-windows-resources`  
 
 {{< spoiler "Dependencies:" >}}
 * dbd
 * dnschef
 * heartleech
 * hyperion
 * mimikatz
 * ncat-w32
 * ollydbg
 * powercat
 * regripper
 * sbd
 * secure-socket-funneling-windows-binaries
 * shellter
 * tftpd32
 * wce
 * windows-binaries
 * windows-privesc-check
 {{< /spoiler >}}
 
 
 - - -
 
 ### kali-tools-wireless
 
  This is Kali Linux, the most advanced penetration testing and security
  auditing distribution.
   
  This metapackage depends on all the wireless tools that Kali Linux provides.
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install kali-tools-wireless`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-tools-802-11
 * kali-tools-bluetooth
 * kali-tools-rfid
 * kali-tools-sdr
 * rfcat
 * rfkill
 * sakis3g
 * spectools
 * wireshark
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
