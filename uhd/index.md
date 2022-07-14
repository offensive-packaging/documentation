---
Title: uhd
Homepage: https://www.ettus.com/sdr-software/uhd-usrp-hardware-driver/
Repository: https://salsa.debian.org/bottoms/pkg-uhd
Architectures: any all
Version: 4.1.0.5-3
Metapackages: kali-linux-everything kali-tools-rfid kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libuhd-dev
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package contains the header files for developing with libuhd.
  Doxygen generated documentation is in the uhd-host package.
 
 **Installed size:** `1.04 MB`  
 **How to install:** `sudo apt install libuhd-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libuhd4.1.0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.1.0
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
 
 **Installed size:** `13.17 MB`  
 **How to install:** `sudo apt install libuhd4.1.0`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-chrono1.74.0 
 * libboost-filesystem1.74.0 
 * libboost-serialization1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libpython3.10 
 * libstdc++6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.1.0-dpdk
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package is built with the Data Plane Development Kit and has additional
  dependencies and system configuration requirements to use those features.
 
 **Installed size:** `13.34 MB`  
 **How to install:** `sudo apt install libuhd4.1.0-dpdk`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-chrono1.74.0 
 * libboost-filesystem1.74.0 
 * libboost-serialization1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libpython3.10 
 * librte-eal21 
 * librte-ethdev21 
 * librte-hash21 
 * librte-mbuf21 
 * librte-mempool21 
 * librte-ring21 
 * libstdc++6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libuhd4.1.0-dpdk-tests
 
  Network tests for the Universal Hardware Driver for Ettus Research products.
   
  This package is built with the Data Plane Development Kit and has additional
  dependencies and system configuration requirements to use those features.
 
 **Installed size:** `1012 KB`  
 **How to install:** `sudo apt install libuhd4.1.0-dpdk-tests`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-filesystem1.74.0 
 * libboost-program-options1.74.0 
 * libc6 
 * libgcc-s1 
 * librte-eal21 
 * librte-ethdev21 
 * librte-hash21 
 * librte-mbuf21 
 * librte-mempool21 
 * librte-net21 
 * librte-ring21 
 * libstdc++6 
 * libuhd4.1.0-dpdk 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-uhd
 
  Host library for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package contains the Python API support for Python3.
 
 **Installed size:** `3.01 MB`  
 **How to install:** `sudo apt install python3-uhd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libpython3.10 
 * libstdc++6 
 * libuhd4.1.0 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 * python3-ruamel.yaml
 {{< /spoiler >}}
 
 ##### usrp_update_fs
 
 Wrapper for uhd_images_downloader for embedded UHD devices.
 
 ```
 root@kali:~# usrp_update_fs -h
 ERROR: Could not import MPM.
 usage: usrp_update_fs [-h] [--image IMAGE] [-y] [-m MANIFEST] -d DEVICE_TYPE
                       [-t GIT_TAG]
 
 USRP filesystem update If run without any options, it will reset the
 filesystem to the state it was originally in, but with the same version
 ("factory reset"). By using -m or -t, the precise version of the new
 filesystem can be selected. -t master will update to the very latest
 filesystem image. Most options require access to the internet to download the
 latest manifest and/or filesystem image.
 
 options:
   -h, --help            show this help message and exit
   --image IMAGE         Binary image of the filesystem update. If this is
                         given, all other options are ignored. Can be a file or
                         a URL
   -y, --yes             Answer questions with yes
   -m MANIFEST, --manifest MANIFEST
                         Manifest source. Can be a file or a URL. Overwrites -t
   -d DEVICE_TYPE, --device-type DEVICE_TYPE
                         Specify/overwrite device type (DANGER! May brick
                         device if used incorrectly!)
   -t GIT_TAG, --git-tag GIT_TAG
                         Will try and locate the given git tag or branch and
                         get the corresponding manifest. Ignored when -m is
                         given. Using this requires internet access.
 ```
 
 - - -
 
 ### uhd-doc
 
  Detailed documentation for the Universal Hardware Driver.
   
  This package includes the Doxygen generated documentation.
 
 **Installed size:** `29.39 MB`  
 **How to install:** `sudo apt install uhd-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-mathjax
 {{< /spoiler >}}
 
 
 - - -
 
 ### uhd-host
 
  Host utilities for the Universal Hardware Driver for Ettus Research products.
   
  The supported devices provide analog radio receiver and transmitter hardware
  along with digital interfaces for getting signals to and from a software
  defined radio running on the host computer.
   
  This package includes the uhd_find_devices application to locate and
  configure attached peripherals, the uhd_usrp_probe application to
  display hardware configuration information and Doxygen generated
  documentation.
 
 **Installed size:** `20.48 MB`  
 **How to install:** `sudo apt install uhd-host`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-filesystem1.74.0 
 * libboost-program-options1.74.0 
 * libboost-test1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * libncurses6 
 * libstdc++6 
 * libtinfo6 
 * libuhd4.1.0 
 * python3
 * python3-numpy 
 * python3-numpy-abi9
 * python3-requests
 {{< /spoiler >}}
 
 ##### rfnoc_image_builder
 
 Build UHD image using RFNoC blocks.
 
 ```
 root@kali:~# rfnoc_image_builder -h
 usage: rfnoc_image_builder [-h] (-y YAML_CONFIG | -r GRC_CONFIG) [-F FPGA_DIR]
                            [-o IMAGE_CORE_OUTPUT] [-x ROUTER_HEX_OUTPUT]
                            [-I INCLUDE_DIR] [-b GRC_BLOCKS] [-l LOG_LEVEL]
                            [--generate-only] [-d DEVICE] [-n IMAGE_CORE_NAME]
                            [-t TARGET] [-g] [-c] [-p VIVADO_PATH]
 
 Build UHD image using RFNoC blocks
 
 options:
   -h, --help            show this help message and exit
   -y YAML_CONFIG, --yaml-config YAML_CONFIG
                         Path to yml configuration file
   -r GRC_CONFIG, --grc-config GRC_CONFIG
                         Path to grc file to generate config from
   -F FPGA_DIR, --fpga-dir FPGA_DIR
                         Path to directory for the FPGA source tree. Defaults
                         to the FPGA source tree of the current repo.
   -o IMAGE_CORE_OUTPUT, --image-core-output IMAGE_CORE_OUTPUT
                         Path to where to save the image core Verilog source.
                         Defaults to the directory of the YAML file, filename
                         <DEVICE>_rfnoc_image_core.v
   -x ROUTER_HEX_OUTPUT, --router-hex-output ROUTER_HEX_OUTPUT
                         Path to where to save the static router hex file.
                         Defaults to the directory of the YAML file, filename
                         <DEVICE>_static_router.hex
   -I INCLUDE_DIR, --include-dir INCLUDE_DIR
                         Path directory of the RFNoC Out-of-Tree module
   -b GRC_BLOCKS, --grc-blocks GRC_BLOCKS
                         Path directory of GRC block descriptions (needed for
                         --grc-config only)
   -l LOG_LEVEL, --log-level LOG_LEVEL
                         Adjust log level
   --generate-only       Just generate files without building IP
   -d DEVICE, --device DEVICE
                         Device to be programmed [x300, x310, e310, e320, n300,
                         n310, n320, x410]. Needs to be specified either here,
                         or in the configuration file.
   -n IMAGE_CORE_NAME, --image_core_name IMAGE_CORE_NAME
                         Name to use for the RFNoC image core.Defaults to the
                         device name.
   -t TARGET, --target TARGET
                         Build target (e.g. X310_HG, N320_XG, ...). Needs to be
                         specified either here, on the configuration file.
   -g, --GUI             Open Vivado GUI during the FPGA building process
   -c, --clean-all       Cleans the IP before a new build
   -p VIVADO_PATH, --vivado-path VIVADO_PATH
                         Path to the base install for Xilinx Vivado if not in
                         default location (e.g., /tools/Xilinx/Vivado).
 ```
 
 - - -
 
 ##### uhd_adc_self_cal
 
 Invoke calibration in some UHD devices.
 
 ```
 root@kali:~# uhd_adc_self_cal --help
 UHD ADC self calibration Allowed options:
   --help                help message
   --version             print the version string and exit
   --args arg            device address args
 
 ```
 
 - - -
 
 ##### uhd_cal_rx_iq_balance
 
 Generate RX IQ Balance Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_rx_iq_balance --help
 USRP Generate RX IQ Balance Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            Device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --tx_offset arg (=934400)             TX LO offset from the RX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_cal_tx_dc_offset
 
 Generate TX DC Offset Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_tx_dc_offset --help
 USRP Generate TX DC Offset Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_freq arg (=507123)          Transmit wave frequency in Hz
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --rx_offset arg (=934400)             RX LO offset from the TX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_cal_tx_iq_balance
 
 Generate TX IQ Balance Calibration Table for a UHD Device
 
 ```
 root@kali:~# uhd_cal_tx_iq_balance --help
 USRP Generate TX IQ Balance Calibration Table Allowed options:
   --help                                help message
   --verbose                             enable some verbose
   --args arg                            device address args [default = ""]
   --subdev arg                          Subdevice specification (default: first
                                         subdevice, often 'A')
   --tx_wave_freq arg (=507123)          Transmit wave frequency in Hz
   --tx_wave_ampl arg (=0.69999999999999996)
                                         Transmit wave amplitude
   --rx_offset arg (=934400)             RX LO offset from the TX LO in Hz
   --freq_start arg                      Frequency start in Hz (do not specify 
                                         for default)
   --freq_stop arg                       Frequency stop in Hz (do not specify 
                                         for default)
   --freq_step arg (=7300000)            Step size for LO sweep in Hz
   --nsamps arg                          Samples per data capture
   --precision arg (=0.0001)             Correction precision (default=0.0001)
 
 This application measures leakage between RX and TX on a transceiver daughterboard to self-calibrate.
 Note: Not all daughterboards support this feature. Refer to the UHD manual for details.
 
 ```
 
 - - -
 
 ##### uhd_config_info
 
 USRP Hardware Driver Build Configuration Info
 
 ```
 root@kali:~# uhd_config_info --help
 UHD Config Info - Allowed Options:
   --build-date          Print build date
   --c-compiler          Print C compiler
   --cxx-compiler        Print C++ compiler
   --c-flags             Print C compiler flags
   --cxx-flags           Print C++ compiler flags
   --enabled-components  Print built-time enabled components
   --install-prefix      Print install prefix
   --boost-version       Print Boost version
   --libusb-version      Print libusb version
   --pkg-path            Print pkg path
   --lib-path            Print library path
   --images-dir          Print images dir
   --abi-version         Print ABI version string
   --print-all           Print everything
   --version             Print this UHD build's version
   --help                Print help message
 
 ```
 
 - - -
 
 ##### uhd_find_devices
 
 USRP Hardware Driver Discovery Utility
 
 ```
 root@kali:~# uhd_find_devices --help
 UHD Find Devices Allowed options:
   --help                help message
   --args arg            device address args
 
 ```
 
 - - -
 
 ##### uhd_image_loader
 
 UHD Image Loader
 
 ```
 root@kali:~# uhd_image_loader --help
 UHD Image Loader
 
 Load firmware and/or FPGA images onto an Ettus Research device.
 
 Allowed options:
   --help                help message
   --args arg            Device args, optional loader args
   --fw-path arg         Firmware path (uses default if none specified)
   --fpga-path arg       FPGA path (uses default if none specified)
   --out-path arg        Output path/filename of the downloaded FPGA .bit file
   --no-fw               Don't burn firmware
   --no-fpga             Don't Burn FPGA
   --download            Download an image to a bit/bin file
 
 ```
 
 - - -
 
 ##### uhd_images_downloader
 
 USRP Hardware Driver firmware/FPGA downloader
 
 ```
 root@kali:~# uhd_images_downloader -h
 usage: uhd_images_downloader [-h] [-t TYPES] [-i INSTALL_LOCATION]
                              [-m MANIFEST_LOCATION] [-I INVENTORY_LOCATION]
                              [-l] [--url-only] [--buffer-size BUFFER_SIZE]
                              [--download-limit DOWNLOAD_LIMIT]
                              [--http-proxy HTTP_PROXY] [-b BASE_URL] [-k] [-T]
                              [-y] [-n] [--refetch] [-V] [-q] [-v]
 
 Download image files required for USRPs. Usage: The `uhd_images_downloader`
 should work, "out of the box", with no command line arguments. Assuming your
 computer has an internet connection to [files.ettus.com], simply run the
 utility every time you update UHD, and the installed images for your devices
 should always be up to date. Images will be downloaded on a per-target basis.
 That is, there are image packages for a desired device and configuration.
 Users can specify which image packages they would plan to use. To see a list
 of available targets, run `uhd_images_downloader --list-targets`. The left
 column of the printout will be a list of available image archives. From there,
 you can construct a regular expression which matches to the targets you wish
 to download. For example, in order to download all image packages related to
 the X300 product line, users may run `uhd_images_downloader --types x3.*`. The
 `uhd_images_downloader` uses a manifest to look-up the URLs of image packages
 to download. Downloaded images are recorded in an inventory file that lives in
 the images install location. This allows the downloader to skip images that
 were previously downloaded, and haven't changed since. Manifests are built
 into the downloader, but can also be accessed at uhd/images/manifest.txt.
 Inventory files are JSON files called `inventory.json`, by default. It is
 possible to specify the inventory file in command line arguments, but we don't
 recommend using this functionality unless you're really sure you need it.
 
 options:
   -h, --help            show this help message and exit
   -t TYPES, --types TYPES
                         RegEx to select image sets from the manifest file.
                         (default: None)
   -i INSTALL_LOCATION, --install-location INSTALL_LOCATION
                         Set custom install location for images (default: None)
   -m MANIFEST_LOCATION, --manifest-location MANIFEST_LOCATION
                         Set custom location for the manifest file (default:
                         None)
   -I INVENTORY_LOCATION, --inventory-location INVENTORY_LOCATION
                         Set custom location for the inventory file (default:
                         None)
   -l, --list-targets    Print targets in the manifest file to stdout, and
                         exit. To get relative paths only, specify an empty
                         base URL (-b ''). (default: False)
   --url-only            With -l, only print the URLs, nothing else. (default:
                         False)
   --buffer-size BUFFER_SIZE
                         Set download buffer size (default: 8192)
   --download-limit DOWNLOAD_LIMIT
                         Set threshold for download limits. Any download larger
                         than this will require approval, either interactively,
                         or by providing --yes. (default: 104857600)
   --http-proxy HTTP_PROXY
                         Specify HTTP(S) proxy in the format
                         http[s]://user:pass@1.2.3.4:port If this this option
                         is not given, the environment variables
                         HTTP_PROXY/HTTPS_PROXY can also be used to specify a
                         proxy. (default: None)
   -b BASE_URL, --base-url BASE_URL
                         Set base URL for images download location. Defaults to
                         $UHD_IMAGES_URL if set, or
                         https://files.ettus.com/binaries/cache/ otherwise.
                         (default: None)
   -k, --keep            Keep the downloaded images archives in the image
                         directory (default: False)
   -T, --test            Verify the downloaded archives before extracting them
                         (default: False)
   -y, --yes             Answer all questions with 'yes' (for scripting
                         purposes). (default: False)
   -n, --dry-run         Print selected target without actually downloading
                         them. (default: False)
   --refetch             Ignore the inventory file and download all images.
                         (default: False)
   -V, --version         show program's version number and exit
   -q, --quiet           Decrease verbosity level (default: 0)
   -v, --verbose         Increase verbosity level (default: 0)
 ```
 
 - - -
 
 ##### uhd_usrp_probe
 
 USRP Hardware Driver Peripheral Report Utility
 
 ```
 root@kali:~# uhd_usrp_probe --help
 UHD USRP Probe Allowed options:
   --help                      help message
   --version                   print the version string and exit
   --args arg                  device address args
   --tree                      specify to print a complete property tree
   --string arg                query a string value from the property tree
   --double arg                query a double precision floating point value 
                               from the property tree
   --int arg                   query a integer value from the property tree
   --sensor arg                query a sensor value from the property tree
   --range arg                 query a range (gain, bandwidth, frequency, ...)  
                               from the property tree
   --vector                    when querying a string, interpret that as 
                               std::vector
   --init-only                 skip all queries, only initialize device
   --interactive-reg-iface arg RFNoC devices only: Spawn a shell to 
                               interactively peek and poke registers on RFNoC 
                               blocks
 
 ```
 
 - - -
 
 ##### usrp2_card_burner
 
 USRP N-Series FPGA/Firmware Burner
 
 ```
 root@kali:~# usrp2_card_burner -h
 Usage: usrp2_card_burner [options]
 
 Options:
   -h, --help   show this help message and exit
   --dev=DEV    raw device path
   --fw=FW      firmware image path (optional)
   --fpga=FPGA  fpga image path (optional)
   --list       list possible raw devices
   --force      override safety check
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
