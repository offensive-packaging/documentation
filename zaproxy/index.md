---
Title: zaproxy
Homepage: https://github.com/zaproxy/zaproxy
Repository: https://gitlab.com/kalilinux/packages/zaproxy
Architectures: all
Version: 2.11.1-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: images/zaproxy-logo.svg
PackagesInfo: |
 ### zaproxy
 
  The OWASP Zed Attack Proxy (ZAP) is an easy to use
  integrated penetration testing tool for finding
  vulnerabilities in web applications.
   
  It is designed to be used by people with a wide range of
  security experience and as such is ideal for developers and
  functional testers who are new to penetration testing as
  well as being a useful addition to an experienced pen
  testers toolbox.
  https://www.owasp.org/index.php/ZAP
 
 **Installed size:** `221.72 MB`  
 **How to install:** `sudo apt install zaproxy`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 {{< /spoiler >}}
 
 ##### owasp-zap
 
 
 ```
 root@kali:~# owasp-zap -h
 Found Java version 11.0.15
 Available memory: 14926 MB
 Using JVM args: -Xmx3731m
 668 [main] INFO  org.parosproxy.paros.Constant - Copying default configuration to /root/.ZAP/config.xml
 772 [main] INFO  org.parosproxy.paros.Constant - Creating directory /root/.ZAP/session
 772 [main] INFO  org.parosproxy.paros.Constant - Creating directory /root/.ZAP/dirbuster
 772 [main] INFO  org.parosproxy.paros.Constant - Creating directory /root/.ZAP/fuzzers
 772 [main] INFO  org.parosproxy.paros.Constant - Creating directory /root/.ZAP/plugin
 Usage:
 	zap.sh [Options]
 Core options:
 	-version                 Reports the ZAP version
 	-cmd                     Run inline (exits when command line options complete)
 	-daemon                  Starts ZAP in daemon mode, i.e. without a UI
 	-config <kvpair>         Overrides the specified key=value pair in the configuration file
 	-configfile <path>       Overrides the key=value pairs with those in the specified properties file
 	-dir <dir>               Uses the specified directory instead of the default one
 	-installdir <dir>        Overrides the code that detects where ZAP has been installed with the specified directory
 	-h                       Shows all of the command line options available, including those added by add-ons
 	-help                    The same as -h
 	-newsession <path>       Creates a new session at the given location
 	-session <path>          Opens the given session after starting ZAP
 	-host <host>             Overrides the host used for proxying specified in the configuration file
 	-port <port>             Overrides the port used for proxying specified in the configuration file
 	-lowmem                  Use the database instead of memory as much as possible - this is still experimental
 	-experimentaldb          Use the experimental generic database code, which is not surprisingly also still experimental
 	-nostdout                Disables the default logging through standard output
 	-silent                  Ensures ZAP does not make any unsolicited requests, including check for updates
 Add-on options:
 	-quickurl <target url>   The URL to attack, e.g. http://www.example.com
 	-quickout <filename>     The file to write the HTML/JSON/MD/XML results to (based on the file extension)
 	-quickprogress:          Display progress bars while scanning
 	-script <script>         Run the specified script from commandline or load in GUI
 	-addoninstall <addOnId>   Installs the add-on with specified ID from the ZAP Marketplace
 	-addoninstallall          Install all available add-ons from the ZAP Marketplace
 	-addonuninstall <addOnId> Uninstalls the Add-on with specified ID
 	-addonupdate              Update all changed add-ons from the ZAP Marketplace
 	-addonlist                List all of the installed add-ons
 	-certload <path>         Loads the Root CA certificate from the specified file name
 	-certpubdump <path>      Dumps the Root CA public certificate into the specified file name, this is suitable for importing into browsers
 	-certfulldump <path>     Dumps the Root CA full certificate (including the private key) into the specified file name, this is suitable for importing into ZAP
 	-graphqlfile <path>       Imports a GraphQL Schema from a File
 	-graphqlurl <url>         Imports a GraphQL Schema from a URL
 	-graphqlendurl <url>      Sets the Endpoint URL
 	-hud                     Launches a browser configured to proxy through ZAP with the HUD enabled, for use in daemon mode
 	-hudurl <url>            Launches a browser as per the -hud option with the specified URL
 	-hudbrowser <browser>    Launches a browser as per the -hud option with the specified browser, supported options: Chrome, Firefox by default Firefox
 	-autorun <filename>      Run the automation jobs specified in the file
 	-autogenmin <filename>   Generate template automation file with the key parameters
 	-autogenmax <filename>   Generate template automation file with all parameters
 	-autogenconf <filename>  Generate template automation file using the current configuration
 	-openapifile <path>      Imports an OpenAPI definition from the specified file name
 	-openapiurl <url>        Imports an OpenAPI definition from the specified URL
 	-openapitargeturl <url>  The Target URL, to override the server URL present in the OpenAPI definition. Refer to the help for supported format.
 
 ```
 
 - - -
 
 ##### zaproxy
 
 
 ```
 root@kali:~# zaproxy -h
 Found Java version 11.0.15
 Available memory: 14926 MB
 Using JVM args: -Xmx3731m
 Usage:
 	zap.sh [Options]
 Core options:
 	-version                 Reports the ZAP version
 	-cmd                     Run inline (exits when command line options complete)
 	-daemon                  Starts ZAP in daemon mode, i.e. without a UI
 	-config <kvpair>         Overrides the specified key=value pair in the configuration file
 	-configfile <path>       Overrides the key=value pairs with those in the specified properties file
 	-dir <dir>               Uses the specified directory instead of the default one
 	-installdir <dir>        Overrides the code that detects where ZAP has been installed with the specified directory
 	-h                       Shows all of the command line options available, including those added by add-ons
 	-help                    The same as -h
 	-newsession <path>       Creates a new session at the given location
 	-session <path>          Opens the given session after starting ZAP
 	-host <host>             Overrides the host used for proxying specified in the configuration file
 	-port <port>             Overrides the port used for proxying specified in the configuration file
 	-lowmem                  Use the database instead of memory as much as possible - this is still experimental
 	-experimentaldb          Use the experimental generic database code, which is not surprisingly also still experimental
 	-nostdout                Disables the default logging through standard output
 	-silent                  Ensures ZAP does not make any unsolicited requests, including check for updates
 Add-on options:
 	-certload <path>         Loads the Root CA certificate from the specified file name
 	-certpubdump <path>      Dumps the Root CA public certificate into the specified file name, this is suitable for importing into browsers
 	-certfulldump <path>     Dumps the Root CA full certificate (including the private key) into the specified file name, this is suitable for importing into ZAP
 	-quickurl <target url>   The URL to attack, e.g. http://www.example.com
 	-quickout <filename>     The file to write the HTML/JSON/MD/XML results to (based on the file extension)
 	-quickprogress:          Display progress bars while scanning
 	-graphqlfile <path>       Imports a GraphQL Schema from a File
 	-graphqlurl <url>         Imports a GraphQL Schema from a URL
 	-graphqlendurl <url>      Sets the Endpoint URL
 	-autorun <filename>      Run the automation jobs specified in the file
 	-autogenmin <filename>   Generate template automation file with the key parameters
 	-autogenmax <filename>   Generate template automation file with all parameters
 	-autogenconf <filename>  Generate template automation file using the current configuration
 	-openapifile <path>      Imports an OpenAPI definition from the specified file name
 	-openapiurl <url>        Imports an OpenAPI definition from the specified URL
 	-openapitargeturl <url>  The Target URL, to override the server URL present in the OpenAPI definition. Refer to the help for supported format.
 	-script <script>         Run the specified script from commandline or load in GUI
 	-addoninstall <addOnId>   Installs the add-on with specified ID from the ZAP Marketplace
 	-addoninstallall          Install all available add-ons from the ZAP Marketplace
 	-addonuninstall <addOnId> Uninstalls the Add-on with specified ID
 	-addonupdate              Update all changed add-ons from the ZAP Marketplace
 	-addonlist                List all of the installed add-ons
 	-hud                     Launches a browser configured to proxy through ZAP with the HUD enabled, for use in daemon mode
 	-hudurl <url>            Launches a browser as per the -hud option with the specified URL
 	-hudbrowser <browser>    Launches a browser as per the -hud option with the specified browser, supported options: Chrome, Firefox by default Firefox
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![zaproxy](images/zaproxy.png)
