---
Title: jsql
Homepage: https://github.com/ron190/jsql-injection
Repository: https://gitlab.com/kalilinux/packages/jsql
Architectures: all
Version: 0.85-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/jsql-logo.svg
PackagesInfo: |
 ### jsql-injection
 
  jSQL Injection is a lightweight application used to find database information
  from a distant server.
  jSQL is free, open source and cross-platform (Windows, Linux, Mac OS X,
  Solaris).
 
 **Installed size:** `7.74 MB`  
 **How to install:** `sudo apt install jsql-injection`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 * java-wrappers
 {{< /spoiler >}}
 
 ##### jsql
 
 
 ```
 root@kali:~# jsql -h
 WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
 ```
 
 - - -
 
 ##### jsql-injection
 
 
 ```
 root@kali:~# jsql-injection -h
 WARNING: sun.reflect.Reflection.getCallerClass is not supported. This will impact performance.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
jsql
```

![jsql](images/jsql.png)
