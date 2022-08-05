---
Title: bing-ip2hosts
Homepage: https://www.morningstarsecurity.com/research/bing-ip2hosts
Repository: https://gitlab.com/kalilinux/packages/bing-ip2hosts
Architectures: all
Version: 1.0.4-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bing-ip2hosts
 
  This package contains a Bing.com web scraper that discovers hostnames by IP
  address. Bing is the flagship Microsoft search engine formerly known as MSN
  Search and Live Search.
   
  It provides a feature unique to search engines - it allows searching by IP
  address. Bing-ip2hosts uses this feature.
   
  It can be used to discover subdomains and other related domains. It also helps
  to identify websites hosted in a shared hosting environment. This technique
  follows best practices during the reconnaissance phase of a penetration test
  or bug bounty, to expand the target's attack surface.
   
  Unlike other many other recon tools that web scrape Bing, this tool has smart
  scraping behaviour to maximize the discovery of hostnames.
 
 **Installed size:** `29 KB`  
 **How to install:** `sudo apt install bing-ip2hosts`  
 
 {{< spoiler "Dependencies:" >}}
 * wget
 {{< /spoiler >}}
 
 ##### bing-ip2hosts
 
 
 ```
 root@kali:~# bing-ip2hosts -h
 
   m,                   .,recon:,        ,,
   #####               ]##""^^"%##m    %##b
   ####b               ]##      `##b
   ####b               ]##       ##    i##    @#b,######m       ,######m ##b
   ####b 1mw,          ]##MMM####      i##    ]###`    %##     ###`    `@##
   ####b  1#####Nw,    ]##``    @#b    i##    ]##       ###   ###       j##
   ####i   %########[  ]##       @##   i##    ]##       ###   ##g       j##
   ####n      2#####[  ]##      @##    i##    ]##       ###   @##       {##
   ####g  ,#########b  ]##   ,,e###    j##    ]##       ###    7##m,,,s#M##
   #############M^     'WWWWWW%b^       ii    'nn       nn*      `1337` g##
   ##########"                                                          G##
     "%##"                                                     @#Gmmem###G
   ,i                ,s2e,     ##                                  ````
    `               "`   %#    ##                             T#
   ]#   ]#,#M5@#p         #b   #H#H%@#     s#M5O#o   ,#MSSM  W@##W=  s#SSW
   ]#   j#p    ^#p      ,#M    ##    @#   ##'   'O#  S#,      ]#     #b
   ]#   j#      #M    ,#M      ##    @#   #o     O#    "SXm   ]#      ^"@#
   ]#   j##,  ,##   ,#2        ##    @#   7#.   .#O  ,   ]#   ]#Q       ,#s
   ]#   j######'    #######x   ##    @#    s#####o    ####^    #Tt    ####^
        j#
        j#          bing-ip2hosts (1.0.4) by Andrew Horton @urbanadventurer
        j#          https://morningstarsecurity.com/research/bing-ip2hosts
                    https://github.com/urbanadventurer/bing-ip2hosts
 [Press Enter]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bing-ip2hosts Usage Examples

```
root@kali:~# bing-ip2hosts -p microsoft.com
[ 65.55.58.201 | Scraping 1 | Found 0 | / ]
http://microsoft.com
http://research.microsoft.com
http://www.answers.microsoft.com
http://www.microsoft.com
http://www.msdn.microsoft.com
```

```
root@kali:~# bing-ip2hosts -p 173.194.33.80
[ 173.194.33.80 | Scraping 60-69 of 73 | Found 41 | | ]| / ]
http://asia.google.com
http://desktop.google.com
http://ejabat.google.com
http://google.netscape.com
http://partner-client.google.com
http://picasa.google.com
```
