---
Title: watobo
Homepage: https://sourceforge.net/projects/watobo/
Repository: https://gitlab.com/kalilinux/packages/watobo
Architectures: i386 amd64
Version: 1.0.1-0kali1
Metapackages: kali-linux-everything kali-tools-web 
Icon: images/watobo-logo.svg
PackagesInfo: |
 ### watobo
 
  WATOBO is intended to enable security professionals to perform highly efficient
  (semi-automated) web application security audits. It works like a local web
  proxy.
 
 **Installed size:** `3.28 MB`  
 **How to install:** `sudo apt install watobo`  
 
 {{< spoiler "Dependencies:" >}}
 * bundler
 * pry
 * ruby | ruby-interpreter
 * ruby-fxruby
 * ruby-jwt
 * ruby-mechanize 
 * ruby-net-http-pipeline
 * ruby-selenium-webdriver 
 {{< /spoiler >}}
 
 ##### watobo
 
 
 ```
 root@kali:~# watobo -h
 #############################################################
 
      W A T O B O - THE Web Application Toolbox
      brought to you by siberas http://www.siberas.de
 
 #############################################################
 + looking for DEV_ENV environment variable ...[N/A]
 /usr/share/watobo/config/datastore.yml
 /usr/share/watobo/config/forwarding_proxy.yml
 /usr/share/watobo/config/general.yml
 /usr/share/watobo/config/gui.yml
 /usr/share/watobo/config/interceptor.yml
 /usr/share/watobo/config/ott_cache.yml
 /usr/share/watobo/config/scan_policy.yml
 /usr/share/watobo/config/scanner.yml
 /usr/share/watobo/config/scope.yml
 /usr/share/watobo/config/sid_cache.yml
 Creating WATOBO's working directory /root/.watobo.* create configuration directory '/root/.watobo/conf' ...
 OK
 * create temp directory '/root/.watobo/tmp' ...
 OK
 * created workspace folder /root/.watobo/workspace
 ---
 uninitialized constant Watobo::Modules::Active::Ror
 when loading module file /usr/share/watobo/modules/active/RoR/cve_2013_015x.rb
 ---
 ---
 uninitialized constant Watobo::Modules::Active::Sap
 when loading module file /usr/share/watobo/modules/active/sap/business_objects.rb
 ---
 Done generating certificate for /C=DE/O=WATOBO/OU=WATOBO CA/CN=Watobo CA
 >> create DH key ...
 * creating SSL key (DH 2048) ... 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
