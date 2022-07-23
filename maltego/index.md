---
Title: maltego
Homepage: https://www.maltego.com
Repository: https://gitlab.com/kalilinux/packages/maltego
Architectures: all
Version: 4.3.0-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-reporting kali-tools-social-engineering kali-tools-web 
Icon: images/maltego-logo.svg
PackagesInfo: |
 ### maltego
 
  Maltego is an open source intelligence and forensics
  application. It will offer you timous mining and gathering
  of information as well as the representation of this
  information in a easy to understand format.
   
  This package replaces previous packages matlegoce and casefile.
 
 **Installed size:** `217.90 MB`  
 **How to install:** `sudo apt install maltego`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### maltego
 
 
 ```
 root@kali:~# maltego -h
 java is /usr/bin/java
 found java executable in PATH
 pwd: file:/usr/share/maltego/maltego-ui/modules/ext/Java_Config_App.jar
 install conf: /usr/share/maltego/etc/maltego.conf
 install version: v4.3.0
 user conf: /root/.maltego/v4.3.0/etc/maltego.conf
 current java: /usr/lib/jvm/java-11-openjdk-amd64
 /usr/lib/jvm: /usr/lib/jvm
 /usr/lib/jvm: /usr/lib/jvm/openjdk-11
 /usr/lib/jvm: /usr/lib/jvm/java-11-openjdk-amd64
 /usr/lib/jvm: /usr/lib/jvm/java-1.11.0-openjdk-amd64
 /usr/lib/jvm: /usr/lib/jvm/default-java
 does not exist: /usr/lib/jvm/openjdk-11/bin/java
 not jre/jdk: /usr/lib/jvm/openjdk-11
 does not exist: /usr/lib/jvm/bin/java
 not jre/jdk: /usr/lib/jvm
 /usr/lib/jvm/java-1.11.0-openjdk-amd64 VS /usr/lib/jvm/java-11-openjdk-amd64 (/usr/lib/jvm/java-11-openjdk-amd64/bin/java)
 /usr/lib/jvm/java-1.11.0-openjdk-amd64 sym /usr/lib/jvm/java-11-openjdk-amd64
 /usr/lib/jvm/java-1.11.0-openjdk-amd64 VS /usr/lib/jvm/default-java (/usr/lib/jvm/java-11-openjdk-amd64/bin/java)
 /usr/lib/jvm/default-java dig /usr/lib/jvm/java-1.11.0-openjdk-amd64
 trying path: /usr/lib/jvm/default-java
 canonical: /usr/lib/jvm/java-11-openjdk-amd64
 javaHome: /usr/lib/jvm/default-java
 resource:com/paterva/maltego/java/config/jre/TestJDK.class -> /tmp/temp162370067680093740532614496803496/TestJDK.class
 executing: /usr/lib/jvm/java-11-openjdk-amd64/bin/java -classpath /tmp/temp162370067680093740532614496803496 TestJDK, in: .
  result: 0
  command execution finished
  out: 11.0.14.1, 11.0.14.1+1-post-Debian-1, Debian, Linux, amd64
  runtime: 11.0.14_01 x64 Debian
 runtimes: 1
 selected java: /usr/lib/jvm/default-java
 Detecting appropriate heap size...
 resource:com/paterva/maltego/java/config/mem/TestMem.class -> /tmp/temp105935312591119341612614559903851/TestMem.class
 memOut: 8341553152
 pm: 7955/7955
 4077...
 6016...
 6985...
 7470...
 7712...
 7833...
 7894...
 7924...
 7939...
 selected heap size: 5840
 canonical: /usr/lib/jvm/java-11-openjdk-amd64
 javaHome: /usr/lib/jvm/default-java
 executing: /usr/lib/jvm/java-11-openjdk-amd64/bin/java -classpath /tmp/temp162370067680093740532614496803496 TestJDK, in: .
  result: 0
  command execution finished
  out: 11.0.14.1, 11.0.14.1+1-post-Debian-1, Debian, Linux, amd64
 ./../platform/lib/nbexec: WARNING: environment variable DISPLAY is not set
 Module reload options:
   --reload /path/to/module.jar  install or reinstall a module JAR file
 
 Additional module options:
   -i, --import <arg>         
   -u, --updates <arg>        
   -h, --hub <arg>            
   -o, --open <arg1>...<argN> 
   -s, --serverHttpAllowed    
   -p, --automationPort <arg> 
   -m, --machine <arg>        
 
 Core options:
   --laf <LaF classname> use given LookAndFeel class instead of the default
   --fontsize <size>     set the base font size of the user interface, in points
   --locale <language[:country[:variant]]> use specified locale
   --userdir <path>      use specified directory to store user settings
   --cachedir <path>     use specified directory to store user cache, must be different from userdir
   --nosplash            do not show the splash screen
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
