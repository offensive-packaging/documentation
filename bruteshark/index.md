---
Title: bruteshark
Homepage: https://github.com/odedshimon/BruteShark
Repository: https://gitlab.com/kalilinux/packages/bruteshark
Architectures: amd64
Version: 1.2.5-0kali7
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bruteshark
 
  This package contains a Network Forensic Analysis Tool (NFAT) that performs
  deep processing and inspection of network traffic (mainly PCAP files, but it
  also capable of directly live capturing from a network interface). It
  includes: password extracting, building a network map, reconstruct TCP
  sessions, extract hashes of encrypted passwords and even convert them to a
  Hashcat format in order to perform an offline Brute Force attack.
   
  The main goal of the project is to provide solution to security researchers
  and network administrators with the task of network traffic analysis while
  they try to identify weaknesses that can be used by a potential attacker to
  gain access to critical points on the network.
   
  On Linux it is a Command Line Interface tool.
 
 **Installed size:** `93.29 MB`  
 **How to install:** `sudo apt install bruteshark`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6
 * libgcc1
 * libgssapi-krb5-2
 * libpcap0.8
 * libstdc++6
 * zlib1g
 {{< /spoiler >}}
 
 ##### brutesharkcli
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
