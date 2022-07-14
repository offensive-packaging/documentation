---
Title: cryptsetup
Homepage: https://gitlab.com/cryptsetup/cryptsetup
Repository: https://salsa.debian.org/cryptsetup-team/cryptsetup
Architectures: linux-any all
Version: 2:2.4.3-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-tools-post-exploitation kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cryptsetup
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  Cryptsetup is backwards compatible with the on-disk format of cryptoloop,
  but also supports more secure formats. This package includes support for
  automatically configuring encrypted devices at boot time via the config
  file /etc/crypttab. Additional features are cryptoroot support through
  initramfs-tools and several supported ways to read a passphrase or key.
   
  This package provides the cryptdisks_start and _stop wrappers, as well as
  luksformat.
 
 **Installed size:** `448 KB`  
 **How to install:** `sudo apt install cryptsetup`  
 
 {{< spoiler "Dependencies:" >}}
 * cryptsetup-bin 
 * debconf  | debconf-2.0
 * dmsetup
 * libc6 
 * libcryptsetup12 
 * libjson-c5 
 * libssh-4 
 {{< /spoiler >}}
 
 ##### cryptdisks_start
 
 Wrapper around cryptsetup that parses /etc/crypttab.
 
 ```
 root@kali:~# cryptdisks_start -h
 Usage: /usr/sbin/cryptdisks_start [-r|--readonly] <name> [.. <name>]
 
 reads /etc/crypttab and starts the mapping corresponding to <name>
 ```
 
 - - -
 
 ##### cryptdisks_stop
 
 Wrapper around cryptsetup that parses /etc/crypttab.
 
 ```
 root@kali:~# cryptdisks_stop -h
 Stopping crypto disk...-h (stopped)...done.
 ```
 
 - - -
 
 ##### luksformat
 
 Create and format an encrypted LUKS device
 
 ```
 root@kali:~# luksformat -h
 luksformat - Create and format an encrypted LUKS device
 Usage: luksformat [-t <file system>] <device> [ mkfs options ]
 
 ```
 
 - - -
 
 ### cryptsetup-bin
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  This package provides cryptsetup, cryptsetup-reencrypt, integritysetup
  and veritysetup.
 
 **Installed size:** `2.11 MB`  
 **How to install:** `sudo apt install cryptsetup-bin`  
 
 {{< spoiler "Dependencies:" >}}
 * libblkid1 
 * libc6 
 * libcryptsetup12 
 * libjson-c5 
 * libpopt0 
 * libssh-4 
 * libuuid1 
 {{< /spoiler >}}
 
 ##### cryptsetup
 
 Manage plain dm-crypt and LUKS encrypted volumes
 
 ```
 root@kali:~# cryptsetup --help
 cryptsetup 2.4.3
 Usage: cryptsetup [OPTION...] <action> <action-specific>
 
 Help options:
   -?, --help                            Show this help message
       --usage                           Display brief usage
   -V, --version                         Print package version
       --active-name=STRING              Override device autodetection of dm
                                         device to be reencrypted
       --align-payload=SECTORS           Align payload at <n> sector boundaries
                                         - for luksFormat
       --allow-discards                  Allow discards (aka TRIM) requests for
                                         device
   -q, --batch-mode                      Do not ask for confirmation
       --cancel-deferred                 Cancel a previously set deferred
                                         device removal
   -c, --cipher=STRING                   The cipher used to encrypt the disk
                                         (see /proc/crypto)
       --debug                           Show debug messages
       --debug-json                      Show debug messages including JSON
                                         metadata
       --deferred                        Device removal is deferred until the
                                         last user closes it
       --device-size=bytes               Use only specified device size (ignore
                                         rest of device). DANGEROUS!
       --decrypt                         Decrypt LUKS2 device (remove
                                         encryption).
       --disable-external-tokens         Disable loading of external LUKS2
                                         token plugins
       --disable-keyring                 Disable loading volume keys via kernel
                                         keyring
       --disable-locks                   Disable locking of on-disk metadata
       --disable-veracrypt               Do not scan for VeraCrypt compatible
                                         device
       --dump-json-metadata              Dump info in JSON format (LUKS2 only)
       --dump-master-key                 Dump volume (master) key instead of
                                         keyslots info
       --encrypt                         Encrypt LUKS2 device (in-place
                                         encryption).
       --force-password                  Disable password quality check (if
                                         enabled)
   -h, --hash=STRING                     The hash used to create the encryption
                                         key from the passphrase
       --header=STRING                   Device or file with separated LUKS
                                         header
       --header-backup-file=STRING       File with LUKS header and keyslots
                                         backup
       --hotzone-size=bytes              Maximal reencryption hotzone size.
       --init-only                       Initialize LUKS2 reencryption in
                                         metadata only.
   -I, --integrity=STRING                Data integrity algorithm (LUKS2 only)
       --integrity-legacy-padding        Use inefficient legacy padding (old
                                         kernels)
       --integrity-no-journal            Disable journal for integrity device
       --integrity-no-wipe               Do not wipe device after format
   -i, --iter-time=msecs                 PBKDF iteration time for LUKS (in ms)
       --iv-large-sectors                Use IV counted in sector size (not in
                                         512 bytes)
       --json-file=STRING                Read or write the json from or to a
                                         file
       --key-description=STRING          Key description
   -d, --key-file=STRING                 Read the key from a file
   -s, --key-size=BITS                   The size of the encryption key
   -S, --key-slot=INT                    Slot number for new key (default is
                                         first free)
       --keyfile-offset=bytes            Number of bytes to skip in keyfile
   -l, --keyfile-size=bytes              Limits the read from keyfile
       --keyslot-cipher=STRING           LUKS2 keyslot: The cipher used for
                                         keyslot encryption
       --keyslot-key-size=BITS           LUKS2 keyslot: The size of the
                                         encryption key
       --label=STRING                    Set label for the LUKS2 device
       --luks2-keyslots-size=bytes       LUKS2 header keyslots area size
       --luks2-metadata-size=bytes       LUKS2 header metadata area size
       --master-key-file=STRING          Read the volume (master) key from file.
       --new-keyfile-offset=bytes        Number of bytes to skip in newly added
                                         keyfile
       --new-keyfile-size=bytes          Limits the read from newly added
                                         keyfile
   -o, --offset=SECTORS                  The start offset in the backend device
       --pbkdf=STRING                    PBKDF algorithm (for LUKS2): argon2i,
                                         argon2id, pbkdf2
       --pbkdf-force-iterations=LONG     PBKDF iterations cost (forced,
                                         disables benchmark)
       --pbkdf-memory=kilobytes          PBKDF memory cost limit
       --pbkdf-parallel=threads          PBKDF parallel cost
       --perf-no_read_workqueue          Bypass dm-crypt workqueue and process
                                         read requests synchronously
       --perf-no_write_workqueue         Bypass dm-crypt workqueue and process
                                         write requests synchronously
       --perf-same_cpu_crypt             Use dm-crypt same_cpu_crypt
                                         performance compatibility option
       --perf-submit_from_crypt_cpus     Use dm-crypt submit_from_crypt_cpus
                                         performance compatibility option
       --persistent                      Set activation flags persistent for
                                         device
       --priority=STRING                 Keyslot priority: ignore, normal,
                                         prefer
       --progress-frequency=secs         Progress line update (in seconds)
   -r, --readonly                        Create a readonly mapping
       --reduce-device-size=bytes        Reduce data device size (move data
                                         offset). DANGEROUS!
       --refresh                         Refresh (reactivate) device with new
                                         parameters
       --resilience=STRING               Reencryption hotzone resilience type
                                         (checksum,journal,none)
       --resilience-hash=STRING          Reencryption hotzone checksums hash
       --resume-only                     Resume initialized LUKS2 reencryption
                                         only.
       --sector-size=INT                 Encryption sector size (default: 512
                                         bytes)
       --serialize-memory-hard-pbkdf     Use global lock to serialize memory
                                         hard PBKDF (OOM workaround)
       --shared                          Share device with another
                                         non-overlapping crypt segment
   -b, --size=SECTORS                    The size of the device
   -p, --skip=SECTORS                    How many sectors of the encrypted data
                                         to skip at the beginning
       --subsystem=STRING                Set subsystem label for the LUKS2
                                         device
       --tcrypt-backup                   Use backup (secondary) TCRYPT header
       --tcrypt-hidden                   Use hidden header (hidden TCRYPT
                                         device)
       --tcrypt-system                   Device is system TCRYPT drive (with
                                         bootloader)
       --test-args                       Do not run action, just validate all
                                         command line parameters
       --test-passphrase                 Do not activate device, just check
                                         passphrase
   -t, --timeout=secs                    Timeout for interactive passphrase
                                         prompt (in seconds)
       --token-id=INT                    Token number (default: any)
       --token-only                      Do not ask for passphrase if
                                         activation by token fails
       --token-type=STRING               Restrict allowed token types used to
                                         retrieve LUKS2 key
   -T, --tries=INT                       How often the input of the passphrase
                                         can be retried
   -M, --type=STRING                     Type of device metadata: luks, luks1,
                                         luks2, plain, loopaes, tcrypt, bitlk
       --unbound                         Create or dump unbound (no assigned
                                         data segment) LUKS2 keyslot
       --use-random                      Use /dev/random for generating volume
                                         key
       --use-urandom                     Use /dev/urandom for generating volume
                                         key
       --uuid=STRING                     UUID for device to use
       --veracrypt                       Scan also for VeraCrypt compatible
                                         device
       --veracrypt-pim=INT               Personal Iteration Multiplier for
                                         VeraCrypt compatible device
       --veracrypt-query-pim             Query Personal Iteration Multiplier
                                         for VeraCrypt compatible device
   -v, --verbose                         Shows more detailed error messages
   -y, --verify-passphrase               Verifies the passphrase by asking for
                                         it twice
 
 <action> is one of:
 	open <device> [--type <type>] [<name>] - open device as <name>
 	close <name> - close device (remove mapping)
 	resize <name> - resize active device
 	status <name> - show device status
 	benchmark [--cipher <cipher>] - benchmark cipher
 	repair <device> - try to repair on-disk metadata
 	reencrypt <device> - reencrypt LUKS2 device
 	erase <device> - erase all keyslots (remove encryption key)
 	convert <device> - convert LUKS from/to LUKS2 format
 	config <device> - set permanent configuration options for LUKS2
 	luksFormat <device> [<new key file>] - formats a LUKS device
 	luksAddKey <device> [<new key file>] - add key to LUKS device
 	luksRemoveKey <device> [<key file>] - removes supplied key or key file from LUKS device
 	luksChangeKey <device> [<key file>] - changes supplied key or key file of LUKS device
 	luksConvertKey <device> [<key file>] - converts a key to new pbkdf parameters
 	luksKillSlot <device> <key slot> - wipes key with number <key slot> from LUKS device
 	luksUUID <device> - print UUID of LUKS device
 	isLuks <device> - tests <device> for LUKS partition header
 	luksDump <device> - dump LUKS partition information
 	tcryptDump <device> - dump TCRYPT device information
 	bitlkDump <device> - dump BITLK device information
 	luksSuspend <device> - Suspend LUKS device and wipe key (all IOs are frozen)
 	luksResume <device> - Resume suspended LUKS device
 	luksHeaderBackup <device> - Backup LUKS device header and keyslots
 	luksHeaderRestore <device> - Restore LUKS device header and keyslots
 	token <add|remove|import|export> <device> - Manipulate LUKS2 tokens
 
 You can also use old <action> syntax aliases:
 	open: create (plainOpen), luksOpen, loopaesOpen, tcryptOpen, bitlkOpen
 	close: remove (plainClose), luksClose, loopaesClose, tcryptClose, bitlkClose
 
 <name> is the device to create under /dev/mapper
 <device> is the encrypted device
 <key slot> is the LUKS key slot number to modify
 <key file> optional key file for the new key for luksAddKey action
 
 Default compiled-in metadata format is LUKS2 (for luksFormat action).
 
 LUKS2 external token plugin support is compiled-in.
 LUKS2 external token plugin path: /lib/x86_64-linux-gnu/cryptsetup.
 
 Default compiled-in key and passphrase parameters:
 	Maximum keyfile size: 8192kB, Maximum interactive passphrase length 512 (characters)
 Default PBKDF for LUKS1: pbkdf2, iteration time: 2000 (ms)
 Default PBKDF for LUKS2: argon2id
 	Iteration time: 2000, Memory required: 1048576kB, Parallel threads: 4
 
 Default compiled-in device cipher parameters:
 	loop-AES: aes, Key 256 bits
 	plain: aes-cbc-essiv:sha256, Key: 256 bits, Password hashing: ripemd160
 	LUKS: aes-xts-plain64, Key: 256 bits, LUKS header hashing: sha256, RNG: /dev/urandom
 	LUKS: Default keysize with XTS mode (two internal keys) will be doubled.
 ```
 
 - - -
 
 ##### cryptsetup-reencrypt
 
 Tool for offline LUKS device re-encryption
 
 ```
 root@kali:~# cryptsetup-reencrypt --help
 cryptsetup-reencrypt 2.4.3
 Usage: cryptsetup-reencrypt [OPTION...] <device>
 
 Help options:
   -?, --help                            Show this help message
       --usage                           Display brief usage
   -V, --version                         Print package version
   -q, --batch-mode                      Do not ask for confirmation
   -B, --block-size=MiB                  Reencryption block size
   -c, --cipher=STRING                   The cipher used to encrypt the disk
                                         (see /proc/crypto)
       --debug                           Show debug messages
       --decrypt                         Permanently decrypt device (remove
                                         encryption)
       --device-size=bytes               Use only specified device size (ignore
                                         rest of device). DANGEROUS!
   -h, --hash=STRING                     The hash used to create the encryption
                                         key from the passphrase
       --header=STRING                   Device or file with separated LUKS
                                         header
   -i, --iter-time=msecs                 PBKDF iteration time for LUKS (in ms)
       --keep-key                        Do not change key, no data area
                                         reencryption
   -d, --key-file=STRING                 Read the key from a file
   -s, --key-size=BITS                   The size of the encryption key
       --keyfile-offset=bytes            Number of bytes to skip in keyfile
   -l, --keyfile-size=bytes              Limits the read from keyfile
   -S, --key-slot=INT                    Use only this slot (others will be
                                         disabled)
       --master-key-file=STRING          Read new volume (master) key from file
   -N, --new                             Create new header on not encrypted
                                         device
       --pbkdf=STRING                    PBKDF algorithm (for LUKS2): argon2i,
                                         argon2id, pbkdf2
       --pbkdf-force-iterations=LONG     PBKDF iterations cost (forced,
                                         disables benchmark)
       --pbkdf-memory=kilobytes          PBKDF memory cost limit
       --pbkdf-parallel=threads          PBKDF parallel cost
       --progress-frequency=secs         Progress line update (in seconds)
       --reduce-device-size=bytes        Reduce data device size (move data
                                         offset). DANGEROUS!
   -T, --tries=INT                       How often the input of the passphrase
                                         can be retried
   -M, --type=STRING                     Type of LUKS metadata: luks1, luks2
       --use-directio                    Use direct-io when accessing devices
       --use-fsync                       Use fsync after each block
       --use-random                      Use /dev/random for generating volume
                                         key
       --use-urandom                     Use /dev/urandom for generating volume
                                         key
       --uuid=STRING                     The UUID used to resume decryption
   -v, --verbose                         Shows more detailed error messages
       --write-log                       Update log file after every block
 ```
 
 - - -
 
 ##### cryptsetup-ssh
 
 Manage LUKS2 SSH token
 
 ```
 root@kali:~# cryptsetup-ssh --help
 Usage: cryptsetup-ssh [OPTION...] <action> <device>
 Experimental cryptsetup plugin for unlocking LUKS2 devices with token connected
 to an SSH server
 
  Options for the 'add' action:
       --key-slot=NUM         Keyslot to assign the token to. If not specified,
                              token will be assigned to the first keyslot
                              matching provided passphrase.
       --ssh-keypath=STRING   Path to the SSH key for connecting to the remote
                              server
       --ssh-path=STRING      Path to the key file on the remote server
       --ssh-server=STRING    IP address/URL of the remote server for this token
                             
       --ssh-user=STRING      Username used for the remote server
 
  Generic options:
       --debug                Show debug messages
       --debug-json           Show debug messages including JSON metadata
   -v, --verbose              Shows more detailed error messages
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 This plugin currently allows only adding a token to an existing key slot.
 
 Specified SSH server must contain a key file on the specified path with a
 passphrase for an existing key slot on the device.
 Provided credentials will be used by cryptsetup to get the password when
 opening the device using the token.
 
 Note: The information provided when adding the token (SSH server address, user
 and paths) will be stored in the LUKS2 header in plaintext.
 ```
 
 - - -
 
 ##### integritysetup
 
 Manage dm-integrity (block level integrity) volumes
 
 ```
 root@kali:~# integritysetup --help
 integritysetup 2.4.3
 Usage: integritysetup [OPTION...] <action> <action-specific>
 
 Help options:
   -?, --help                                  Show this help message
       --usage                                 Display brief usage
   -V, --version                               Print package version
       --allow-discards                        Allow discards (aka TRIM)
                                               requests for device
   -q, --batch-mode                            Do not ask for confirmation
       --buffer-sectors=SECTORS                Buffers size
       --bitmap-flush-time=ms                  Bitmap mode flush time
       --bitmap-sectors-per-bit=INT            Number of 512-byte sectors per
                                               bit (bitmap mode).
       --cancel-deferred                       Cancel a previously set deferred
                                               device removal
       --data-device=path                      Path to data device (if
                                               separated)
       --debug                                 Show debug messages
       --deferred                              Device removal is deferred until
                                               the last user closes it
   -I, --integrity=STRING                      Data integrity algorithm
       --integrity-key-file=STRING             Read the integrity key from a
                                               file
       --integrity-key-size=BITS               The size of the data integrity
                                               key
       --integrity-legacy-padding              Use inefficient legacy padding
                                               (old kernels)
       --integrity-legacy-hmac                 Do not protect superblock with
                                               HMAC (old kernels)
       --integrity-legacy-recalculate          Allow recalculating of volumes
                                               with HMAC keys (old kernels)
   -D, --integrity-no-journal                  Disable journal for integrity
                                               device
       --interleave-sectors=SECTORS            Interleave sectors
       --journal-commit-time=ms                Journal commit time
       --journal-integrity=STRING              Journal integrity algorithm
       --journal-integrity-key-size=BITS       The size of the journal
                                               integrity key
       --journal-integrity-key-file=STRING     Read the journal integrity key
                                               from a file
       --journal-crypt=STRING                  Journal encryption algorithm
       --journal-crypt-key-file=STRING         Read the journal encryption key
                                               from a file
       --journal-crypt-key-size=BITS           The size of the journal
                                               encryption key
   -j, --journal-size=bytes                    Journal size
       --journal-watermark=percent             Journal watermark
       --no-wipe                               Do not wipe device after format
       --progress-frequency=secs               Progress line update (in seconds)
   -B, --integrity-bitmap-mode                 Use bitmap to track changes and
                                               disable journal for integrity
                                               device
       --integrity-recalculate                 Recalculate initial tags
                                               automatically.
       --integrity-recalculate-reset           Reset automatic recalculate
                                               position.
   -R, --integrity-recovery-mode               Recovery mode (no journal, no
                                               tag checking)
   -s, --sector-size=bytes                     Sector size
   -t, --tag-size=bytes                        Tag size (per-sector)
   -v, --verbose                               Shows more detailed error
                                               messages
 
 <action> is one of:
 	format <integrity_device> - format device
 	open <integrity_device> <name> - open device as <name>
 	close <name> - close device (remove mapping)
 	status <name> - show active device status
 	dump <integrity_device> - show on-disk information
 
 <name> is the device to create under /dev/mapper
 <integrity_device> is the device containing data with integrity tags
 
 Default compiled-in dm-integrity parameters:
 	Checksum algorithm: crc32c
 	Maximum keyfile size: 4kB
 ```
 
 - - -
 
 ##### veritysetup
 
 Manage dm-verity (block level verification) volumes
 
 ```
 root@kali:~# veritysetup --help
 veritysetup 2.4.3
 Usage: veritysetup [OPTION...] <action> <action-specific>
 
 Help options:
   -?, --help                           Show this help message
       --usage                          Display brief usage
   -V, --version                        Print package version
       --cancel-deferred                Cancel a previously set deferred device
                                        removal
       --check-at-most-once             Verify data block only the first time
                                        it is read
       --data-block-size=bytes          Block size on the data device
       --data-blocks=blocks             The number of blocks in the data file
       --debug                          Show debug messages
       --deferred                       Device removal is deferred until the
                                        last user closes it
       --fec-device=path                Path to device with error correction
                                        data
       --fec-offset=bytes               Starting offset on the FEC device
       --fec-roots=bytes                FEC parity bytes
       --format=number                  Format type (1 - normal, 0 - original
                                        Chrome OS)
   -h, --hash=string                    Hash algorithm
       --hash-block-size=bytes          Block size on the hash device
       --hash-offset=bytes              Starting offset on the hash device
       --ignore-corruption              Ignore corruption, log it only
       --ignore-zero-blocks             Do not verify zeroed blocks
       --no-superblock                  Do not use verity superblock
       --panic-on-corruption            Panic kernel if corruption is detected
       --restart-on-corruption          Restart kernel if corruption is detected
       --root-hash-file=STRING          Path to root hash file
       --root-hash-signature=STRING     Path to root hash signature file
   -s, --salt=hex string                Salt
       --uuid=STRING                    UUID for device to use
   -v, --verbose                        Shows more detailed error messages
 
 <action> is one of:
 	format <data_device> <hash_device> - format device
 	verify <data_device> <hash_device> [<root_hash>] - verify device
 	open <data_device> <name> <hash_device> [<root_hash>] - open device as <name>
 	close <name> - close device (remove mapping)
 	status <name> - show active device status
 	dump <hash_device> - show on-disk information
 
 <name> is the device to create under /dev/mapper
 <data_device> is the data device
 <hash_device> is the device containing verification data
 <root_hash> hash of the root node on <hash_device>
 
 Default compiled-in dm-verity parameters:
 	Hash: sha256, Data block (bytes): 4096, Hash block (bytes): 4096, Salt size: 32, Hash format: 1
 ```
 
 - - -
 
 ### cryptsetup-initramfs
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  This package provides initramfs integration for cryptsetup.
 
 **Installed size:** `141 KB`  
 **How to install:** `sudo apt install cryptsetup-initramfs`  
 
 {{< spoiler "Dependencies:" >}}
 * busybox | busybox-static
 * cryptsetup 
 * debconf  | debconf-2.0
 * initramfs-tools  | linux-initramfs-tool
 {{< /spoiler >}}
 
 
 - - -
 
 ### cryptsetup-run
 
  This is a transitional dummy package to get upgrading systems to install the
  cryptsetup package. It can safely be removed once no other package depends on
  it.
 
 **Installed size:** `70 KB`  
 **How to install:** `sudo apt install cryptsetup-run`  
 
 {{< spoiler "Dependencies:" >}}
 * cryptsetup 
 {{< /spoiler >}}
 
 
 - - -
 
 ### cryptsetup-suspend
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  This package provides suspend mode integration for cryptsetup. It takes
  care of removing LUKS master key from memory before system suspend.
   
  Please note that the suspend mode integration is limited to LUKS devices
  and requires systemd.  Moreover, this is an early implementation and may not
  be as mature as the other cryptsetup-* packages yet.
 
 **Installed size:** `117 KB`  
 **How to install:** `sudo apt install cryptsetup-suspend`  
 
 {{< spoiler "Dependencies:" >}}
 * cryptsetup-initramfs 
 * initramfs-tools-core
 * kbd
 * libc6 
 * libcryptsetup12 
 * systemd
 {{< /spoiler >}}
 
 
 - - -
 
 ### libcryptsetup-dev
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  This package provides the libcryptsetup development files.
 
 **Installed size:** `174 KB`  
 **How to install:** `sudo apt install libcryptsetup-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libcryptsetup12 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libcryptsetup12
 
  Cryptsetup provides an interface for configuring encryption on block
  devices (such as /home or swap partitions), using the Linux kernel
  device mapper target dm-crypt. It features integrated Linux Unified Key
  Setup (LUKS) support.
   
  This package provides the libcryptsetup shared library.
 
 **Installed size:** `553 KB`  
 **How to install:** `sudo apt install libcryptsetup12`  
 
 {{< spoiler "Dependencies:" >}}
 * libargon2-1 
 * libblkid1 
 * libc6 
 * libdevmapper1.02.1 
 * libjson-c5 
 * libssl1.1 
 * libuuid1 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
