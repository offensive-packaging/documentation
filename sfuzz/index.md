---
Title: sfuzz
Homepage: http://aconole.brad-x.com/programs/sfuzz.html
Repository: https://gitlab.com/kalilinux/packages/sfuzz
Architectures: any
Version: 0.7.0-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-fuzzing kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sfuzz
 
  In the same vein as the Generic Protocol Framework, sfuzz is
  a really simple to use black box testing suite called Simple
  Fuzzer (what else would you expect?). The goal is to provide
  a simple to use, but fairly powerful and flexible black box
  testing utility.
 
 **Installed size:** `191 KB`  
 **How to install:** `sudo apt install sfuzz`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sfo
 
 
 
 - - -
 
 ##### sfuzz
 
 
 ```
 root@kali:~# sfuzz -h
 		Simple Fuzzer
 By:	 Aaron Conole
 version: 0.7.0
 url:	 http://aconole.brad-x.com/programs/sfuzz.html
 EMAIL:	 apconole@yahoo.com
 Build-prefix: /usr
 	-h	 This message.
 	-V	 Version information.
 
 networking / output:
 	-v	 Verbose output
 	-q	 Silent output mode (generally for CLI fuzzing)
 	-X	 prints the output in hex
 
 	-b	 Begin fuzzing at the test specified.
 	-e	 End testing on failure.
 	-t	 Wait time for reading the socket
 	-S	 Remote host
 	-p	 Port
 	-T|-U|-O TCP|UDP|Output mode
 	-R	 Refrain from closing connections (ie: "leak" them)
 
 	-f	 Config File
 	-L	 Log file
 	-n	 Create a new logfile after each fuzz
 	-r	 Trim the tailing newline
 	-D	 Define a symbol and value (X=y).
 	-l	 Only perform literal fuzzing
 	-s	 Only perform sequence fuzzing
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sfuzz Usage Example

Fuzz the target server (`-S 192.168.1.1`) on port 10443 (`-p 10443`) with TCP output mode (`-T`), using the basic HTTP config (`-f /usr/share/sfuzz/sfuzz-sample/basic.http`):

```
root@kali:~# sfuzz -S 192.168.1.1 -p 10443 -T -f /usr/share/sfuzz/sfuzz-sample/basic.http
[12:53:47] dumping options:
    filename: </usr/share/sfuzz/sfuzz-sample/basic.http>
    state:    <8>
    lineno:   <56>
    literals:  [74]
    sequences: [34]
    symbols: [0]
    req_del:  <200>
    mseq_len: <10024>
    plugin: <none>
    s_syms: <0>
    literal[1] = [AREALLYBADSTRING]
```
