---
Title: hackrf
Homepage: http://greatscottgadgets.com/hackrf/
Repository: https://salsa.debian.org/bottoms/pkg-hackrf
Architectures: any
Version: 2021.03.1-2
Metapackages: kali-linux-everything kali-linux-large kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hackrf
 
  HackRF is an open source Software Defined Radio that can receive
  and transmit between 30 MHz and 6 GHz. HackRF has a 20 MHz bandwidth.
  It is a High Speed USB device powered by the USB bus.
   
  This package contains a set of command line utilities:
   * hackrf_cpldjtag: program CLPD
   * hackrf_info: probe device and show configuration
   * hackrf_max2837: chip register read/write tool
   * hackrf_rffc5071: chip register read/write tool
   * hackrf_si5351c: chip register read/write tool
   * hackrf_spiflash: read and write flash data from file.
   * hackrf_transfer: file based transmit and receive sdr
 
 **Installed size:** `195 KB`  
 **How to install:** `sudo apt install hackrf`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfftw3-single3 
 * libhackrf0 
 {{< /spoiler >}}
 
 ##### hackrf_clock
 
 Clock configuration utility
 
 ```
 root@kali:~# hackrf_clock -h
 hackrf_clock - HackRF clock configuration utility
 Usage:
 	-h, --help: this help
 	-r, --read <clock_num>: read settings for clock_num
 	-a, --all: read settings for all clocks
 	-o, --clkout <clkout_enable>: enable/disable CLKOUT
 	-d, --device <serial_number>: Serial number of desired HackRF.
 
 Examples:
 	hackrf_clock -r 3 : prints settings for CLKOUT
 ```
 
 - - -
 
 ##### hackrf_cpldjtag
 
 Program CPLD
 
 ```
 root@kali:~# hackrf_cpldjtag -h
 Usage:
 	-h, --help: this help
 	-x, --xsvf <filename>: XSVF file to be written to CPLD.
 	-d, --device <serialnumber>: Serial number of device, if multiple devices
 ```
 
 - - -
 
 ##### hackrf_debug
 
 Register manipultion tool
 
 ```
 root@kali:~# hackrf_debug -h
 
 Usage:
 	-h, --help: this help
 	-n, --register <n>: set register number for read/write operations
 	-r, --read: read register specified by last -n argument, or all registers
 	-w, --write <v>: write register specified by last -n argument with value <v>
 	-c, --config: print SI5351C multisynth configuration information
 	-d, --device <s>: specify a particular device by serial number
 	-m, --max2837: target MAX2837
 	-s, --si5351c: target SI5351C
 	-f, --rffc5072: target RFFC5072
 	-u, --ui <1/0>: enable/disable UI
 
 Examples:
 	hackrf_debug --si5351c -n 0 -r     # reads from si5351c register 0
 	hackrf_debug --si5351c -c          # displays si5351c multisynth configuration
 	hackrf_debug --rffc5072 -r         # reads all rffc5072 registers
 	hackrf_debug --max2837 -n 10 -w 22 # writes max2837 register 10 with 22 decimal
 ```
 
 - - -
 
 ##### hackrf_info
 
 Probe device and show configuration
 
 ```
 root@kali:~# man hackrf_info
 hackrf_info(1)                   User Commands                  hackrf_info(1)
 
 NAME
        hackrf_info - probe device and show configuration
 
 DESCRIPTION
        The  HackRF project started by Michael Ossmann and Jared Boone to build
        software radio peripheral using Free Software and Free Hardware design.
        Care  was  taken to only use electronic components with published docu-
        mentation (no NDAs!) and  to  avoid  software  libraries  without  open
        source licenses.
 
        Jawbreaker  is  the first complete HackRF platform, a wideband software
        radio transceiver with a USB interface.
 
        This application lets the user probe the device and show configuration.
 
 SYNOPSIS
        hackrf_info
 
 OPTIONS
        none
 
 SEE ALSO
        Great   Scott   Gadgets   HackRF   web   page:    http://greatscottgad-
        gets.com/hackrf/
 
        Other hackrf programs:
 
        hackrf_cpldjtag(1),          hackrf_info(1),         hackrf_max2837(1),
        hackrf_rffc5071(1),       hackrf_si5351c(1),        hackrf_spiflash(1),
        hackrf_transfer(1)
 
 AUTHOR
        This manual page was written by Maitland Bottoms for the Debian project
        (but may be used by others).
 
 COPYRIGHT
        Copyright (c) 2013 A. Maitland Bottoms <bottoms@debian.org>
 
        This program is free software: you can redistribute it and/or modify it
        under  the  terms of the GNU General Public License as published by the
        Free Software Foundation, either version 2 of the License, or (at  your
        option) any later version.
 
        This  program  is  distributed  in the hope that it will be useful, but
        WITHOUT ANY  WARRANTY;  without  even  the  implied  warranty  of  MER-
        CHANTABILITY  or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General
        Public License for more details.
 
 HACKRF                             2013.07.1                    hackrf_info(1)
 ```
 
 - - -
 
 ##### hackrf_operacake
 
 Control of operacake board via hackrf
 
 ```
 root@kali:~# hackrf_operacake -h
 
 Usage:
 	-h, --help: this help
 	-d, --device <n>: specify a particular device by serial number
 	-o, --address <n>: specify a particular operacake by address [default: 0]
 	-m, --mode <mode>: specify switching mode [options: manual, frequency, time]
 	-a <n>: set port A connection
 	-b <n>: set port B connection
 	-f <port:min:max>: automatically assign <port> for range <min:max> in MHz
 	-t <port:dwell>: in time-switching mode, dwell on <port> for <dwell> samples. Specify only <port> to use the default dwell time (with -w). This argument can be repeated to specify a list of ports.
 	-w <n>: set default dwell time for time-switching mode	-l, --list: list available operacake boards
 	-g, --gpio_test: test GPIO functionality of an opera cake
 ```
 
 - - -
 
 ##### hackrf_spiflash
 
 Program Flash
 
 ```
 root@kali:~# hackrf_spiflash -h
 Usage:
 	-h, --help: this help
 	-a, --address <n>: starting address (default: 0)
 	-l, --length <n>: number of bytes to read (default: 1048576)
 	-r, --read <filename>: Read data into file.
 	-w, --write <filename>: Write data from file.
 	-i, --no-check: Skip check for firmware compatibility with target device.
 	-d, --device <serialnumber>: Serial number of device, if multiple devices
 	-s, --status: Read SPI flash status registers before other operations.
 	-c, --clear: Clear SPI flash status registers before other operations.
 	-R, --reset: Reset HackRF after other operations.
 	-v, --verbose: Verbose output.
 ```
 
 - - -
 
 ##### hackrf_sweep
 
 Control frequency sweep of hackrf
 
 ```
 root@kali:~# hackrf_sweep --help
 hackrf_sweep: invalid option -- '-'
 Usage:
 	[-h] # this help
 	[-d serial_number] # Serial number of desired HackRF
 	[-a amp_enable] # RX RF amplifier 1=Enable, 0=Disable
 	[-f freq_min:freq_max] # minimum and maximum frequencies in MHz
 	[-p antenna_enable] # Antenna port power, 1=Enable, 0=Disable
 	[-l gain_db] # RX LNA (IF) gain, 0-40dB, 8dB steps
 	[-g gain_db] # RX VGA (baseband) gain, 0-62dB, 2dB steps
 	[-w bin_width] # FFT bin width (frequency resolution) in Hz, 2445-5000000
 	[-1] # one shot mode
 	[-N num_sweeps] # Number of sweeps to perform
 	[-B] # binary output
 	[-I] # binary inverse FFT output
 	-r filename # output file
 
 Output fields:
 	date, time, hz_low, hz_high, hz_bin_width, num_samples, dB, dB, . . .
 ```
 
 - - -
 
 ##### hackrf_transfer
 
 File based transmit and receive sdr
 
 ```
 root@kali:~# hackrf_transfer -h
 Usage:
 	-h # this help
 	[-d serial_number] # Serial number of desired HackRF.
 	-r <filename> # Receive data into file (use '-' for stdout).
 	-t <filename> # Transmit data from file (use '-' for stdin).
 	-w # Receive data into file with WAV header and automatic name.
 	   # This is for SDR# compatibility and may not work with other software.
 	[-f freq_hz] # Frequency in Hz [0MHz to 7250MHz].
 	[-i if_freq_hz] # Intermediate Frequency (IF) in Hz [2150MHz to 2750MHz].
 	[-o lo_freq_hz] # Front-end Local Oscillator (LO) frequency in Hz [84MHz to 5400MHz].
 	[-m image_reject] # Image rejection filter selection, 0=bypass, 1=low pass, 2=high pass.
 	[-a amp_enable] # RX/TX RF amplifier 1=Enable, 0=Disable.
 	[-p antenna_enable] # Antenna port power, 1=Enable, 0=Disable.
 	[-l gain_db] # RX LNA (IF) gain, 0-40dB, 8dB steps
 	[-g gain_db] # RX VGA (baseband) gain, 0-62dB, 2dB steps
 	[-x gain_db] # TX VGA (IF) gain, 0-47dB, 1dB steps
 	[-s sample_rate_hz] # Sample rate in Hz (2-20MHz, default 10MHz).
 	[-n num_samples] # Number of samples to transfer (default is unlimited).
 	[-S buf_size] # Enable receive streaming with buffer size buf_size.
 	[-c amplitude] # CW signal source mode, amplitude 0-127 (DC value to DAC).
 	[-R] # Repeat TX mode (default is off) 
 	[-b baseband_filter_bw_hz] # Set baseband filter bandwidth in Hz.
 	Possible values: 1.75/2.5/3.5/5/5.5/6/7/8/9/10/12/14/15/20/24/28MHz, default <= 0.75 * sample_rate_hz.
 	[-C ppm] # Set Internal crystal clock error in ppm.
 	[-H hw_sync_enable] # Synchronise USB transfer using GPIO pins.
 ```
 
 - - -
 
 ### libhackrf-dev
 
  HackRF is an open source Software Defined Radio that can receive
  and transmit between 30 MHz and 6 GHz. HackRF has a 20 MHz bandwidth.
  It is a High Speed USB device powered by the USB bus.
   
  This package contains development files.
 
 **Installed size:** `67 KB`  
 **How to install:** `sudo apt install libhackrf-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libhackrf0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libhackrf0
 
  HackRF is an open source Software Defined Radio that can receive
  and transmit between 30 MHz and 6 GHz. HackRF has a 20 MHz bandwidth.
  It is a High Speed USB device powered by the USB bus.
   
  This package contains the shared library.
 
 **Installed size:** `59 KB`  
 **How to install:** `sudo apt install libhackrf0`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libusb-1.0-0 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
