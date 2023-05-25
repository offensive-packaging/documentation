---
Title: crackmapexec
Homepage: https://github.com/byt3bl33d3r/CrackMapExec
Repository: https://gitlab.com/kalilinux/packages/crackmapexec
Architectures: all
Version: 5.4.0-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-top10 
Icon: images/crackmapexec-logo.svg
PackagesInfo: |
 ### crackmapexec
 
  This package is a swiss army knife for pentesting Windows/Active Directory
  environments.
   
  From enumerating logged on users and spidering SMB shares to executing psexec
  style attacks, auto-injecting Mimikatz/Shellcode/DLL's into memory using
  Powershell, dumping the NTDS.dit and more.
   
  The biggest improvements over the above tools are:
   - Pure Python script, no external tools required
   - Fully concurrent threading
   - Uses **ONLY** native WinAPI calls for discovering sessions, users, dumping
     SAM hashes etc...
   - Opsec safe (no binaries are uploaded to dump clear-text credentials, inject
     shellcode etc...)
   
  Additionally, a database is used to store used/dumped credentals. It also
  automatically correlates Admin credentials to hosts and vice-versa allowing you
  to easily keep track of credential sets and gain additional situational
  awareness in large environments.
 
 **Installed size:** `2.30 MB`  
 **How to install:** `sudo apt install crackmapexec`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aardwolf
 * python3-aioconsole
 * python3-bs4 
 * python3-dsinternals
 * python3-impacket
 * python3-lsassy
 * python3-masky
 * python3-msgpack
 * python3-neo4j
 * python3-paramiko
 * python3-pylnk3
 * python3-pypsrp
 * python3-pywerview
 * python3-requests
 * python3-termcolor
 * python3-terminaltables
 * python3-unicrypto
 * python3-xmltodict
 {{< /spoiler >}}
 
 ##### cmedb
 
 
 ```
 root@kali:~# cmedb -h
 cmedb (default)(smb) > 
 ```
 
 - - -
 
 ##### crackmapexec
 
 
 ```
 root@kali:~# crackmapexec -h
 usage: crackmapexec [-h] [-t THREADS] [--timeout TIMEOUT] [--jitter INTERVAL]
                     [--darrell] [--verbose]
                     {mssql,winrm,ldap,ssh,smb,rdp,ftp} ...
 
       ______ .______           ___        ______  __  ___ .___  ___.      ___      .______    _______ ___   ___  _______   ______
      /      ||   _  \         /   \      /      ||  |/  / |   \/   |     /   \     |   _  \  |   ____|\  \ /  / |   ____| /      |
     |  ,----'|  |_)  |       /  ^  \    |  ,----'|  '  /  |  \  /  |    /  ^  \    |  |_)  | |  |__    \  V  /  |  |__   |  ,----'
     |  |     |      /       /  /_\  \   |  |     |    <   |  |\/|  |   /  /_\  \   |   ___/  |   __|    >   <   |   __|  |  |
     |  `----.|  |\  \----. /  _____  \  |  `----.|  .  \  |  |  |  |  /  _____  \  |  |      |  |____  /  .  \  |  |____ |  `----.
      \______|| _| `._____|/__/     \__\  \______||__|\__\ |__|  |__| /__/     \__\ | _|      |_______|/__/ \__\ |_______| \______|
 
                                                 A swiss army knife for pentesting networks
                                     Forged by @byt3bl33d3r and @mpgn_x64 using the powah of dank memes
 
                                            Exclusive release for Porchetta Industries users
                                                        https://porchetta.industries/
 
                                                    Version : 5.4.0
                                                    Codename: Indestructible G0thm0g
 
 options:
   -h, --help            show this help message and exit
   -t THREADS            set how many concurrent threads to use (default: 100)
   --timeout TIMEOUT     max timeout in seconds of each thread (default: None)
   --jitter INTERVAL     sets a random delay between each connection (default: None)
   --darrell             give Darrell a hand
   --verbose             enable verbose output
 
 protocols:
   available protocols
 
   {mssql,winrm,ldap,ssh,smb,rdp,ftp}
     mssql               own stuff using MSSQL
     winrm               own stuff using WINRM
     ldap                own stuff using LDAP
     ssh                 own stuff using SSH
     smb                 own stuff using SMB
     rdp                 own stuff using RDP
     ftp                 own stuff using FTP
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
