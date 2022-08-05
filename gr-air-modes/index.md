---
Title: gr-air-modes
Homepage: https://github.com/bistromath/gr-air-modes
Repository: https://salsa.debian.org/bottoms/pkg-gr-air-modes
Architectures: any
Version: 0.0.20210211-2
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gr-air-modes
 
  A software-defined radio receiver for Mode S
  transponder signals, including ADS-B reports from equipped aircraft.
   
  Multiple output formats are supported:
   * Raw (or minimally processed) output of packet data
   * Parsed text
   * SQLite database
   * KML for use with Google Earth
   * SBS-1-compatible output for use with e.g. PlanePlotter or Virtual
     Radar Server
   * FlightGear multiplayer interface for real-time display of traffic
     within the simulator
 
 **Installed size:** `365 KB`  
 **How to install:** `sudo apt install gr-air-modes`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-air-modes1 
 * libgnuradio-runtime3.10.2 
 * libstdc++6 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 * python3-zmq
 {{< /spoiler >}}
 
 ##### modes_rx
 
 Gnuradio Mode-S/ADS-B receiver
 
 ```
 root@kali:~# man modes_rx
 MODES_RX:(1)                     User Commands                    MODES_RX:(1)
 
 NAME
        modes_rx: - Gnuradio Mode-S/ADS-B receiver
 
 SYNOPSIS
        modes_rx [options] [options]
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -l LOCATION, --location=LOCATION
               GPS coordinates of receiving station in format xx.xxxxx,xx.xxxxx
 
        -a REMOTE, --remote=REMOTE
               specify  additional  servers  from  which to take data in format
               tcp://x.x.x.x:y,tcp://....
 
        -n, --no-print
               disable printing decoded packets to stdout
 
        -K KML, --kml=KML
               filename for Google Earth KML output
 
        -P, --sbs1
               open an SBS-1-compatible server on port 30003
 
        -m MULTIPLAYER, --multiplayer=MULTIPLAYER
               FlightGear server to send aircraft data, in format host:port
 
               Receiver setup options:
 
        -s SOURCE, --source=SOURCE
               Choose source:  uhd,  osmocom,  <filename>,  or  <ip:port>  [de-
               fault=uhd]
 
        -t PORT, --tcp=PORT
               Open a TCP server on this port to publish reports
 
        -R SUBDEV, --subdev=SUBDEV
               select USRP Rx side A or B
 
        -A ANTENNA, --antenna=ANTENNA
               select which antenna to use on daughterboard
 
        -D ARGS, --args=ARGS
               arguments to pass to radio constructor
 
        -f FREQ, --freq=FREQ
               set receive frequency in Hz [default=1090000000.0]
 
        -g dB, --gain=dB
               set RF gain
 
        -r RATE, --rate=RATE
               set sample rate [default=4000000.0]
 
        -T THRESHOLD, --threshold=THRESHOLD
               set pulse detection threshold above noise in dB [default=7.0]
 
        -p, --pmf
               Use pulse matched filtering [default=False]
 
        -d, --dcblock
               Use  a  DC  blocking  filter  (best  for HackRF Jawbreaker) [de-
               fault=False]
 
 DESCRIPTION
        A Qt Graphical User Interface to display positions and status  messages
        of aircraft as reported on 1090 MHz.
 
        gr-air-modes  implements  a  software-defined radio receiver for Mode S
        transponder signals, including ADS-B reports from equipped aircraft.
 
        Mode S is the transponder protocol used in modern commercial  aircraft.
        A  Mode  S-equipped  aircraft  replies to radar interrogation by either
        ground radar (secondary surveillance) or other aircraft ("Traffic  Col-
        lision Avoidance System", or TCAS). The protocol is an extended version
        of the Mode A/C protocol used in transponders since the 1940s.  Mode  S
        reports  include a unique airframe identifier (referred to as the "ICAO
        number") and altitude (to facilitate  separation  control).   This  re-
        ceiver  listens to the 1090MHz downlink channel; interrogation requests
        at 1030MHz are not received or decoded by this program.
 
        Automatic Dependent Surveillance-Broadcast (ADS-B) is  a  communication
        protocol using the Extended Squitter capability of the Mode S transport
        layer. There are other implementations (VDL Mode 2  and  UAT,  for  in-
        stance)  but  Mode S remains the primary ADS-B transport for commercial
        use. The protocol is:
 
        * Automatic: it requires no pilot input
 
        * Dependent: it is dependent on altimeter, GPS, and other aircraft
          instrumentation for information
 
        * Surveillance: it provides current information about the transmitting
          aircraft
 
        * Broadcast: it is one-way, broadcast to all receivers within range.
 
        ADS-B-equipped aircraft broadcast ("squitter") their  position,  veloc-
        ity,  flight  number, and other interesting information to any receiver
        within range of the aircraft. Position reports are typically  generated
        once per second and flight indentification every five seconds.
 
        Implementation of ADS-B is mandatory in European airspace as well as in
        Australia. North American implementation is  still  voluntary,  with  a
        mandate arriving in 2020 via the FAA's "NextGen" program.
 
        The  receiver  modes_rx is written for use with Ettus Research USRP de-
        vices, although the "RTLSDR" receivers are also supported via the Osmo-
        com driver. In theory, any receiver which outputs complex samples at at
        least 2Msps should work via the file input or UDP input options, or  by
        means of a Gnuradio interface. Multiple output formats are supported:
 
        * Raw (or minimally processed) output of packet data
 
        * Parsed text
 
        * SQLite database
 
        * KML for use with Google Earth
 
        * SBS-1-compatible output for use with e.g. PlanePlotter or Virtual
          Radar Server
 
        * FlightGear multiplayer interface for real-time display of traffic
          within the simulator
 
        Most  of  the common ADS-B reports are fully decoded per specification.
        Those that are not are generally ones which are not commonly used.
 
        Should you receive a large number of reports which result in  "not  im-
        plemented"  or  "No handler" messages, please use the -w option to save
        raw data and forward it to the author. To save time, note that  receiv-
        ing  a  small number of spurious reports is expected; false reports can
        be excluded by looking for multiple  reports  from  the  same  aircraft
        (i.e., the same ICAO 6-digit hexadecimal number).
 
 REQUIRES
        A  GNU Radio supported receiver for RF capable of 2 Mbits/second sample
        rate and tuning to 1090 MHz. (Or captured data file or network  connec-
        tion to a data source.)
 
 SEE ALSO
        The X GUI application modes_gui
 
        modes_gui(1)
 
 modes_rx                         October 2013                     MODES_RX:(1)
 ```
 
 - - -
 
 ### libgnuradio-air-modes1
 
  A software-defined radio receiver for Mode S
  transponder signals, including ADS-B reports from equipped aircraft.
   
  This package provides a shared library.
 
 **Installed size:** `105 KB`  
 **How to install:** `sudo apt install libgnuradio-air-modes1`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-pmt3.10.2 
 * libgnuradio-runtime3.10.2 
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
