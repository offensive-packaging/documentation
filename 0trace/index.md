---
Title: 0trace
Homepage: https://lcamtuf.coredump.cx
Repository: https://gitlab.com/kalilinux/packages/0trace
Architectures: any
Version: 0.01-3kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: images/0trace-logo.svg
PackagesInfo: |
 ### 0trace
 
  The package is traceroute tool that can be run within an existing, open TCP
  connection, therefore bypassing some types of stateful packet filters with
  ease.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install 0trace`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * tcpdump
 {{< /spoiler >}}
 
 ##### 0trace.sh
 
 
 ```
 root@kali:~# 0trace.sh -h
 Usage: /usr/bin/0trace.sh iface target_ip [ target_port ]
 ```
 
 - - -
 
 ##### sendprobe
 
 
 ```
 root@kali:~# sendprobe -h
 Usage: sendprobe src_ip dst_ip sport dport seq ack
 ```
 
 - - -
 
 ##### usleep
 
 Suspend execution for microsecond intervals
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
