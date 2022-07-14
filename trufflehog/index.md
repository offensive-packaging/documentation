---
Title: trufflehog
Homepage: https://github.com/trufflesecurity/truffleHog
Repository: https://gitlab.com/kalilinux/packages/trufflehog
Architectures: all
Version: 2.2.1-0kali1
Metapackages: 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### trufflehog
 
  This package contains a utitlity to search through git repositories for
  secrets, digging deep into commit history and branches. This is effective at
  finding secrets accidentally committed.
 
 **Installed size:** `41 KB`  
 **How to install:** `sudo apt install trufflehog`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-git
 * python3-trufflehogregexes
 {{< /spoiler >}}
 
 ##### trufflehog
 
 
 ```
 root@kali:~# trufflehog -h
 usage: trufflehog [-h] [--json] [--regex] [--rules RULES] [--allow ALLOW]
                   [--entropy DO_ENTROPY] [--since_commit SINCE_COMMIT]
                   [--max_depth MAX_DEPTH] [--branch BRANCH]
                   [-i INCLUDE_PATHS_FILE] [-x EXCLUDE_PATHS_FILE]
                   [--repo_path REPO_PATH] [--cleanup]
                   git_url
 
 Find secrets hidden in the depths of git.
 
 positional arguments:
   git_url               URL for secret searching
 
 options:
   -h, --help            show this help message and exit
   --json                Output in JSON
   --regex               Enable high signal regex checks
   --rules RULES         Ignore default regexes and source from json file
   --allow ALLOW         Explicitly allow regexes from json list file
   --entropy DO_ENTROPY  Enable entropy checks
   --since_commit SINCE_COMMIT
                         Only scan from a given commit hash
   --max_depth MAX_DEPTH
                         The max commit depth to go back when searching for
                         secrets
   --branch BRANCH       Name of the branch to be scanned
   -i INCLUDE_PATHS_FILE, --include_paths INCLUDE_PATHS_FILE
                         File with regular expressions (one per line), at least
                         one of which must match a Git object path in order for
                         it to be scanned; lines starting with "#" are treated
                         as comments and are ignored. If empty or not provided
                         (default), all Git object paths are included unless
                         otherwise excluded via the --exclude_paths option.
   -x EXCLUDE_PATHS_FILE, --exclude_paths EXCLUDE_PATHS_FILE
                         File with regular expressions (one per line), none of
                         which may match a Git object path in order for it to
                         be scanned; lines starting with "#" are treated as
                         comments and are ignored. If empty or not provided
                         (default), no Git object paths are excluded unless
                         effectively excluded via the --include_paths option.
   --repo_path REPO_PATH
                         Path to the cloned repo. If provided, git_url will not
                         be used
   --cleanup             Clean up all temporary result files
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
