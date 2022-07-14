---
Title: peirates
Homepage: https://github.com/inguardians/peirates
Repository: https://gitlab.com/kalilinux/packages/peirates
Architectures: any
Version: 1.0.30-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### peirates
 
  This package contains a Kubernetes penetration tool, enables an attacker to
  escalate privilege and pivot through a Kubernetes cluster. It automates known
  techniques to steal and collect service accounts, obtain further code
  execution, and gain control of the cluster.
 
 **Installed size:** `42.97 MB`  
 **How to install:** `sudo apt install peirates`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### peirates
 
 
 ```
 root@kali:~# peirates -h
 [0/0]0x0
 Usage of peirates:
   -L string
     	List of comma-seperated Pods: ex pod1,pod2,pod3
   -c string
     	Command to run in pods (default "hostname")
   -i string
     	API Server IP address: ex. 10.22.34.67
   -p string
     	API Server Port: ex 443, 6443
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
