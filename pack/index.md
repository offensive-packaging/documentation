---
Title: pack
Homepage: https://medium.com/@iphelix
Repository: https://gitlab.com/kalilinux/packages/pack
Architectures: all
Version: 0.0.4-0kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pack
 
  PACK was developed in order to aid in a password cracking
  competition "Crack Me If You Can" that occurred during
  Defcon 2010. The goal of this toolkit is to aid in
  preparation for the "better than bruteforce" password
  attacks by analyzing common ways that people create
  passwords. After the analysis stage, the statistical
  database can be used to generate attack masks for tools
  such as oclHashcat.
   
  NOTE: This tool itself can not crack passwords, but helps
  other tools crack more passwords faster.
 
 **Installed size:** `110 KB`  
 **How to install:** `sudo apt install pack`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-enchant
 {{< /spoiler >}}
 
 ##### dictstat
 
 
 ```
 root@kali:~# dictstat -h
 ┏━(Message from Kali developers)
 ┃
 ┃ The command dictstat is deprecated. Please use statsgen instead.
 ┃
 ┗━
 ```
 
 - - -
 
 ##### maskgen
 
 
 ```
 root@kali:~# maskgen -h
 Usage: maskgen pass0.masks [pass1.masks ...] [options]
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -t 86400, --targettime=86400
                         Target time of all masks (seconds)
   -o masks.hcmask, --outputmasks=masks.hcmask
                         Save masks to a file
   --showmasks           Show matching masks
 
   Individual Mask Filter Options:
     --minlength=8       Minimum password length
     --maxlength=8       Maximum password length
     --mintime=3600      Minimum mask runtime (seconds)
     --maxtime=3600      Maximum mask runtime (seconds)
     --mincomplexity=1   Minimum complexity
     --maxcomplexity=100
                         Maximum complexity
     --minoccurrence=1   Minimum occurrence
     --maxoccurrence=100
                         Maximum occurrence
 
   Mask Sorting Options:
     --optindex          sort by mask optindex (default)
     --occurrence        sort by mask occurrence
     --complexity        sort by mask complexity
 
   Check mask coverage:
     --checkmasks=?u?l?l?l?l?l?d,?l?l?l?l?l?d?d
                         check mask coverage
     --checkmasksfile=masks.hcmask
                         check mask coverage in a file
 
   Miscellaneous options:
     --pps=1000000000    Passwords per Second
     -q, --quiet         Don't show headers.
 ```
 
 - - -
 
 ##### pack200
 
 Packages a JAR file into a compressed pack200 file for web deployment.
 
 ```
 root@kali:~# pack200 -h
 
 Warning: The pack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 Usage:  pack200 [-opt... | --option=value]... x.pack[.gz] y.jar
 
 Packing Options
   -r, --repack                    repack or normalize a jar, suitable for 
                                   signing with jarsigner
   -g, --no-gzip                   output a plain pack file, suitable to be
                                   compressed with a file compression utility
   --gzip                          (default) post compress the pack output
                                   with gzip
   -G, --strip-debug               remove debugging attributes (SourceFile,
                                   LineNumberTable, LocalVariableTable
                                   and LocalVariableTypeTable) while packing
   -O, --no-keep-file-order        do not transmit file ordering information
   --keep-file-order               (default) preserve input file ordering
   -S{N}, --segment-limit={N}      limit segment sizes (default unlimited)
   -E{N}, --effort={N}             packing effort (default N=5)
   -H{h}, --deflate-hint={h}       transmit deflate hint: true, false,
                                   or keep (default)
   -m{V}, --modification-time={V}  transmit modtimes: latest or keep (default)
   -P{F}, --pass-file={F}          transmit the given input element(s) unchanged
   -U{a}, --unknown-attribute={a}  unknown attribute action: error, strip,
                                   or pass (default)
   -C{N}={L}, --class-attribute={N}={L}  (user-defined attribute)
   -F{N}={L}, --field-attribute={N}={L}  (user-defined attribute)
   -M{N}={L}, --method-attribute={N}={L} (user-defined attribute)
   -D{N}={L}, --code-attribute={N}={L}   (user-defined attribute)
   -f{F}, --config-file={F}        read file F for Pack200.Packer properties
   -v, --verbose                   increase program verbosity
   -q, --quiet                     set verbosity to lowest level
   -l{F}, --log-file={F}           output to the given log file, 
                                   or '-' for System.out
   -?, -h, --help                  print this help message
   -V, --version                   print program version
   -J{X}                           pass option X to underlying Java VM
 
 Notes:
   The -P, -C, -F, -M, and -D options accumulate.
   Example attribute definition:  -C SourceFile=RUH .
   Config. file properties are defined by the Pack200 API.
   For meaning of -S, -E, -H-, -m, -U values, see Pack200 API.
   Layout definitions (like RUH) are defined by JSR 200.
 
 Repacking mode updates the JAR file with a pack/unpack cycle:
     pack200 [-r|--repack] [-opt | --option=value]... [repackedy.jar] y.jar
 
 
 Exit Status:
   0 if successful, >0 if an error occurred
 
 Warning: The pack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 ```
 
 - - -
 
 ##### policygen
 
 
 ```
 root@kali:~# policygen -h
 Usage: policygen [options]
 
 Type --help for more options
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -o masks.hcmask, --outputmasks=masks.hcmask
                         Save masks to a file
   --pps=1000000000      Passwords per Second
   --showmasks           Show matching masks
   --noncompliant        Generate masks for noncompliant passwords
   -q, --quiet           Don't show headers.
 
   Password Policy:
     Define the minimum (or maximum) password strength policy that you
     would like to test
 
     --minlength=8       Minimum password length
     --maxlength=8       Maximum password length
     --mindigit=1        Minimum number of digits
     --minlower=1        Minimum number of lower-case characters
     --minupper=1        Minimum number of upper-case characters
     --minspecial=1      Minimum number of special characters
     --maxdigit=3        Maximum number of digits
     --maxlower=3        Maximum number of lower-case characters
     --maxupper=3        Maximum number of upper-case characters
     --maxspecial=3      Maximum number of special characters
 ```
 
 - - -
 
 ##### rulegen
 
 
 ```
 root@kali:~# rulegen -h
 Usage: rulegen [options] passwords.txt
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -b rockyou, --basename=rockyou
                         Output base name. The following files will be
                         generated: basename.words, basename.rules and
                         basename.stats
   -w wiki.dict, --wordlist=wiki.dict
                         Use a custom wordlist for rule analysis.
   -q, --quiet           Don't show headers.
   --threads=THREADS     Parallel threads to use for processing.
 
   Fine tune source word generation::
     --maxworddist=10    Maximum word edit distance (Levenshtein)
     --maxwords=5        Maximum number of source word candidates to consider
     --morewords         Consider suboptimal source word candidates
     --simplewords       Generate simple source words for given passwords
 
   Fine tune rule generation::
     --maxrulelen=10     Maximum number of operations in a single rule
     --maxrules=5        Maximum number of rules to consider
     --morerules         Generate suboptimal rules
     --simplerules       Generate simple rules insert,delete,replace
     --bruterules        Bruteforce reversal and rotation rules (slow)
 
   Fine tune spell checker engine::
     --providers=aspell,myspell
                         Comma-separated list of provider engines
 
   Debuggin options::
     -v, --verbose       Show verbose information.
     -d, --debug         Debug rules.
     --password          Process the last argument as a password not a file.
     --word=Password     Use a custom word for rule analysis
     --hashcat           Test generated rules with hashcat-cli
 ```
 
 - - -
 
 ##### statsgen
 
 
 ```
 root@kali:~# statsgen -h
 Usage: statsgen [options] passwords.txt
 
 Type --help for more options
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -o password.masks, --output=password.masks
                         Save masks and stats to a file
   --hiderare            Hide statistics covering less than 1% of the sample
   -q, --quiet           Don't show headers.
 
   Password Filters:
     --minlength=8       Minimum password length
     --maxlength=8       Maximum password length
     --charset=loweralpha,numeric
                         Password charset filter (comma separated)
     --simplemask=stringdigit,allspecial
                         Password mask filter (comma separated)
 ```
 
 - - -
 
 ##### unpack200
 
 Transforms a packed file produced by pack200(1) into a JAR file for web deployment.
 
 ```
 root@kali:~# unpack200 -h
 
 Warning: The unpack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 Usage:  unpack200 [-opt... | --option=value]... x.pack[.gz] y.jar
 
 Unpacking Options
   -H{h}, --deflate-hint={h}     override transmitted deflate hint:
                                 true, false, or keep (default)
   -r, --remove-pack-file        remove input file after unpacking
   -v, --verbose                 increase program verbosity
   -q, --quiet                   set verbosity to lowest level
   -l{F}, --log-file={F}         output to the given log file,
                                 or '-' for standard output (default)
   -?, -h, --help                print this help message
   -V, --version                 print program version
 
 Exit Status:
   0 if successful, >0 if an error occurred
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## statsgen Usage Example

Generate statistics for passwords with a length of 10 (`–minlength=10 –maxlength=10`) contained in the rockyou wordlist (`rockyou.txt`):

```
root@kali:~# statsgen --minlength=10 --maxlength=10 rockyou.txt
                       _
     StatsGen 0.0.3   | |
      _ __   __ _  ___| | _
     | '_ \ / _` |/ __| |/ /
     | |_) | (_| | (__|   <
     | .__/ \__,_|\___|_|\_\
     | |
     |_| iphelix@thesprawl.org


[*] Analyzing passwords in [rockyou.txt]
[+] Analyzing 14% (2013695/14344391) of passwords
    NOTE: Statistics below is relative to the number of analyzed passwords, not total number of passwords

[*] Length:
[+]                        10: 100% (2013695)

[*] Character-set:
[+]             loweralphanum: 41% (836160)
[+]                   numeric: 23% (478196)
[+]                loweralpha: 20% (416939)
[+]      loweralphaspecialnum: 02% (59911)
[+]         loweralphaspecial: 02% (55761)
[+]             mixedalphanum: 02% (54198)
[+]             upperalphanum: 02% (47430)
[+]                upperalpha: 00% (19723)
[+]                mixedalpha: 00% (15460)
[+]                       all: 00% (9015)
[+]         mixedalphaspecial: 00% (6856)
[+]                specialnum: 00% (6685)
[+]      upperalphaspecialnum: 00% (3698)
[+]         upperalphaspecial: 00% (3459)
[+]                   special: 00% (204)

[*] Password complexity:
[+]                     digit: min(0) max(10)
[+]                     lower: min(0) max(10)
[+]                     upper: min(0) max(10)
[+]                   special: min(0) max(10)

[*] Simple Masks:
[+]               stringdigit: 37% (750938)
[+]                     digit: 23% (478196)
[+]                    string: 22% (452122)
[+]               digitstring: 03% (78963)
[+]                 othermask: 03% (67762)
[+]         stringdigitstring: 02% (59783)
[+]       stringspecialstring: 01% (33173)
[+]        stringspecialdigit: 01% (25293)
[+]             stringspecial: 01% (22207)
[+]          digitstringdigit: 00% (17290)
[+]        stringdigitspecial: 00% (12563)
[+]      specialstringspecial: 00% (3463)
[+]        digitspecialstring: 00% (2406)
[+]             specialstring: 00% (1773)
[+]        digitstringspecial: 00% (1621)
[+]        specialstringdigit: 00% (1468)
[+]        specialdigitstring: 00% (1225)
[+]         digitspecialdigit: 00% (1185)
[+]              digitspecial: 00% (1183)
[+]       specialdigitspecial: 00% (515)
[+]              specialdigit: 00% (362)
[+]                   special: 00% (204)

[*] Advanced Masks:
[+]      ?d?d?d?d?d?d?d?d?d?d: 23% (478196)
[+]      ?l?l?l?l?l?l?l?l?l?l: 20% (416939)
[+]      ?l?l?l?l?l?l?l?l?d?d: 10% (213109)
[+]      ?l?l?l?l?l?l?d?d?d?d: 07% (160592)
[+]      ?l?l?l?l?l?l?l?l?l?d: 06% (129823)
[+]      ?l?l?l?l?l?l?l?d?d?d: 04% (87611)
[+]      ?l?l?l?l?d?d?d?d?d?d: 01% (33277)
```

## policygen Usage Example

Generate Hashcat masks with a length of 8 (`–length=8`) and containing at least 1 uppercase letter (`–minupper 1`) and at least 1 digit (`–mindigit 1`), saving the masks to a file (`-o complexity.hcmask`):

```
root@kali:~# policygen --length=8 --minupper 1 --mindigit 1 -o complexity.hcmask
[*] Password policy:
[+] Password length: 8
[+] Minimum strength: lower: 0, upper: 1, digits: 1, special: 0
[+] Maximum strength: lower: 8, upper: 8, digits: 8, special: 8
[*] Total Masks:  65536 Runtime: [76d|1834h|110078m|6604680s]
[*] Policy Masks: 52670 Runtime: [40d|977h|58659m|3519568s]
root@kali:~# head complexity.hcmask
?l?l?l?l?l?l?u?d
?l?l?l?l?l?l?d?u
?l?l?l?l?l?u?l?d
?l?l?l?l?l?u?u?d
?l?l?l?l?l?u?d?l
?l?l?l?l?l?u?d?u
?l?l?l?l?l?u?d?d
?l?l?l?l?l?u?d?s
?l?l?l?l?l?u?s?d
?l?l?l?l?l?d?l?u
```
