---
Title: gitleaks
Homepage: https://github.com/zricethezav/gitleaks
Repository: https://gitlab.com/kalilinux/packages/gitleaks
Architectures: any
Version: 8.2.7-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gitleaks
 
  This package contains a SAST tool for detecting hardcoded secrets
  like passwords, API keys, and tokens in git repos. Gitleaks aims
  to be the easy-to-use, all-in-one solution for finding secrets,
  past or present, in your code.
  Features:
    * Scan for committed secrets
    * Scan for unstaged secrets as part of shifting security left
    * Scan directories and files
    * Available Github Action
    * Custom rules via toml configuration
    * High performance using go-git
    * JSON, SARIF, and CSV reporting
    * Private repo scans using key or password based authentication
 
 **Installed size:** `5.90 MB`  
 **How to install:** `sudo apt install gitleaks`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gitleaks
 
 
 ```
 root@kali:~# gitleaks -h
 Gitleaks scans code, past or present, for secrets
 
 Usage:
   gitleaks [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   detect      detect secrets in code
   help        Help about any command
   protect     protect secrets in code
   version     display gitleaks version
 
 Flags:
   -c, --config string          config file path
                                order of precedence: 
                                1. --config/-c 
                                2. env var GITLEAKS_CONFIG
                                3. (--source/-s)/.gitleaks.toml
                                If none of the three options are used, then gitleaks will use the default config
       --exit-code int          exit code when leaks have been encountered (default 1)
   -h, --help                   help for gitleaks
   -l, --log-level string       log level (debug, info, warn, error, fatal) (default "info")
       --redact                 redact secrets from logs and stdout
   -f, --report-format string   output format (json, csv, sarif) (default "json")
   -r, --report-path string     report file
   -s, --source string          path to source (default: $PWD) (default ".")
   -v, --verbose                show verbose output from scan
 
 Use "gitleaks [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
