---
Title: sleuthkit
Homepage: http://www.sleuthkit.org/sleuthkit
Repository: https://salsa.debian.org/pkg-security-team/sleuthkit
Architectures: any
Version: 4.11.1+dfsg-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libtsk-dev
 
  The Sleuth Kit, also known as TSK, is a collection of UNIX-based command
  line file and volume system forensic analysis tools. The filesystem tools
  allow you to examine filesystems of a suspect computer in a non-intrusive
  fashion. Because the tools do not rely on the operating system to process the
  filesystems, deleted and hidden content is shown.
   
  The volume system (media management) tools allow you to examine the layout of
  disks and other media. You can also recover deleted files, get information
  stored in slack spaces, examine filesystems journal, see partitions layout on
  disks or images etc. But is very important clarify that the TSK acts over the
  current filesystem only.
   
  The Sleuth Kit supports DOS partitions, BSD partitions (disk labels), Mac
  partitions, Sun slices (Volume Table of Contents), and GPT disks. With these
  tools, you can identify where partitions are located and extract them so that
  they can be analyzed with filesystem analysis tools.
   
  Currently, TSK supports several filesystems, as NTFS, FAT, exFAT, HFS+, Ext3,
  Ext4, UFS and YAFFS2.
   
  This package contains header files and static version of the library.
 
 **Installed size:** `2.57 MB`  
 **How to install:** `sudo apt install libtsk-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libtsk19 
 * zlib1g-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libtsk19
 
  The Sleuth Kit, also known as TSK, is a collection of UNIX-based command
  line file and volume system forensic analysis tools. The filesystem tools
  allow you to examine filesystems of a suspect computer in a non-intrusive
  fashion. Because the tools do not rely on the operating system to process the
  filesystems, deleted and hidden content is shown.
   
  The volume system (media management) tools allow you to examine the layout of
  disks and other media. You can also recover deleted files, get information
  stored in slack spaces, examine filesystems journal, see partitions layout on
  disks or images etc. But is very important clarify that the TSK acts over the
  current filesystem only.
   
  The Sleuth Kit supports DOS partitions, BSD partitions (disk labels), Mac
  partitions, Sun slices (Volume Table of Contents), and GPT disks. With these
  tools, you can identify where partitions are located and extract them so that
  they can be analyzed with filesystem analysis tools.
   
  Currently, TSK supports several filesystems, as NTFS, FAT, exFAT, HFS+, Ext3,
  Ext4, UFS and YAFFS2.
   
  This package contains the library which can be used to implement all of the
  functionality of the command line tools into an application that needs to
  analyze data from a disk image.
 
 **Installed size:** `1.09 MB`  
 **How to install:** `sudo apt install libtsk19`  
 
 {{< spoiler "Dependencies:" >}}
 * libafflib0v5 
 * libc6 
 * libewf2 
 * libgcc-s1 
 * libsqlite3-0 
 * libstdc++6 
 * libvhdi1 
 * libvmdk1 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### sleuthkit
 
  The Sleuth Kit, also known as TSK, is a collection of UNIX-based command
  line file and volume system forensic analysis tools. The filesystem tools
  allow you to examine filesystems of a suspect computer in a non-intrusive
  fashion. Because the tools do not rely on the operating system to process the
  filesystems, deleted and hidden content is shown.
   
  The volume system (media management) tools allow you to examine the layout of
  disks and other media. You can also recover deleted files, get information
  stored in slack spaces, examine filesystems journal, see partitions layout on
  disks or images etc. But is very important clarify that the TSK acts over the
  current filesystem only.
   
  The Sleuth Kit supports DOS partitions, BSD partitions (disk labels), Mac
  partitions, Sun slices (Volume Table of Contents), and GPT disks. With these
  tools, you can identify where partitions are located and extract them so that
  they can be analyzed with filesystem analysis tools.
   
  Currently, TSK supports several filesystems, as NTFS, FAT, exFAT, HFS+, Ext3,
  Ext4, UFS and YAFFS2.
   
  This package contains the set of command line tools in The Sleuth Kit.
 
 **Installed size:** `1.56 MB`  
 **How to install:** `sudo apt install sleuthkit`  
 
 {{< spoiler "Dependencies:" >}}
 * file
 * libafflib0v5 
 * libc6 
 * libdate-manip-perl
 * libewf2 
 * libgcc-s1 
 * libstdc++6 
 * libtsk19 
 * libvhdi1 
 * libvmdk1 
 * perl
 {{< /spoiler >}}
 
 ##### blkcalc
 
 Converts between unallocated disk unit numbers and regular disk unit numbers.
 
 ```
 root@kali:~# blkcalc -h
 blkcalc: invalid option -- 'h'
 Invalid argument: (null)
 usage: blkcalc [-dsu unit_addr] [-vV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] image [images]
 Slowly calculates the opposite block number
 	One of the following must be given:
 	  -d: The given address is from a 'dd' image 
 	  -s: The given address is from a 'blkls -s' (slack) image
 	  -u: The given address is from a 'blkls' (unallocated) image
 	-f fstype: The file system type (use '-f list' for supported types)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### blkcat
 
 Display the contents of file system data unit in a disk image.
 
 ```
 root@kali:~# blkcat --help
 blkcat: invalid option -- '-'
 Invalid argument: --help
 usage: blkcat [-ahsvVw] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] [-u usize] image [images] unit_addr [num]
 	-a: displays in all ASCII 
 	-h: displays in hexdump-like fashion
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-f fstype: File system type (use '-f list' for supported types)
 	-s: display basic block stats such as unit size, fragments, etc.
 	-v: verbose output to stderr
 	-V: display version
 	-w: displays in web-like (html) fashion
 	-u usize: size of each data unit in image (for raw, blkls, swap)
 	[num] is the number of data units to display (default is 1)
 ```
 
 - - -
 
 ##### blkls
 
 List or output file system data units.
 
 ```
 root@kali:~# blkls -h
 blkls: invalid option -- 'h'
 Invalid argument: (null)
 usage: blkls [-aAelvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] image [images] [start-stop]
 	-e: every block (including file system metadata blocks)
 	-l: print details in time machine list format
 	-a: Display allocated blocks
 	-A: Display unallocated blocks
 	-f fstype: File system type (use '-f list' for supported types)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-s: print slack space only (other flags are ignored
 	-v: verbose to stderr
 	-V: print version
 ```
 
 - - -
 
 ##### blkstat
 
 Display details of a file system data unit (i.e. block or sector)
 
 ```
 root@kali:~# blkstat -h
 blkstat: invalid option -- 'h'
 Invalid argument: (null)
 usage: blkstat [-vV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] image [images] addr
 	-f fstype: File system type (use '-f list' for supported types)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: Verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### fcat
 
 Output the contents of a file based on its name.
 
 ```
 root@kali:~# fcat --help
 fcat: invalid option -- '-'
 Invalid argument: --help
 usage: fcat [-hRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] file_path image [images]
 	-h: Do not display holes in sparse files
 	-R: Suppress recovery errors
 	-s: Display slack space at end of file
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: verbose to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### ffind
 
 Finds the name of the file or directory using a given inode
 
 ```
 root@kali:~# ffind -h
 ffind: invalid option -- 'h'
 Invalid argument: (null)
 usage: ffind [-aduvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] image [images] inode
 	-a: Find all occurrences
 	-d: Find deleted entries ONLY
 	-u: Find undeleted entries ONLY
 	-f fstype: Image file system type (use '-f list' for supported types)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: Verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### fiwalk
 
 Print the filesystem statistics and exit
 
 ```
 root@kali:~# fiwalk -h
 usage: fiwalk [options] iso-name
 Default behavior: Just print the file system statistics and exit.
 options:
     -c config.txt   read config.txt for metadata extraction tools
     -C nn           only process nn files, then do a clean exit
 
 include/exclude parameters; may be repeated. 
     -n pattern  = only match files for which the filename matches
                   the pattern.
               example: -n .jpeg -n .jpg will find all JPEG files
               Case is ignored. Will not match orphan files.
     
 Ways to make this program run faster:
     -I ignore NTFS system files
     -g just report the file objects - don't get the data
     -O only walk allocated files
     -b do not report byte runs if data not accessed
     -z do not calculate MD5 or SHA1 values
     -Gnn - Only process the contents of files smaller than nn gigabytes (default 2)
            (Specify -G0 to remove space restrictions)
 
 Ways to make this program run slower:
     -M = Report MD5 for each file (default on)
     -1 = Report SHA1 for each file (default on)
     -S nnnn = Perform sector hashes every nnnn bytes
     -f = Report the output of the 'file' command for each
 
 Output options:
     -m = Output in SleuthKit 'Body file' format
     -A<file> = ARFF output to <file>
     -X<file> = XML output to a <file> (full DTD)
          -X0 = Write output to filename.xml
     -Z       = zap (erase) the output file
     -x       = XML output to stdout (no DTD)
     -T<file> = Walkfile output to <file>
     -a <audit.txt> = Read the scalpel audit.txt file
 
 Misc:
     -d = debug this program
     -v = Enable SleuthKit verbose flag
 
 SleuthKit Version: 4.11.1
 AFFLIB Version:    3.7.19
 LIBEWF Version:    20140813
 ```
 
 - - -
 
 ##### fls
 
 List file and directory names in a disk image.
 
 ```
 root@kali:~# fls --help
 fls: invalid option -- '-'
 Invalid argument: --help
 usage: fls [-adDFlhpruvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-m dir/] [-o imgoffset] [-z ZONE] [-s seconds] image [images] [inode]
 	If [inode] is not given, the root directory is used
 	-a: Display "." and ".." entries
 	-d: Display deleted entries only
 	-D: Display only directories
 	-F: Display only files
 	-l: Display long version (like ls -l)
 	-i imgtype: Format of image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-m: Display output in mactime input format with
 	      dir/ as the actual mount point of the image
 	-h: Include MD5 checksum hash in mactime output
 	-o imgoffset: Offset into image file (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-S snap_id: Snapshot ID (for APFS only)
 	-p: Display full path for each file
 	-r: Recurse on directory entries
 	-u: Display undeleted entries only
 	-v: verbose output to stderr
 	-V: Print version
 	-z: Time zone of original machine (i.e. EST5EDT or GMT) (only useful with -l)
 	-s seconds: Time skew of original machine (in seconds) (only useful with -l & -m)
 	-k password: Decryption password for encrypted volumes
 ```
 
 - - -
 
 ##### fsstat
 
 Display general details of a file system
 
 ```
 root@kali:~# fsstat -h
 fsstat: invalid option -- 'h'
 Invalid argument: (null)
 usage: fsstat [-tvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image
 	-t: display type only
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: verbose output to stderr
 	-V: Print version
 	-k password: Decryption password for encrypted volumes
 ```
 
 - - -
 
 ##### hfind
 
 Lookup a hash value in a hash database
 
 ```
 root@kali:~# hfind -h
 hfind: invalid option -- 'h'
 usage: hfind [-eqVa] [-c] [-f lookup_file] [-i db_type] db_file [hashes]
 	-e: Extended mode - where values other than just the name are printed
 	-q: Quick mode - where a 1 is printed if it is found, else 0
 	-V: Print version to STDOUT
 	-c db_name: Create new database with the given name.
 	-a: Add given hashes to the database.
 	-f lookup_file: File with one hash per line to lookup
 	-i db_type: Create index file for a given hash database type
 	db_file: The path of the hash database, must have .kdb extension for -c option
 	[hashes]: hashes to lookup (STDIN is used otherwise)
 
 	Supported index types: nsrl-md5, nsrl-sha1, md5sum, encase, hk
 ```
 
 - - -
 
 ##### icat
 
 Output the contents of a file based on its inode number.
 
 ```
 root@kali:~# icat --help
 icat: invalid option -- '-'
 Invalid argument: --help
 usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
 	-h: Do not display holes in sparse files
 	-r: Recover deleted file
 	-R: Recover deleted file and suppress recovery errors
 	-s: Display slack space at end of file
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-S snap_id: Snapshot ID (for APFS only)
 	-v: verbose to stderr
 	-V: Print version
 	-k password: Decryption password for encrypted volumes
 ```
 
 - - -
 
 ##### ifind
 
 Find the meta-data structure that has allocated a given disk unit or file name.
 
 ```
 root@kali:~# ifind -h
 ifind: invalid option -- 'h'
 Invalid argument: (null)
 usage: ifind [-alvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] [-d unit_addr] [-n file] [-p par_addr] [-z ZONE] image [images]
 	-a: find all inodes
 	-d unit_addr: Find the meta data given the data unit
 	-l: long format when -p is given
 	-n file: Find the meta data given the file name
 	-p par_addr: Find UNALLOCATED MFT entries given the parent's meta address (NTFS only)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: Verbose output to stderr
 	-V: Print version
 	-z ZONE: Time zone setting when -l -p is given
 ```
 
 - - -
 
 ##### ils
 
 List inode information
 
 ```
 root@kali:~# ils -h
 ils: invalid option -- 'h'
 Invalid argument: (null)
 usage: ils [-emOpvV] [-aAlLzZ] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] [-s seconds] image [images] [inum[-end]]
 	-e: Display all inodes
 	-m: Display output in the mactime format
 	-O: Display inodes that are unallocated, but were sill open (UFS/ExtX only)
 	-p: Display orphan inodes (unallocated with no file name)
 	-s seconds: Time skew of original machine (in seconds)
 	-a: Allocated inodes
 	-A: Unallocated inodes
 	-l: Linked inodes
 	-L: Unlinked inodes
 	-z: Unused inodes
 	-Z: Used inodes
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-v: verbose output to stderr
 	-V: Display version number
 ```
 
 - - -
 
 ##### img_cat
 
 Output contents of an image file.
 
 ```
 root@kali:~# img_cat -h
 img_cat: invalid option -- 'h'
 Invalid argument: (null)
 usage: img_cat [-vV] [-i imgtype] [-b dev_sector_size] [-s start_sector] [-e stop_sector] image
 	-i imgtype: The format of the image file (use 'i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-s start_sector: The sector number to start at
 	-e stop_sector:  The sector number to stop at
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### img_stat
 
 Display details of an image file
 
 ```
 root@kali:~# img_stat -h
 img_stat: invalid option -- 'h'
 Invalid argument: (null)
 usage: img_stat [-tvV] [-i imgtype] [-b dev_sector_size] image
 	-t: display type only
 	-i imgtype: The format of the image file (use '-i list' for list of supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### istat
 
 Display details of a meta-data structure (i.e. inode)
 
 ```
 root@kali:~# istat -h
 istat: invalid option -- 'h'
 Invalid argument: (null)
 usage: istat [-N num] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-P pooltype] [-B pool_volume_block] [-z zone] [-s seconds] [-rvV] image inum
 	-N num: force the display of NUM address of block pointers
 	-r: display run list instead of list of block addresses
 	-z zone: time zone of original machine (i.e. EST5EDT or GMT)
 	-s seconds: Time skew of original machine (in seconds)
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-P pooltype: Pool container type (use '-p list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-S snap_id: Snapshot ID (for APFS only)
 	-v: verbose output to stderr
 	-V: print version
 	-k password: Decryption password for encrypted volumes
 ```
 
 - - -
 
 ##### jcat
 
 Show the contents of a block in the file system journal.
 
 ```
 root@kali:~# jcat -h
 jcat: invalid option -- 'h'
 Invalid argument: (null)
 usage: jcat [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-vV] image [images] [inode] blk
 	blk: The journal block to view
 	inode: The file system inode where the journal is located
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-v: verbose output to stderr
 	-V: print version
 ```
 
 - - -
 
 ##### jls
 
 List the contents of a file system journal
 
 ```
 root@kali:~# jls -h
 jls: invalid option -- 'h'
 Invalid argument: (null)
 usage: jls [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-vV] image [inode]
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-v: verbose output to stderr
 	-V: print version
 ```
 
 - - -
 
 ##### jpeg_extract
 
 Jpeg extractor
 
 ```
 root@kali:~# jpeg_extract --help
 Usage--exif-[OPTION...]-file
 ---v,---version-------------------Display-software-version
 ---i,---ids-----------------------Show-IDs-instead-of-tag-names
 ---t,---tag=tag-------------------Select-tag
 --------ifd=IFD-------------------Select-IFD
 ---l,---list-tags-----------------List-all-EXIF-tags
 ---|,---show-mnote----------------Show-contents-of-tag-MakerNote
 --------remove--------------------Remove-tag-or-ifd
 ---s,---show-description----------Show-description-of-tag
 ---e,---extract-thumbnail---------Extract-thumbnail
 ---r,---remove-thumbnail----------Remove-thumbnail
 ---n,---insert-thumbnail=FILE-----Insert-FILE-as-thumbnail
 --------no-fixup------------------Do-not-fix-existing-tags-in-files
 ---o,---output=FILE---------------Write-data-to-FILE
 --------set-value=STRING----------Value-of-tag
 ---c,---create-exif---------------Create-EXIF-data-if-not-existing
 ---m,---machine-readable----------Output-in-a-machine-readable--tab-delimited-
 ----------------------------------format
 ---w,---width=WIDTH---------------Width-of-output
 ---x,---xml-output----------------Output-in-a-XML-format
 ---d,---debug---------------------Show-debugging-messages
 
 Help-options-
 ---?,---help----------------------Show-this-help-message
 --------usage---------------------Display-brief-usage-message
 ```
 
 - - -
 
 ##### mactime
 
 Create an ASCII time line of file activity
 
 ```
 root@kali:~# man mactime
 MACTIME(1)                  General Commands Manual                 MACTIME(1)
 
 NAME
        mactime - Create an ASCII time line of file activity
 
 SYNOPSIS
        mactime  [-b body ] [-g group file ] [-p password file ] [-i (day|hour)
        index file ] [-dhmVy] [-z TIME_ZONE ] [DATE_RANGE]
 
 DESCRIPTION
        mactime creates an ASCII time line of file activity based on  the  body
        file specified by '-b' or from STDIN.  The time line is written to STD-
        OUT.  The body file must be in the time machine format that is  created
        by 'ils -m', 'fls -m', or the mac-robber tool.
 
 ARGUMENTS
        -b body
               Specify  the  location of a body file.  This file must be gener-
               ated by a tool such as 'fls -m' or 'ils -m'.   The  'mac-robber'
               and 'grave-robber' tools can also be used to generate the file.
 
        -g group file
               Specify  the  location  of the group file.  mactime will display
               the group name instead of the GID if this is given.
 
        -p password file
               Specify the location of the passwd file.  mactime  will  display
               the user name instead of the UID of this is given.
 
        -i day|hour index file
               Specify  the  location  of an index file to write to.  The first
               argument specifies the granularity, either an hourly summary  or
               daily.  If the '-d' flag is given, then the summary will be sep-
               arated by a ',' to import into a spread sheet.
 
        -d     Display timeline and index  files  in  comma  delimited  format.
               This  is used to import the data into a spread sheet for presen-
               tations or graphs.
 
        -h     Display header info about the session including time range,  in-
               put source, and passwd or group files.
 
        -V     Display version to STDOUT.
 
        -m     The  month  is  given as a number instead of name (does not work
               with -y).
 
        -y     The date is displayed in ISO8601 format.
 
        -z TIME_ZONE
               The timezone from where the data was  collected.   The  name  of
               this  argument  is  system  dependent (examples include EST5EDT,
               GMT+1).  Does not work with -y.
 
        -z list
               List valid timezones.
 
        DATE_RANGE
               The range of dates to make the time line for.  The standard for-
               mat is yyyy-mm-dd for a starting date and no ending date. For an
               ending date, use yyyy-mm-dd..yyyy-mm-dd.  Date can contain time,
               use format yyyy-mm-ddThh:mm:ss for starting and/or ending date.
 
 LICENSE
        The changes from mactime in TCT and mac-daddy are distributed under the
        Common Public License, found in the cpl1.0.txt file in the  The  Sleuth
        Kit licenses directory.
 
 HISTORY
        A version of mactime first appeared in The Coroner's Toolkit (TCT) (Dan
        Farmer) and later mac-daddy (Rob Lee).
 
 AUTHOR
        Brian Carrier <carrier at sleuthkit dot org>
 
        Send documentation updates to <doc-updates at sleuthkit dot org>
 
                                                                     MACTIME(1)
 ```
 
 - - -
 
 ##### mmcat
 
 Output the contents of a partition to stdout
 
 ```
 root@kali:~# man mmcat
 MMCAT(1)                    General Commands Manual                   MMCAT(1)
 
 NAME
        mmcat - Output the contents of a partition to stdout
 
 SYNOPSIS
        mmcat  [-t  mmtype  ]  [-o offset ] [ -i imgtype ] [-b dev_sector_size]
        [-vV] image [images] part_num
 
 DESCRIPTION
        mmcat outputs the contents of a specific volume to stdout.  This allows
        you to extract the contents of a partition to a separate file.
 
 ARGUMENTS
        -t mmtype
               Specify  the  media  management type.  Use '-t list' to list the
               supported types.  If not given, autodetection methods are used.
 
        -o offset
               Specify the offset into the image where  the  volume  containing
               the  partition system starts.  The relative offset of the parti-
               tion system will be added to this value.
 
        -b dev_sector_size
               The size, in bytes, of the underlying device  sectors.   If  not
               given,  the  value in the image format is used (if it exists) or
               512-bytes is assumed.
 
        -i imgtype
               Identify the type of image file, such as raw.  Use '-i list'  to
               list  the  supported types.  If not given, autodetection methods
               are used.
 
        -v     Verbose output of debugging statements to stderr
 
        -V     Display version
 
        image [images]
               The disk or partition image to read, whose format is given  with
               '-i'.   Multiple  image  file names can be given if the image is
               split into multiple segments.  If only one image file is  given,
               and  its  name is the first in a sequence (e.g., as indicated by
               ending in '.001'), subsequent image segments  will  be  included
               automatically.
 
        part_num
               Address  of partition to process.  See the mmls output to deter-
               mine the address of the partitions.
 
 AUTHOR
        Brian Carrier <carrier at sleuthkit dot org>
 
        Send documentation updates to <doc-updates at sleuthkit dot org>
 
                                                                       MMCAT(1)
 ```
 
 - - -
 
 ##### mmls
 
 Display the partition layout of a volume system (partition tables)
 
 ```
 root@kali:~# man mmls
 MMLS(1)                     General Commands Manual                    MMLS(1)
 
 NAME
        mmls  - Display the partition layout of a volume system  (partition ta-
        bles)
 
 SYNOPSIS
        mmls [-t mmtype ] [-o offset ] [  -i  imgtype  ]  [-b  dev_sector_size]
        [-BrvV] [-aAmM] image [images]
 
 DESCRIPTION
        mmls  displays  the  layout of the partitions in a volume system, which
        include partition tables and disk labels.
 
 ARGUMENTS
        -t mmtype
               Specify the media management type.  Use '-t list'  to  list  the
               supported types.  If not given, autodetection methods are used.
 
        -o offset
               Specify  the  offset  into the image where the volume containing
               the partition system starts.  The relative offset of the  parti-
               tion system will be added to this value.
 
        -b dev_sector_size
               The  size,  in  bytes, of the underlying device sectors.  If not
               given, the value in the image format is used (if it  exists)  or
               512-bytes is assumed.
 
        -i imgtype
               Identify  the type of image file, such as raw.  Use '-i list' to
               list the supported types.  If not given,  autodetection  methods
               are used.
 
        -B     Include a column with the partition sizes in bytes
 
        -r     Recurse into DOS partitions and look for other partition tables.
               This setup frequently occurs when Unix is installed on x86  sys-
               tems.
 
        -v     Verbose output of debugging statements to stderr
 
        -V     Display version
 
        -a     Show allocated volumes
 
        -A     Show unallocated volumes
 
        -m     Show metadata volumes
 
        -M     Hide metadata volumes
 
        image [images]
               The  disk or partition image to read, whose format is given with
               '-i'.  Multiple image file names can be given if  the  image  is
               split  into multiple segments.  If only one image file is given,
               and its name is the first in a sequence (e.g., as  indicated  by
               ending  in  '.001'),  subsequent image segments will be included
               automatically.
 
        'mmls' is similar to 'fdisk -lu'  in  Linux  with  a  few  differences.
        Namely, it will show which sectors are not being used so that those can
        be searched for hidden data.  It also gives the length value so that it
        can be plugged into 'dd' more easily for extracting the partitions.  It
        also will show BSD disk labels for Free, Open, and NetBSD and will dis-
        play the output in sectors and not cylinders.  Lastly, it works on non-
        Linux systems.
 
        If none of -a, -A, -m, or -M are given then all volume  types  will  be
        listed.  If any of them are given, then only the types specified on the
        command line will be listed.
 
        Allocated volumes are those that are listed in a partition table in the
        volume  system  AND  can store data.  Unallocated volumes are virtually
        created by mmls to show you which sectors have not been allocated to  a
        volume.   The  metadata  volumes  overlap the allocated and unallocated
        volumes and describe where the  partition  tables  and  other  metadata
        structures  are  located.  In some volume systems, these structures are
        in allocated space and in others they are  in  unallocated  space.   In
        some  volume  systems, their location is explicitly given in the parti-
        tion tables and in others they are not.
 
 EXAMPLES
        To list the partition table of a Windows system using autodetect:
 
        # mmls disk_image.dd
 
        To list the contents of a BSD system that starts in sector 12345  of  a
        split image:
 
        # mmls -t bsd -o 12345 -i split disk-1.dd disk-2.dd
 
 AUTHOR
        Brian Carrier <carrier at sleuthkit dot org>
 
                                                                        MMLS(1)
 ```
 
 - - -
 
 ##### mmstat
 
 Display details about the volume system (partition tables)
 
 ```
 root@kali:~# man mmstat
 MMSTAT(1)                   General Commands Manual                  MMSTAT(1)
 
 NAME
        mmstat - Display details about the volume system (partition tables)
 
 SYNOPSIS
        mmstat  [-t  mmtype  ] [-o offset ] [ -i imgtype ] [-b dev_sector_size]
        [-vV] image [images]
 
 DESCRIPTION
        mmstat displays the general details of a volume system, which  includes
        partition tables and disk labels.  Mainly, the type is given.
 
 ARGUMENTS
        -t mmtype
               Specify  the  media  management type.  Use '-t list' to list the
               supported types.  If not given, autodetection methods are used.
 
        -o offset
               Specify the offset into the image where  the  volume  containing
               the  partition system starts.  The relative offset of the parti-
               tion system will be added to this value.
 
        -b dev_sector_size
               The size, in bytes, of the underlying device  sectors.   If  not
               given,  the  value in the image format is used (if it exists) or
               512-bytes is assumed.
 
        -i imgtype
               Identify the type of image file, such as raw.  Use '-i list'  to
               list  the  supported types.  If not given, autodetection methods
               are used.
 
        -v     Verbose output of debugging statements to stderr
 
        -V     Display version
 
        image [images]
               The disk or partition image to read, whose format is given  with
               '-i'.   Multiple  image  file names can be given if the image is
               split into multiple segments.  If only one image file is  given,
               and  its  name is the first in a sequence (e.g., as indicated by
               ending in '.001'), subsequent image segments  will  be  included
               automatically.
 
 AUTHOR
        Brian Carrier <carrier at sleuthkit dot org>
 
        Send documentation updates to <doc-updates at sleuthkit dot org>
 
                                                                      MMSTAT(1)
 ```
 
 - - -
 
 ##### pstat
 
 
 ```
 root@kali:~# pstat -h
 pstat: invalid option -- 'h'
 Invalid argument: (null)
 usage: pstat [-tvV] [-p pooltype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image
 	-t: display type only
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### sigfind
 
 Find a binary signature in a file
 
 ```
 root@kali:~# man sigfind
 SIGFIND(1)                  General Commands Manual                 SIGFIND(1)
 
 NAME
        sigfind - Find a binary signature in a file
 
 SYNOPSIS
        sigfind [-b bsize ] [-o offset ] [-t template ] [-lV] [ hex_signature ]
        file
 
 DESCRIPTION
        sigfind searches through a file and looks for the  hex_signature  at  a
        given  offset.   This  can be used to search for lost boot sectors, su-
        perblocks, and partition tables.
 
 ARGUMENTS
        -b bsize
               Specify the block size in which to search.  The default  is  512
               and the value must be a multiple of 512.
 
        -o offset
               Specify the offset in a block in which the signature must exist.
               The default is 0.
 
        -t template
               Specify a template name that defines  the  signature  value  and
               offset.   Run  with  no  options to get a list of supported tem-
               plates.
 
        -l     The signature is  stored  in  little-endian  ordering  and  must
               therefore be reversed.
 
        -V     Display version
 
        [hex_signature]
               The  binary  signature  that  you are searching for.  It must be
               given in hexadecimal format.  This argument must exist if -t  is
               not used.
 
        file   Any raw data.
 
 EXAMPLES
        sigfind -o 510 -l AA55 disk.dd
 
        sigfind -t fat disk.dd
 
 AUTHOR
        Brian Carrier <carrier at sleuthkit dot org>
 
        Send documentation updates to <doc-updates at sleuthkit dot org>
 
                                                                     SIGFIND(1)
 ```
 
 - - -
 
 ##### sorter
 
 Sort files in an image into categories based on file type
 
 ```
 root@kali:~# sorter -h
 Missing image argument
 
 sorter [-b size] [-E] [-e] [-h]  [-l] [-md5] [-s] [-sha1] [-U] [-v] [-V] [-a hash_alert] [-c config] [-C config] [-d dir] [-m mnt] [-n nsrl_db] [-x hash_exclude] [-o imgoffset] [-f fstype] [-i imgtype] image [images] [dir_meta_addr] 
 
     -b size: Minimum size.  Ignore files smaller than 'size'
 	-E: Perform category indexing only (no extension checks - was '-i')
 	-e: Perform extension checks only (no category index files)
 	-h: HTML Format
 	-l: List index to STDOUT (no files are ever written)
 	-md5: Print the MD5 value with the index output
 	-s: Save files to category directories
 	-sha1: Print the SHA-1 value with the index output
 	-U: Ignore the unknown category - only save catgories in config files
 	-v: verbose debugging output
 	-V: print version information
 	-a hash_alert: hash database of hashes to alert on
 	-c config: specify a config file to use (in addition to default files)
 	   NOTE: This config file has priority over default files
 	-C config: specify the ONLY config file to use
 	-d dir: Save category index files in the specified directory
 	-f fstype: file system type (Sleuth Kit types) of image
 	-i imgtype: Format of image file
 	-o imgoffset: Offset of file system in image (in sectors)
 	-m mnt: The mounting point of the image
 	-n nsrl_db: The NIST NSRL database file (NSRLFile.txt) (hashes to ignore)
 	-x hash_exclude: hash database of hashes to ignore
 	dir_meta_addr: Address of directory to start analyzing from 
 	image: image to analyze
 ```
 
 - - -
 
 ##### srch_strings
 
 Display printable strings in files
 
 ```
 root@kali:~# srch_strings -h
 Usage: srch_strings [option(s)] [file(s)]
  Display printable strings in [file(s)] (stdin by default)
  The options are:
   -a -                 Scan the entire file, not just the data section
   -f       Print the name of the file before each string
   -n number       Locate & print any NUL-terminated sequence of at
   -<number>                 least [number] characters (default 4).
   -t {o,x,d}        Print the location of the string in base 8, 10 or 16
   -o                        An alias for --radix=o
   -e {s,S,b,l,B,L} Select character size and endianness:
                             s = 7-bit, S = 8-bit, {b,l} = 16-bit, {B,L} = 32-bit
   -h                  Display this information
   -v               Print the program's version number
 ```
 
 - - -
 
 ##### tsk_comparedir
 
 Compare the contents of a directory with the contents of an image or local device.
 
 ```
 root@kali:~# tsk_comparedir -h
 tsk_comparedir: invalid option -- 'h'
 Invalid argument: (null)
 usage: tsk_comparedir [-f fstype] [-i imgtype] [-b dev_sector_size] [-o sector_offset] [-P pooltype] [-B pool_volume_block] [-n start_inum] [-vV] image [image] comparison_directory
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: The file system type (use '-f list' for supported types)
 	-o sector_offset: sector offset for file system to compare
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-n start_inum: inum for directory in image file to start compare at
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### tsk_gettimes
 
 Collect MAC times from a disk image into a body file.
 
 ```
 root@kali:~# tsk_gettimes -h
 tsk_gettimes: invalid option -- 'h'
 Invalid argument: (null)
 usage: tsk_gettimes [-vVm] [-i imgtype] [-b dev_sector_size] [-z zone] [-s seconds] image [image]
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-m: Calculate MD5 hash in output (slow)
 	-v: verbose output to stderr
 	-V: Print version
 	-z: Time zone of original machine (i.e. EST5EDT or GMT) (only useful with -l)
 	-s seconds: Time skew of original machine (in seconds) (only useful with -l & -m)
 ```
 
 - - -
 
 ##### tsk_imageinfo
 
 
 ```
 root@kali:~# tsk_imageinfo -h
 tsk_imageinfo: invalid option -- 'h'
 Invalid argument: (null)
 usage: tsk_imageinfo [-vV] [-i imgtype] [-b dev_sector_size] image
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-v: verbose output to stderr
 	-V: Print version
 ```
 
 - - -
 
 ##### tsk_loaddb
 
 Populate a SQLite database with metadata from a disk image
 
 ```
 root@kali:~# tsk_loaddb --help
 tsk_loaddb: invalid option -- '-'
 Invalid argument: --help
 usage: tsk_loaddb [-ahkvV] [-i imgtype] [-b dev_sector_size] [-d database] [-z ZONE] image [image]
 	-a: Add image to existing database, instead of creating a new one (requires -d to specify database)
 	-k: Don't create block data table
 	-h: Calculate hash values for the files
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-d database: Path for the database (default is the same directory as the image, with name derived from image name)
 	-v: verbose output to stderr
 	-V: Print version
 	-z: Time zone of original machine (i.e. EST5EDT or GMT)
 ```
 
 - - -
 
 ##### tsk_recover
 
 Export files from an image into a local directory
 
 ```
 root@kali:~# tsk_recover -h
 tsk_recover: invalid option -- 'h'
 Invalid argument: (null)
 usage: tsk_recover [-vVae] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o sector_offset] [-P pooltype] [-B pool_volume_block] [-d dir_inum] image [image] output_dir
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: The file system type (use '-f list' for supported types)
 	-v: verbose output to stderr
 	-V: Print version
 	-a: Recover allocated files only
 	-e: Recover all files (allocated and unallocated)
 	-o sector_offset: sector offset for a volume to recover (recovers only that volume)
 	-P pooltype: Pool container type (use '-P list' for supported types)
 	-B pool_volume_block: Starting block (for pool volumes only)
 	-d dir_inum: Directory inum to recover from (must also specify a specific partition using -o or there must not be a volume system)
 ```
 
 - - -
 
 ##### usnjls
 
 List the contents of a NTFS Update Sequence Number journal
 
 ```
 root@kali:~# usnjls -h
 usnjls: invalid option -- 'h'
 Invalid argument: (null)
 usage: usnjls [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-lmvV] image [inode]
 	-i imgtype: The format of the image file (use '-i list' for supported types)
 	-b dev_sector_size: The size (in bytes) of the device sectors
 	-f fstype: File system type (use '-f list' for supported types)
 	-o imgoffset: The offset of the file system in the image (in sectors)
 	-l: Long output format with detailed information
 	-m: Time machine output format
 	-v: verbose output to stderr
 	-V: print version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
