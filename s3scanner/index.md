---
Title: s3scanner
Homepage: https://github.com/sa7mon/S3Scanner
Repository: https://gitlab.com/kalilinux/packages/s3scanner
Architectures: all
Version: 2.0.2-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### s3scanner
 
  This package contains a tool to find open S3 buckets and dump their contents.
  The features are:
    * zap Multi-threaded scanning
    * telescope Supports tons of S3-compatible APIs
    * female_detective Scans all bucket permissions to find misconfigurations
    * floppy_disk Dump bucket contents to a local folder
    * whale Docker support
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install s3scanner`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-boto3
 {{< /spoiler >}}
 
 ##### s3scanner
 
 
 ```
 root@kali:~# s3scanner -h
 usage: s3scanner [-h] [--version] [--threads n] [--endpoint-url ENDPOINT_URL]
                  [--endpoint-address-style {path,vhost}] [--insecure]
                  {scan,dump} ...
 
 s3scanner: Audit unsecured S3 buckets
            by Dan Salmon - github.com/sa7mon, @bltjetpack
 
 options:
   -h, --help            show this help message and exit
   --version             Display the current version of this tool
   --threads n, -t n     Number of threads to use. Default: 4
   --endpoint-url ENDPOINT_URL, -u ENDPOINT_URL
                         URL of S3-compliant API. Default: https://s3.amazonaws.com
   --endpoint-address-style {path,vhost}, -s {path,vhost}
                         Address style to use for the endpoint. Default: path
   --insecure, -i        Do not verify SSL
 
 mode:
   {scan,dump}           (Must choose one)
     scan                Scan bucket permissions
     dump                Dump the contents of buckets
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
