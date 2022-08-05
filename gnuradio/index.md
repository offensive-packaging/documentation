---
Title: gnuradio
Homepage: https://www.gnuradio.org/
Repository: https://salsa.debian.org/bottoms/pkg-gnuradio
Architectures: any all
Version: 3.10.3.0-2
Metapackages: kali-linux-everything kali-tools-rfid kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gnuradio
 
  GNU Radio provides signal processing blocks to implement software
  radios. It can be used with readily-available low-cost external RF
  hardware to create software-defined radios, or without hardware in a
  simulation-like environment. It is widely used in hobbyist, academic
  and commercial environments to support both wireless communications
  research and real-world radio systems.
   
  GNU Radio applications are primarily written using the Python
  programming language, while the supplied performance-critical signal
  processing path is implemented in C++ using processor floating-point
  extensions, where available. Thus, the developer is able to implement
  real-time, high-throughput radio systems in a simple-to-use,
  rapid-application-development environment.
   
  While not primarily a simulation tool, GNU Radio does support
  development of signal processing algorithms using pre-recorded or
  generated data, avoiding the need for actual RF hardware.
   
  This package contains the gnuradio-companion, a graphical tool for
  creating signal flow graphs and generating flow-graph source code.
  Also included are a variety of tools and utility programs.
 
 **Installed size:** `20.58 MB`  
 **How to install:** `sudo apt install gnuradio`  
 
 {{< spoiler "Dependencies:" >}}
 * gnome-terminal | x-terminal-emulator
 * libboost-program-options1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgmp10 
 * libgnuradio-analog3.10.3 
 * libgnuradio-audio3.10.3 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-channels3.10.3 
 * libgnuradio-digital3.10.3 
 * libgnuradio-dtv3.10.3 
 * libgnuradio-fec3.10.3 
 * libgnuradio-fft3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-iio3.10.3 
 * libgnuradio-network3.10.3 
 * libgnuradio-pdu3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-qtgui3.10.3 
 * libgnuradio-runtime3.10.3 
 * libgnuradio-soapy3.10.3 
 * libgnuradio-trellis3.10.3 
 * libgnuradio-uhd3.10.3 
 * libgnuradio-video-sdl3.10.3 
 * libgnuradio-vocoder3.10.3 
 * libgnuradio-wavelet3.10.3 
 * libgnuradio-zeromq3.10.3 
 * libjs-mathjax
 * libqt5core5a 
 * libqt5widgets5 
 * libsoapysdr0.8 
 * libspdlog1-fmt8
 * libstdc++6 
 * libuhd4.2.0 
 * libvolk2-bin
 * libvolk2.5 
 * python3
 * python3 
 * python3-click
 * python3-click-plugins
 * python3-gi
 * python3-gi-cairo
 * python3-jsonschema
 * python3-lxml
 * python3-mako
 * python3-numpy 
 * python3-numpy-abi9
 * python3-opengl
 * python3-packaging
 * python3-pygccxml
 * python3-pyqt5
 * python3-pyqtgraph
 * python3-schema
 * python3-sip
 * python3-thrift
 * python3-yaml
 * python3-zmq
 {{< /spoiler >}}
 
 ##### dial_tone
 
 Dial tone example
 
 ```
 root@kali:~# man dial_tone
 DIAL_TONE(1)                     User Commands                    DIAL_TONE(1)
 
 NAME
        dial_tone - dial tone example
 
 DESCRIPTION
        GnuRadio Dial Tone example
 
 OPTIONS
        None
 
        Play a Dial Tone on the sound card output device.
 
 SEE ALSO
        The  c++ gnuradio example programs are in /usr/bin. There are also many
        Python and GnuRadio  Companion  examples  in  /usr/share/gnuradio/exam-
        ples/...
 
        tags_demo(1)      uhd_rx_cfile(1)     uhd_rx_nogui(1)     uhd_siggen(1)
        uhd_siggen_gui(1)
 
 DIAL_TONE 3.10.3.0                2022-07-23                      DIAL_TONE(1)
 ```
 
 - - -
 
 ##### display_qt
 
 A Gnu Radio Example gr-qtgui
 
 ```
 root@kali:~# man display_qt
 DISPLAY_QT(1)                    User Commands                   DISPLAY_QT(1)
 
 NAME
        display_qt - a Gnu Radio Example gr-qtgui
 
 DESCRIPTION
        Display a GUI using QT of a sine wave in noise.
 
        Example  program  instantiates a GNU Radio flow graph using a sine wave
        source, a noise source, and  gr-qtgui  blocks.  This  new  (in  version
        3.7.10) example shows how to build a C++ only QT based application.
 
 SEE ALSO
        http://gnuradio.squarespace.com/examples/tag/qt
 
 display_qt 3.10.3.0               2022-07-23                     DISPLAY_QT(1)
 ```
 
 - - -
 
 ##### gnuradio-companion
 
 GNU Radio Companion (GRC) is a graphical tool for creating GNU Radio signal flowgraphs.
 
 ```
 root@kali:~# man gnuradio-companion
 GNURADIO-COMPANION(1)            User Commands           GNURADIO-COMPANION(1)
 
 NAME
        gnuradio-companion  - GNU Radio Companion (GRC) is a graphical tool for
        creating GNU Radio signal flowgraphs.
 
 SYNOPSIS
        gnuradio-companion [options] [flowgraphs]
 
 DESCRIPTION
        GNU Radio is a free & open-source  software  development  toolkit  that
        provides  signal processing blocks to implement software-defined radios
        and signal-processing systems. The GNU  Radio  applications  themselves
        are  generally known as "flowgraphs", which are a series of signal pro-
        cessing blocks connected together, thus describing a data flow.
 
        gnuradio-companion is effectively a Python code-generation tool. When a
        flowgraph  is  "compiled" in GRC, it generates Python code that creates
        the desired GUI windows and  widgets,  and  creates  and  connects  the
        blocks in the flowgraph.
 
 OPTIONS
        flowgraphs Invoke the program with one or more existing flowgraphs.
 
        -h, --help
               show a help message and exit.
 
        --log  defines the level of logging output.
 
 SEE ALSO
        https://wiki.gnuradio.org/index.php/GNURadioCompanion
 
 GNU Radio Companion 3.10.3.0      2022-07-23             GNURADIO-COMPANION(1)
 ```
 
 - - -
 
 ##### gnuradio-config-info
 
 Show details on installed GNU radio
 
 ```
 root@kali:~# gnuradio-config-info -h
 Program options: gnuradio-config-info [options]:
   -h [ --help ]         print help message
   --print-all           print all information
   --prefix              print GNU Radio installation prefix
   --sysconfdir          print GNU Radio system configuration directory
   --prefsdir            print GNU Radio preferences directory
   --userprefsdir        print GNU Radio user preferences directory
   --prefs               print GNU Radio preferences
   --builddate           print GNU Radio build date (RFC2822 format)
   --enabled-components  print GNU Radio build time enabled components
   --cc                  print GNU Radio C compiler version
   --cxx                 print GNU Radio C++ compiler version
   --cflags              print GNU Radio CFLAGS
   -v [ --version ]      print GNU Radio version
   --pybind              print pybind11 version used in this build
 
 ```
 
 - - -
 
 ##### gr-ctrlport-monitor
 
 Gnuradio control port gui
 
 ```
 root@kali:~# man gr-ctrlport-monitor
 GR-CTRLPORT-MONITOR(1)           User Commands          GR-CTRLPORT-MONITOR(1)
 
 NAME
        gr-ctrlport-monitor - gnuradio control port gui
 
 SYNOPSIS
        gr-ctrlport-monitor [options]
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -H HOST, --host=HOST
               Hostname of ControlPort server.
 
        -p PORT, --port=PORT
               Port number of host's ControlPort endpoint.
 
        -i INTERFACES, --interfaces=INTERFACES
               Interfaces to use. [default=['lo']]
 
        -P PROTOCOL, --protocol=PROTOCOL
               Type of protocol to use (usually tcp). [default=tcp]
 
        -a APP, --app=APP
               Name of application [default=gnuradio]
 
        gr-ctrlport-monitor: error: no such option: --version
 
 SEE ALSO
        The  full  documentation  for Usage: is maintained as a Texinfo manual.
        If the info and Usage: programs are properly installed  at  your  site,
        the command
 
               info Usage:
 
        should give you access to the complete manual.
 
 GNU Radio Companion 3.10.3.0      2022-07-23            GR-CTRLPORT-MONITOR(1)
 ```
 
 - - -
 
 ##### gr-perf-monitorx
 
 Gnuradio control port gui
 
 ```
 root@kali:~# man gr-perf-monitorx
 GR-CTRLPORT-MONITOR(1)           User Commands          GR-CTRLPORT-MONITOR(1)
 
 NAME
        gr-ctrlport-monitor - gnuradio control port gui
 
 SYNOPSIS
        gr-ctrlport-monitor [options]
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -H HOST, --host=HOST
               Hostname of ControlPort server.
 
        -p PORT, --port=PORT
               Port number of host's ControlPort endpoint.
 
        -i INTERFACES, --interfaces=INTERFACES
               Interfaces to use. [default=['lo']]
 
        -P PROTOCOL, --protocol=PROTOCOL
               Type of protocol to use (usually tcp). [default=tcp]
 
        -a APP, --app=APP
               Name of application [default=gnuradio]
 
        gr-ctrlport-monitor: error: no such option: --version
 
 SEE ALSO
        The  full  documentation  for Usage: is maintained as a Texinfo manual.
        If the info and Usage: programs are properly installed  at  your  site,
        the command
 
               info Usage:
 
        should give you access to the complete manual.
 
 GNU Radio Companion 3.10.3.0      2022-07-23            GR-CTRLPORT-MONITOR(1)
 ```
 
 - - -
 
 ##### gr_filter_design
 
 GUI for creating filters for GNU Radio
 
 ```
 root@kali:~# man gr_filter_design
 GR_FILTER_DESIGN(1)              User Commands             GR_FILTER_DESIGN(1)
 
 NAME
        gr_filter_design - GUI for creating filters for GNU Radio
 
 SYNOPSIS
        gr_filter_design: [options] (input_filename)
 
 OPTIONS
        -h, --help
               show this help message and exit
 
 SEE ALSO
        gnuradio-companion(1)
 
 gr_filter_design 3.10.3.0         2022-07-23               GR_FILTER_DESIGN(1)
 ```
 
 - - -
 
 ##### gr_modtool
 
 The swiss army knife of module editing
 
 ```
 root@kali:~# man gr_modtool
 GNURADIO(1)                      User Commands                     GNURADIO(1)
 
 NAME
        gr-modtool - The swiss army knife of module editing
 
 DESCRIPTION
        When  developing a module, there's a lot of boring, monotonous work in-
        volved: boilerplate code, makefile editing etc. gr-modtool is a  script
        which aims to help with all these things by automatically editing make-
        files, using templates and doing as much work as possible for  the  de-
        veloper, such that you can jump straight into the DSP coding.
 
        Note  that gr-modtool makes a lot of assumptions on what the code looks
        like. The more your module is custom and has specific changes, the less
        useful gr-modtool becomes.
 
 SEE ALSO
        https://wiki.gnuradio.org/index.php/OutOfTreeModules
 
 gr_modtool 3.10.3.0               2022-07-23                       GNURADIO(1)
 ```
 
 - - -
 
 ##### gr_plot
 
 Display time series of samples from a file
 
 ```
 root@kali:~# gr_plot -h
 usage: gr_plot [-h]
                [-d {complex64,float32,uint32,int32,uint16,int16,uint8,int8}]
                [-B BLOCK] [-s START] [-R SAMPLE_RATE]
                FILE [FILE ...]
 
 Takes a GNU Radio binary file and displays the samples versus time. You can
 set the block size to specify how many points to read in at a time and the
 start position in the file. By default, the system assumes a sample rate of 1,
 so in time, each sample is plotted versus the sample number. To set a true
 time axis, set the sample rate (-R or --sample-rate) to the sample rate used
 when capturing the samples.
 
 positional arguments:
   FILE                  Input file with samples
 
 options:
   -h, --help            show this help message and exit
   -d {complex64,float32,uint32,int32,uint16,int16,uint8,int8}, --data-type {complex64,float32,uint32,int32,uint16,int16,uint8,int8}
                         Specify the data type [default='complex64']
   -B BLOCK, --block BLOCK
                         Specify the block size [default=1000]
   -s START, --start START
                         Specify where to start in the file [default=0]
   -R SAMPLE_RATE, --sample-rate SAMPLE_RATE
                         Set the sampler rate of the data [default=1.0]
 ```
 
 - - -
 
 ##### gr_plot_const
 
 Constellation plot of I&Q data using GNU Radio
 
 ```
 root@kali:~# gr_plot_const -h
 usage: gr_plot_const [-h] [-B BLOCK] [-s START] [-R SAMPLE_RATE] FILE
 
 Takes a GNU Radio complex binary file and displays the I&Q data versus time
 and the constellation plot (I vs. Q). You can set the block size to specify
 how many points to read in at a time and the start position in the file. By
 default, the system assumes a sample rate of 1, so in time, each sample is
 plotted versus the sample number. To set a true time axis, set the sample rate
 (-R or --sample-rate) to the sample rate used when capturing the samples.
 
 positional arguments:
   FILE                  Input file with complex samples
 
 options:
   -h, --help            show this help message and exit
   -B BLOCK, --block BLOCK
                         Specify the block size [default=1000]
   -s START, --start START
                         Specify where to start in the file [default=0]
   -R SAMPLE_RATE, --sample-rate SAMPLE_RATE
                         Set the sampler rate of the data [default=1.0]
 ```
 
 - - -
 
 ##### gr_plot_fft
 
 Frequency domain GNU Radio plotting
 
 ```
 root@kali:~# gr_plot_fft -h
 usage: gr_plot_fft [-h]
                    [-d {complex64,float32,uint32,int32,uint16,int16,uint8,int8}]
                    [-B BLOCK] [-s START] [-R SAMPLE_RATE]
                    FILE
 
 Takes a GNU Radio complex binary file and displays the I&Q data versus time as
 well as the frequency domain (FFT) plot. The y-axis values are plotted
 assuming volts as the amplitude of the I&Q streams and converted into dBm in
 the frequency domain (the 1/N power adjustment out of the FFT is performed
 internally). The script plots a certain block of data at a time, specified on
 the command line as -B or --block. This value defaults to 1000. The start
 position in the file can be set by specifying -s or --start and defaults to 0
 (the start of the file). By default, the system assumes a sample rate of 1, so
 in time, each sample is plotted versus the sample number. To set a true time
 and frequency axis, set the sample rate (-R or --sample-rate) to the sample
 rate used when capturing the samples.
 
 positional arguments:
   FILE                  Input file with samples
 
 options:
   -h, --help            show this help message and exit
   -d {complex64,float32,uint32,int32,uint16,int16,uint8,int8}, --data-type {complex64,float32,uint32,int32,uint16,int16,uint8,int8}
                         Specify the data type [default='complex64']
   -B BLOCK, --block BLOCK
                         Specify the block size [default=1000]
   -s START, --start START
                         Specify where to start in the file [default=0]
   -R SAMPLE_RATE, --sample-rate SAMPLE_RATE
                         Set the sampler rate of the data [default=1.0]
 ```
 
 - - -
 
 ##### gr_plot_iq
 
 Plot complex binary I&Q data versus time using GNU Radio
 
 ```
 root@kali:~# gr_plot_iq -h
 usage: gr_plot_iq [-h] [-B BLOCK] [-s START] [-R SAMPLE_RATE] FILE
 
 Takes a GNU Radio complex binary file and displays the I&Q data versus time.
 You can set the block size to specify how many points to read in at a time and
 the start position in the file. By default, the system assumes a sample rate
 of 1, so in time, each sample is plotted versus the sample number. To set a
 true time axis, set the sample rate (-R or --sample-rate) to the sample rate
 used when capturing the samples.
 
 positional arguments:
   FILE                  Input file with complex samples
 
 options:
   -h, --help            show this help message and exit
   -B BLOCK, --block BLOCK
                         Specify the block size [default=1000]
   -s START, --start START
                         Specify where to start in the file [default=0]
   -R SAMPLE_RATE, --sample-rate SAMPLE_RATE
                         Set the sampler rate of the data [default=1.0]
 ```
 
 - - -
 
 ##### gr_plot_psd
 
 GNU Radio power spectrum plotting
 
 ```
 root@kali:~# gr_plot_psd -h
 usage: gr_plot_psd [-h]
                    [-d {complex64,float32,int32,uint32,int16,uint16,int8,uint8}]
                    [-B BLOCK] [-s START] [-R SAMPLE_RATE]
                    [--psd-size PSD_SIZE] [--spec-size SPEC_SIZE] [-S]
                    FILE
 
 Takes a GNU Radio binary file (with specified data type using --data-type) and
 displays the I&Q data versus time as well as the power spectral density (PSD)
 plot. The y-axis values are plotted assuming volts as the amplitude of the I&Q
 streams and converted into dBm in the frequency domain (the 1/N power
 adjustment out of the FFT is performed internally). The script plots a certain
 block of data at a time, specified on the command line as -B or --block. The
 start position in the file can be set by specifying -s or --start and defaults
 to 0 (the start of the file). By default, the system assumes a sample rate of
 1, so in time, each sample is plotted versus the sample number. To set a true
 time and frequency axis, set the sample rate (-R or --sample-rate) to the
 sample rate used when capturing the samples. Finally, the size of the FFT to
 use for the PSD and spectrogram plots can be set independently with --psd-size
 and --spec-size, respectively. The spectrogram plot does not display by
 default and is turned on with -S or --enable-spec.
 
 positional arguments:
   FILE                  Input file with samples
 
 options:
   -h, --help            show this help message and exit
   -d {complex64,float32,int32,uint32,int16,uint16,int8,uint8}, --data-type {complex64,float32,int32,uint32,int16,uint16,int8,uint8}
                         Specify the data type [default='complex64']
   -B BLOCK, --block BLOCK
                         Specify the block size [default=8192]
   -s START, --start START
                         Specify where to start in the file [default=0]
   -R SAMPLE_RATE, --sample-rate SAMPLE_RATE
                         Set the sampler rate of the data [default=1.0]
   --psd-size PSD_SIZE   Set the size of the PSD FFT [default=1024]
   --spec-size SPEC_SIZE
                         Set the size of the spectrogram FFT [default=256]
   -S, --enable-spec     Turn on plotting the spectrogram [default=False]
 ```
 
 - - -
 
 ##### gr_plot_qt
 
 Plot data using Qt graphics and GNU Radio
 
 ```
 root@kali:~# man gr_plot_qt
 GR_PLOT_QT(1)                    User Commands                   GR_PLOT_QT(1)
 
 NAME
        gr_plot_qt - plot data using Qt graphics and GNU Radio
 
 DESCRIPTION
        Fancy plot display.
 
 SEE ALSO
        gr_plot_char(1)   gr_plot_const(1)   gr_plot_fft_c(1)  gr_plot_fft_f(1)
        gr_plot_float(1)    gr_plot_int(1)    gr_plot_iq(1)    gr_plot_psd_c(1)
        gr_plot_psd_f(1)  gr_plot_qt(1)  gr_plot_short(1)
 
 gr_plot_qt 3.10.3.0               2022-07-23                     GR_PLOT_QT(1)
 ```
 
 - - -
 
 ##### gr_read_file_metadata
 
 A Gnu Radio Utility
 
 ```
 root@kali:~# man gr_read_file_metadata
 GR_READ_FILE_METADATA(1)         User Commands        GR_READ_FILE_METADATA(1)
 
 NAME
        gr_read_file_metadata - a Gnu Radio Utility
 
 DESCRIPTION
        Read in a GNU Radio file with meta data, extracts the header and prints
        it.
 
        Metadata file source and sink blocks (Tom Rondeau)
 
        Two new blocks implement enhanced file source and sink blocks that  in-
        corporate  metadata  passed using the stream tags feature in GNU Radio.
        It is now possible to store things like frequency and sample rate  into
        capture  files,  or  whatever key/value pairs you tag onto data streams
        inside a flowgraph.
 
 SEE ALSO
        http://www.trondeau.com/home/2012/12/15/metadata-file-format.html
 
 gr_read_file_metadata 3.10.3.0    2022-07-23          GR_READ_FILE_METADATA(1)
 ```
 
 - - -
 
 ##### grcc
 
 Gnu Radio Companion Compiler
 
 ```
 root@kali:~# man grcc
 GRCC(1)                          User Commands                         GRCC(1)
 
 NAME
        grcc - Gnu Radio Companion Compiler
 
 DESCRIPTION
        Just compile a gnuradio companion flowgraph without invoking the gui.
 
        Given  an input GRC file and an output directory, create a runnable ap-
        plication in the output directory.
 
 SEE ALSO
        gnuradio-companion(1)
 
 grcc 3.10.3.0                     2022-07-23                           GRCC(1)
 ```
 
 - - -
 
 ##### polar_channel_construction
 
 Gnu Radio Polar Configurator
 
 ```
 root@kali:~# man polar_channel_construction
 POLAR_CHANNEL_CONSTRUCTION(1)    User Commands   POLAR_CHANNEL_CONSTRUCTION(1)
 
 NAME
        polar_channel_construction - Gnu Radio Polar Configurator
 
 DESCRIPTION
        POLAR code channel construction.
 
 Channel Construction
        polar_channel_construction  exposes  functionality  to  calculate polar
        channels for different sizes.   It  may  be  used  to  calculate  Bhat-
        tacharyya  parameters once and store them in a file in '~/.gnuradio/po-
        lar'.  Frozen bit positions are recalculated on every run.
 
        polar_channel_construction provides a command-line  interface  for  all
        the  channel construction code.  These features are also accessible via
        the Polar Configurator block in GRC.
 
 BEC
        BEC channel construction can be calculated explicitly because  the  BEC
        represents a special case which simplifies the task.  All functionality
        regarding this channel is located in 'channel_construction_bec'.
 
 AWGN
        In general channel construction for polar codes is a very time  consum-
        ing  task.  Tal and Vardy proposed a quantization algorithm for channel
        construction which makes it feasible.  The corresponding implementation
        is  located  in  'channel_construction_awgn'.   It should be noted that
        this more of a baseline implementation which  lacks  all  the  advanced
        features  the  original  implementation provides.  However, simulations
        show that BEC channel construction with a design-SNR  of  0.0dB  yields
        similar performance and should be preferred here.
 
 SEE ALSO
        gnuradio-companion(1)
 
 polar_channel_construction 3.10.3.2022-07-23     POLAR_CHANNEL_CONSTRUCTION(1)
 ```
 
 - - -
 
 ##### tags_demo
 
 GNURadio and UHD tags example
 
 ```
 root@kali:~# tags_demo --help
 UHD Tags Demo Allowed options:
   --help                             help message
   --addr arg                         the device address in string format
   --rate arg (=1000000)              the sample rate in samples per second
   --freq arg (=10000000)             the center frequency in Hz
   --burst arg (=0.10000000000000001) the duration of each burst in seconds
   --idle arg (=0.050000000000000003) idle time between bursts in seconds
   --length_tag arg                   the length tag key name
 
 The tags sink demo block will print USRP source time stamps.
 The tags source demo block will send bursts to the USRP sink.
 Look at the USRP output on a scope to see the timed bursts.
 
 ```
 
 - - -
 
 ##### uhd_fft
 
 Display spectrum from UHD receiver
 
 ```
 root@kali:~# man uhd_fft
 UHD_FFT(1)                       User Commands                      UHD_FFT(1)
 
 NAME
        uhd_fft - Display spectrum from UHD receiver
 
 DESCRIPTION
        Show received signal spectrum
 
        Unable to access the X Display, is $DISPLAY set properly?
 
 SEE ALSO
        uhd_rx_cfile(1) uhd_rx_nogui(1) uhd_siggen(1) uhd_siggen_gui(1)
 
 uhd_fft 3.10.3.0                  2022-07-23                        UHD_FFT(1)
 ```
 
 - - -
 
 ##### uhd_rx_cfile
 
 Save UHD received data
 
 ```
 root@kali:~# man uhd_rx_cfile
 UHD_RX_CFILE(1)                  User Commands                 UHD_RX_CFILE(1)
 
 NAME
        uhd_rx_cfile - Save UHD received data
 
 SYNOPSIS
        uhd_rx_cfile: [options] output_filename
 
 DESCRIPTION
        Save I&Q data to a complex file for later use.
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -a ARGS, --args=ARGS
               UHD device address args , [default=]
 
        --spec=SPEC
               Subdevice of UHD device where appropriate
 
        -A ANTENNA, --antenna=ANTENNA
               select Rx Antenna where appropriate
 
        --samp-rate=SAMP_RATE
               set sample rate (bandwidth) [default=1000000.0]
 
        -f FREQ, --freq=FREQ
               set frequency to FREQ
 
        -g GAIN, --gain=GAIN
               set gain in dB (default is midpoint)
 
        -s, --output-shorts
               output interleaved shorts instead of complex floats
 
        -N NSAMPLES, --nsamples=NSAMPLES
               number of samples to collect [default=+inf]
 
        -v, --verbose
               verbose output
 
        --lo-offset=LO_OFFSET
               set daughterboard LO offset to OFFSET [default=hw default]
 
 SEE ALSO
        uhd_fft(1) uhd_rx_nogui(1) uhd_siggen(1) uhd_siggen_gui(1)
 
 uhd_rx_cfile 3.10.3.0             2022-07-23                   UHD_RX_CFILE(1)
 ```
 
 - - -
 
 ##### uhd_rx_nogui
 
 GNU Radio receiver
 
 ```
 root@kali:~# man uhd_rx_nogui
 UHD_RX_NOGUI(1)                  User Commands                 UHD_RX_NOGUI(1)
 
 NAME
        uhd_rx_nogui - GNU Radio receiver
 
 SYNOPSIS
        uhd_rx_nogui.py [options]
 
 DESCRIPTION
        Command line GNU Radio receiver that takes signal from a UHD peripheral
        receiver and sends demodulated audio to the sound device.
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -a ARGS, --args=ARGS
               UHD device address args , [default=]
 
        --spec=SPEC
               Subdevice of UHD device where appropriate
 
        -A ANTENNA, --antenna=ANTENNA
               select Rx Antenna where appropriate [default=none]
 
        -f Hz, --frequency=Hz
               set receive frequency to Hz [default=none]
 
        -c Hz, --calibration=Hz
               set frequency offset to Hz [default=0.0]
 
        -g dB, --gain=dB
               set RF gain [default is midpoint]
 
        -m TYPE, --modulation=TYPE
               set modulation type (AM,FM) [default=none]
 
        -o RATE, --output-rate=RATE
               set audio output rate to RATE [default=32000]
 
        -r dB, --rf-squelch=dB
               set RF squelch to dB [default=-50.0]
 
        -p FREQ, --ctcss=FREQ
               set CTCSS squelch to FREQ [default=none]
 
        -O AUDIO_OUTPUT, --audio-output=AUDIO_OUTPUT
               pcm device name.  E.g., hw:0,0 or surround51 or /dev/dsp
 
 SEE ALSO
        uhd_fft(1) uhd_rx_cfile(1) uhd_siggen(1) uhd_siggen_gui(1)
 
 uhd_rx_nogui 3.10.3.0             2022-07-23                   UHD_RX_NOGUI(1)
 ```
 
 - - -
 
 ##### uhd_siggen
 
 Signal Generator using UHD hardware
 
 ```
 root@kali:~# man uhd_siggen
 UHD_SIGGEN(1)                    User Commands                   UHD_SIGGEN(1)
 
 NAME
        uhd_siggen - Signal Generator using UHD hardware
 
 SYNOPSIS
        uhd_siggen: [options]
 
 DESCRIPTION
        Command-line signal generator application.
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -a ARGS, --args=ARGS
               UHD device address args , [default=]
 
        --spec=SPEC
               Subdevice of UHD device where appropriate
 
        -A ANTENNA, --antenna=ANTENNA
               select Rx Antenna where appropriate
 
        -s SAMP_RATE, --samp-rate=SAMP_RATE
               set sample rate (bandwidth) [default=1000000.0]
 
        -g GAIN, --gain=GAIN
               set gain in dB (default is midpoint)
 
        -f FREQ, --tx-freq=FREQ
               Set carrier frequency to FREQ [default=mid-point]
 
        -x WAVEFORM_FREQ, --waveform-freq=WAVEFORM_FREQ
               Set baseband waveform frequency to FREQ [default=0]
 
        -y WAVEFORM2_FREQ, --waveform2-freq=WAVEFORM2_FREQ
               Set 2nd waveform frequency to FREQ [default=none]
 
        --sine Generate a carrier modulated by a complex sine wave
 
        --const
               Generate a constant carrier
 
        --offset=OFFSET
               Set waveform phase offset to OFFSET [default=0]
 
        --gaussian
               Generate Gaussian random output
 
        --uniform
               Generate Uniform random output
 
        --2tone
               Generate Two Tone signal for IMD testing
 
        --sweep
               Generate a swept sine wave
 
        --amplitude=AMPL
               Set output amplitude to AMPL (0.0-1.0) [default=0.15]
 
        -v, --verbose
               Use verbose console output [default=False]
 
 SEE ALSO
        uhd_siggen_gui(1)
 
 uhd_siggen 3.10.3.0               2022-07-23                     UHD_SIGGEN(1)
 ```
 
 - - -
 
 ##### uhd_siggen_gui
 
 GNU Radio signal generator using UHD hardware
 
 ```
 root@kali:~# man uhd_siggen_gui
 UHD_SIGGEN_GUI(1)                User Commands               UHD_SIGGEN_GUI(1)
 
 NAME
        uhd_siggen_gui - GNU Radio signal generator using UHD hardware
 
 SYNOPSIS
        uhd_siggen_gui: [options]
 
 DESCRIPTION
        GUI to allow UHD supported hardware to be a signal generator.
 
 OPTIONS
        -h, --help
               show this help message and exit
 
        -a ARGS, --args=ARGS
               UHD device address args , [default=]
 
        --spec=SPEC
               Subdevice of UHD device where appropriate
 
        -A ANTENNA, --antenna=ANTENNA
               select Rx Antenna where appropriate
 
        -s SAMP_RATE, --samp-rate=SAMP_RATE
               set sample rate (bandwidth) [default=1000000.0]
 
        -g GAIN, --gain=GAIN
               set gain in dB (default is midpoint)
 
        -f FREQ, --tx-freq=FREQ
               Set carrier frequency to FREQ [default=mid-point]
 
        -x WAVEFORM_FREQ, --waveform-freq=WAVEFORM_FREQ
               Set baseband waveform frequency to FREQ [default=0]
 
        -y WAVEFORM2_FREQ, --waveform2-freq=WAVEFORM2_FREQ
               Set 2nd waveform frequency to FREQ [default=none]
 
        --sine Generate a carrier modulated by a complex sine wave
 
        --const
               Generate a constant carrier
 
        --offset=OFFSET
               Set waveform phase offset to OFFSET [default=0]
 
        --gaussian
               Generate Gaussian random output
 
        --uniform
               Generate Uniform random output
 
        --2tone
               Generate Two Tone signal for IMD testing
 
        --sweep
               Generate a swept sine wave
 
        --amplitude=AMPL
               Set output amplitude to AMPL (0.0-1.0) [default=0.15]
 
        -v, --verbose
               Use verbose console output [default=False]
 
 SEE ALSO
        uhd_siggen(1)
 
 uhd_siggen_gui 3.10.3.0           2022-07-23                 UHD_SIGGEN_GUI(1)
 ```
 
 - - -
 
 ### gnuradio-dev
 
  Header files for the GNU Radio software defined radio system.
  Since GNU Radio is a framework for development of SDR
  applications, you are likely to need this installed.
   
  Part of the main gnuradio build.
 
 **Installed size:** `2.52 MB`  
 **How to install:** `sudo apt install gnuradio-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * gnuradio 
 * libboost-date-time1.74-dev
 * libboost-filesystem1.74-dev
 * libboost-program-options1.74-dev
 * libboost-regex1.74-dev
 * libboost-system1.74-dev
 * libboost-test1.74-dev
 * libboost-thread1.74-dev
 * libcppunit-dev
 * libfftw3-dev
 * libgmp-dev
 * libgsm1-dev
 * libspdlog-dev
 * libthrift-dev
 * libvolk2-dev
 * pybind11-dev
 * python3-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### gnuradio-doc
 
  Documentation for the GNU Radio software defined radio system
  in html and xml form.
   
  Part of the main gnuradio build.
 
 **Installed size:** `251.71 MB`  
 **How to install:** `sudo apt install gnuradio-doc`  
 
 
 - - -
 
 ### libgnuradio-analog3.10.3
 
  Library for handling analog signal processing functions.
  These functions are also in gnuradio-core.
  Part of the main gnuradio build.
 
 **Installed size:** `630 KB`  
 **How to install:** `sudo apt install libgnuradio-analog3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-fft3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-audio3.10.3
 
  This is the gr-audio library, used to connect to audio sources
  (mic-in) and sinks (speaker-out) ports on a computer. The underlying
  hardware driver is system and OS dependent and this module should
  automatically discover the correct one to use.  Part of the main
  gnuradio build.
 
 **Installed size:** `430 KB`  
 **How to install:** `sudo apt install libgnuradio-audio3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libasound2 
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libjack-jackd2-0  | libjack-0.125
 * libportaudio2 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-blocks3.10.3
 
  Some non-signal processing blocks.
  These functions are also in gnuradio-core.
  Part of the main gnuradio build.
 
 **Installed size:** `2.71 MB`  
 **How to install:** `sudo apt install libgnuradio-blocks3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libsndfile1 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-channels3.10.3
 
  Some channel oriented processing blocks.
  These functions are also in gnuradio-core.
  Part of the main gnuradio build.
 
 **Installed size:** `470 KB`  
 **How to install:** `sudo apt install libgnuradio-channels3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-analog3.10.3 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-digital3.10.3
 
  All the functions for doing digital modulation and demodulation,
  including bpsk, qpsk, gmsk and ofdm signals.
  Part of the main gnuradio build.
 
 **Installed size:** `1.49 MB`  
 **How to install:** `sudo apt install libgnuradio-digital3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-analog3.10.3 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-dtv3.10.3
 
  ATSC support, gr-atsc ported to a new framework, as well as
  DVB-S2, DVB-T, DVB-T2 digital video broadcast standards.
  Part of the main gnuradio build.
 
 **Installed size:** `1.32 MB`  
 **How to install:** `sudo apt install libgnuradio-dtv3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-fec3.10.3 
 * libgnuradio-fft3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-fec3.10.3
 
  Handle forward error correction processing in gnuradio.
  Implements the GNU Radio FEC API, supporting encoders and
  decoders for no-op dummmy, repetition, and convolutional classes.
  Part of the main gnuradio build.
 
 **Installed size:** `757 KB`  
 **How to install:** `sudo apt install libgnuradio-fec3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libgsl27 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-fft3.10.3
 
  Library for Fourier transform techniques used in gnuradio.
  Uses single precision FFT from libfftw3-single3.
  Part of the main gnuradio build.
 
 **Installed size:** `306 KB`  
 **How to install:** `sudo apt install libgnuradio-fft3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfftw3-single3 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-filter3.10.3
 
  Library of filter blocks used in gnuradio. Implements
  FIR, IIR and FFT filters, as well as Polyphase filterbank and
  PFB arbitrary resampler methods.
  Part of the main gnuradio build.
 
 **Installed size:** `1.00 MB`  
 **How to install:** `sudo apt install libgnuradio-filter3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-fft3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-iio3.10.3
 
  Libiio is a library that has been conceived to ease the development of
  applications interfacing Industrial Input/Output (IIO) devices through
  the IIO subsystem of the Linux kernel.
   
  The IIO blocks for GnuRadio can be used to create flowgraphs that interface
  IIO devices through libiio.
   
  Part of the main gnuradio build.
 
 **Installed size:** `495 KB`  
 **How to install:** `sudo apt install libgnuradio-iio3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libad9361-0 
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libiio0 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-network3.10.3
 
  Library of  blocks that implement UDP and TCP source and
  sink blocks supporting both IPv4 and IPv6.
  Part of the main gnuradio build.
 
 **Installed size:** `546 KB`  
 **How to install:** `sudo apt install libgnuradio-network3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-pdu3.10.3
 
  Protocol Data Units library provides signal processing
  blocks that operate on Protocol Data Unit format messages. Many
  such blocks are analogs of streaming API functionality.
  Part of the main gnuradio build.
 
 **Installed size:** `590 KB`  
 **How to install:** `sudo apt install libgnuradio-pdu3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-atomic1.74.0 
 * libboost-program-options1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libfftw3-single3 
 * libfmt8 
 * libgcc-s1 
 * libgmp10 
 * libgmpxx4ldbl 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-fft3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libsndfile1 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-pmt3.10.3
 
  Polymorphic Types are opaque data types that are designed as generic
  containers of data that can be safely passed around between blocks
  and threads in GNU Radio.
  Part of the main gnuradio build.
 
 **Installed size:** `406 KB`  
 **How to install:** `sudo apt install libgnuradio-pmt3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-qtgui3.10.3
 
  QT-based graphical sinks for gnuradio applications.
  Implements opengl, raster and native plotting methods, and
  supports a QT Style Sheet (QSS) file to adjust the look.
  Part of the main gnuradio build.
 
 **Installed size:** `1.75 MB`  
 **How to install:** `sudo apt install libgnuradio-qtgui3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-fft3.10.3 
 * libgnuradio-filter3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5widgets5 
 * libqwt-qt5-6 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-runtime3.10.3
 
  Top level component library. Defines core blocks. Handles
  settings for logging, performance counters, and control port.
  Part of the main gnuradio build.
 
 **Installed size:** `1.84 MB`  
 **How to install:** `sudo apt install libgnuradio-runtime3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-program-options1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgmp10 
 * libgnuradio-pmt3.10.3 
 * libpython3.10 
 * libspdlog1-fmt8
 * libstdc++6 
 * libthrift-0.16.0 
 * libunwind8
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-soapy3.10.3
 
  Soapy hardware drivers using the SoapySDR driver framework.
  Part of the main gnuradio build.
 
 **Installed size:** `426 KB`  
 **How to install:** `sudo apt install libgnuradio-soapy3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgmp10 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libsoapysdr0.8 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-trellis3.10.3
 
  Library for trellis coding modulation, including the Viterbi
  Algorithm, Concatenated Coding and Turbo Decoding
  based upon finite state machine (FSM) class.
  Part of the main gnuradio build.
 
 **Installed size:** `1006 KB`  
 **How to install:** `sudo apt install libgnuradio-trellis3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-uhd3.10.3
 
  The gnuradio interface to the UHD library to connect to and send and
  receive data between to the Ettus Research, LLC product line -
  including the USRP family of software radio peripheral devices.
  Part of the main gnuradio build.
 
 **Installed size:** `587 KB`  
 **How to install:** `sudo apt install libgnuradio-uhd3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libuhd4.2.0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-video-sdl3.10.3
 
  Library for handling SDL (Simple DirectMedia Layer) video data.
  Implements input and output blocks.
  Part of the main gnuradio build.
 
 **Installed size:** `229 KB`  
 **How to install:** `sudo apt install libgnuradio-video-sdl3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libsdl1.2debian 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-vocoder3.10.3
 
  Library of vocoder blocks, including ulaw, alaw, gsm and codec2.
  Debian uses external libraries for gsm and codec2.
   
  Part of the main gnuradio build.
 
 **Installed size:** `314 KB`  
 **How to install:** `sudo apt install libgnuradio-vocoder3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcodec2-1.0 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libgsm1 
 * libspdlog1-fmt8
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-wavelet3.10.3
 
  Library of Daubechies wavelet function blocks.
  wvps computes the Wavelet Power Spectrum from
  a set of wavelet coefficients.
   
  Part of the main gnuradio build.
 
 **Installed size:** `125 KB`  
 **How to install:** `sudo apt install libgnuradio-wavelet3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-atomic1.74.0 
 * libboost-program-options1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgmp10 
 * libgmpxx4ldbl 
 * libgnuradio-blocks3.10.3 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libgsl27 
 * libgslcblas0 
 * libsndfile1 
 * libspdlog1-fmt8
 * libstdc++6 
 * libvolk2.5 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-zeromq3.10.3
 
  0MQ messaging library support. Provide network socket
  endpoints for gnuradio data and message streams.
  PUB/SUB, PUSH/PULL, REP/REQ models supported.
   
  Part of the main gnuradio build.
 
 **Installed size:** `354 KB`  
 **How to install:** `sudo apt install libgnuradio-zeromq3.10.3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfmt8 
 * libgcc-s1 
 * libgnuradio-pmt3.10.3 
 * libgnuradio-runtime3.10.3 
 * libspdlog1-fmt8
 * libstdc++6 
 * libzmq5 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
