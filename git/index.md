---
Title: git
Homepage: https://git-scm.com/
Repository: https://repo.or.cz/w/git/debian.git/
Architectures: any all
Version: 1:2.35.1-1
Metapackages: kali-linux-arm kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-exploitation kali-tools-forensics kali-tools-information-gathering kali-tools-post-exploitation kali-tools-reporting kali-tools-reverse-engineering kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web 
Icon: images/git-logo.svg
PackagesInfo: |
 ### git
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the git main components with minimal dependencies.
  Additional functionality, e.g. a graphical user interface and revision
  tree visualizer, tools for interoperating with other VCS's, or a web
  interface, is provided as separate git* packages.
 
 **Installed size:** `36.90 MB`  
 **How to install:** `sudo apt install git`  
 
 {{< spoiler "Dependencies:" >}}
 * git-man 
 * libc6 
 * libcurl3-gnutls 
 * liberror-perl
 * libexpat1 
 * libpcre2-8-0 
 * perl
 * zlib1g 
 {{< /spoiler >}}
 
 ##### git
 
 The stupid content tracker
 Perl interface to the Git version control system
 
 ```
 root@kali:~# git --help
 usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
            [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
            [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
            [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
            [--super-prefix=<path>] [--config-env=<name>=<envvar>]
            <command> [<args>]
 
 These are common Git commands used in various situations:
 
 start a working area (see also: git help tutorial)
    clone     Clone a repository into a new directory
    init      Create an empty Git repository or reinitialize an existing one
 
 work on the current change (see also: git help everyday)
    add       Add file contents to the index
    mv        Move or rename a file, a directory, or a symlink
    restore   Restore working tree files
    rm        Remove files from the working tree and from the index
 
 examine the history and state (see also: git help revisions)
    bisect    Use binary search to find the commit that introduced a bug
    diff      Show changes between commits, commit and working tree, etc
    grep      Print lines matching a pattern
    log       Show commit logs
    show      Show various types of objects
    status    Show the working tree status
 
 grow, mark and tweak your common history
    branch    List, create, or delete branches
    commit    Record changes to the repository
    merge     Join two or more development histories together
    rebase    Reapply commits on top of another base tip
    reset     Reset current HEAD to the specified state
    switch    Switch branches
    tag       Create, list, delete or verify a tag object signed with GPG
 
 collaborate (see also: git help workflows)
    fetch     Download objects and refs from another repository
    pull      Fetch from and integrate with another repository or a local branch
    push      Update remote refs along with associated objects
 
 'git help -a' and 'git help -g' list available subcommands and some
 concept guides. See 'git help <command>' or 'git help <concept>'
 to read about a specific subcommand or concept.
 See 'git help git' for an overview of the system.
 ```
 
 - - -
 
 ##### git-receive-pack
 
 Receive what is pushed into the repository
 
 ```
 root@kali:~# git-receive-pack -h
 usage: git receive-pack <git-dir>
 
     -q, --quiet           quiet
 
 ```
 
 - - -
 
 ##### git-shell
 
 Restricted login shell for Git-only SSH access
 
 ```
 root@kali:~# git-shell -h
 fatal: Run with no arguments or with -c cmd
 ```
 
 - - -
 
 ##### git-upload-archive
 
 Send archive back to git-archive
 
 ```
 root@kali:~# git-upload-archive -h
 usage: git upload-archive <repo>
 ```
 
 - - -
 
 ##### git-upload-pack
 
 Send objects packed back to git-fetch-pack
 
 ```
 root@kali:~# git-upload-pack -h
 usage: git upload-pack [<options>] <dir>
 
     --stateless-rpc       quit after a single request/response exchange
     --strict              do not try <directory>/.git/ if <directory> is no Git directory
     --timeout <n>         interrupt transfer after <n> seconds of inactivity
 
 ```
 
 - - -
 
 ### git-all
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This is a dummy package which brings in all subpackages.
 
 **Installed size:** `957 KB`  
 **How to install:** `sudo apt install git-all`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * git-cvs
 * git-doc
 * git-email
 * git-gui
 * git-mediawiki
 * git-svn
 * gitk
 * gitweb
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-cvs
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the git cvsimport, cvsexportcommit, and cvsserver
  tools, which allow Git to read from and write to CVS repositories and
  offer access over CVS protocol to Git repositories.
   
  The git cvsimport tool can incrementally import from a repository that
  is being actively developed and only requires remote access over CVS
  protocol. Unfortunately, in many situations the import leads to
  incorrect results. For reliable, one-shot imports, cvs2git from the
  cvs2svn package or parsecvs may be a better fit.
 
 **Installed size:** `1.30 MB`  
 **How to install:** `sudo apt install git-cvs`  
 
 {{< spoiler "Dependencies:" >}}
 * cvsps
 * git 
 * libdbd-sqlite3-perl
 {{< /spoiler >}}
 
 ##### git-cvsserver
 
 A CVS server emulator for Git
 
 ```
 root@kali:~# git-cvsserver --help
 Unknown option: help
 usage: git cvsserver [options] [pserver|server] [<directory> ...]
     --base-path <path>  : Prepend to requested CVSROOT
                           Can be read from GIT_CVSSERVER_BASE_PATH
     --strict-paths      : Don't allow recursing into subdirectories
     --export-all        : Don't check for gitcvs.enabled in config
     --version, -V       : Print version information and exit
     -h, -H              : Print usage information and exit
 
 <directory> ... is a list of allowed directories. If no directories
 are given, all are allowed. This is an additional restriction, gitcvs
 access still needs to be enabled by the gitcvs.enabled config option.
 Alternately, one directory may be specified in GIT_CVSSERVER_ROOT.
 ```
 
 - - -
 
 ### git-daemon-run
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  git-daemon, as provided by the git package, is a simple server for git
  repositories, ideally suited for read-only updates, i.e. pulling from git
  repositories through the network.  This package provides a runit service
  for running git-daemon permanently.  This configuration is simpler and
  more reliable than git-daemon-sysvinit, at a cost of being less
  familiar for administrators accustomed to sysvinit.
 
 **Installed size:** `969 KB`  
 **How to install:** `sudo apt install git-daemon-run`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * git 
 * runit
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-daemon-sysvinit
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  git-daemon, as provided by the git package, is a simple server for git
  repositories, ideally suited for read-only updates, i.e. pulling from git
  repositories through the network.  This package provides a sysvinit service
  for running git-daemon permanently.  Unlike git-daemon-run, this
  package provides the usual sysvinit service management commands
  ("service git-daemon start/stop") for git-daemon.
 
 **Installed size:** `972 KB`  
 **How to install:** `sudo apt install git-daemon-sysvinit`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * git 
 * lsb-base 
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-doc
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the documentation.
 
 **Installed size:** `11.95 MB`  
 **How to install:** `sudo apt install git-doc`  
 
 
 - - -
 
 ### git-email
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the git-send-email program for sending series of
  patch emails.
 
 **Installed size:** `1.00 MB`  
 **How to install:** `sudo apt install git-email`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-gui
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the git graphical user interface.
   
  If aspell is installed, it can check the spelling of commit messages
  as the user types.
   
  If meld is installed, it can be used for displaying diffs and for
  interactive merge conflict resolution.
 
 **Installed size:** `2.32 MB`  
 **How to install:** `sudo apt install git-gui`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * tk
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-man
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides reference documentation for use by the 'man'
  utility and the 'git help' command.
 
 **Installed size:** `1.91 MB`  
 **How to install:** `sudo apt install git-man`  
 
 
 - - -
 
 ### git-mediawiki
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the mediawiki remote helper, which allows Git to
  read from and write to a wiki such as Wikipedia as though it were a
  remote Git repository, and a 'git mw' command that can show a preview
  of how wiki markup will be rendered before pushing.
 
 **Installed size:** `1017 KB`  
 **How to install:** `sudo apt install git-mediawiki`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * libdatetime-format-iso8601-perl
 * liblwp-protocol-https-perl
 * libmediawiki-api-perl 
 {{< /spoiler >}}
 
 
 - - -
 
 ### git-svn
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides tools for interoperating with Subversion repositories,
  and importing SVN development history.
 
 **Installed size:** `1.17 MB`  
 **How to install:** `sudo apt install git-svn`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * libsvn-perl
 * libterm-readkey-perl
 * libyaml-perl
 {{< /spoiler >}}
 
 
 - - -
 
 ### gitk
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package provides the gitk program, a tcl/tk revision tree visualizer.
 
 **Installed size:** `1.74 MB`  
 **How to install:** `sudo apt install gitk`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * tk
 {{< /spoiler >}}
 
 ##### gitk
 
 The Git repository browser
 
 ```
 root@kali:~# gitk -h
 application-specific initialization failed: couldn't connect to display ""
 Error in startup script: Command-specific options:
  -sync:     Use synchronous mode for display server
  -colormap: Colormap for main window
  -display:  Display to use
  -geometry: Initial geometry for window
  -name:     Name to use for application
  -visual:   Visual for main window
  -use:      Id of window in which to embed application
  --:        Marks the end of the options
  -help:     Print summary of command-line options and abort
     (processing arguments in argv variable)
     invoked from within
 "load /usr/lib/x86_64-linux-gnu/libtk8.6.so"
     ("package ifneeded Tk 8.6.12" script)
     invoked from within
 "package require Tk"
     (file "/usr/bin/gitk" line 10)
 ```
 
 - - -
 
 ### gitweb
 
  Git is popular version control system designed to handle very large
  projects with speed and efficiency; it is used for many high profile
  open source projects, most notably the Linux kernel.
   
  Git falls in the category of distributed source code management tools.
  Every Git working directory is a full-fledged repository with full
  revision tracking capabilities, not dependent on network access or a
  central server.
   
  This package configures a web interface for browsing git repositories.
   
  If apache2 is installed, the web interface is automatically made
  available at http://localhost/gitweb.  Other servers that support CGI
  or mod_perl are supported through manual configuration.
   
  If libcgi-fast-perl is installed, gitweb can also be run over FastCGI
  (and served by nginx, for example).
 
 **Installed size:** `978 KB`  
 **How to install:** `sudo apt install gitweb`  
 
 {{< spoiler "Dependencies:" >}}
 * git 
 * libcgi-pm-perl
 * perl
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
