---
Title: regripper
Homepage: https://code.google.com/p/regripper/
Repository: https://gitlab.com/kalilinux/packages/regripper
Architectures: i386 amd64
Version: 2.5-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### regripper
 
  RegRipper is an open source tool, written in Perl, for extracting/parsing
  information (keys, values, data) from the Registry and presenting it for
  analysis.
   
  RegRipper consists of two basic tools, both of which provide similar
  capability. The RegRipper GUI allows the analyst to select a hive to parse, an
  output file for the results, and a profile (list of plugins) to run against the
  hive. When the analyst launches the tool against the hive, the results go to
  the file that the analyst designated. If the analyst chooses to parse the
  System hive, they might also choose to send the results to system.txt. The GUI
  tool
  will also create a log of it's activity in the same directory as the output
  file, using the same file name but using the .log extension (i.e., if the
  output is written to system.txt, the log will be written to system.log).
 
 **Installed size:** `7.60 MB`  
 **How to install:** `sudo apt install regripper`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 * perl
 * wine
 {{< /spoiler >}}
 
 ##### regripper
 
 
 ```
 root@kali:~# regripper -h
 ┏━(Message from Kali developers)
 ┃
 ┃ You may need to install the wine32 package first:
 ┃  # dpkg --add-architecture i386 && apt update && apt -y install wine32
 ┃
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
regripper
```

![regripper](images/regripper.png)
