---
Title: bruteshark
Homepage: https://github.com/odedshimon/BruteShark
Repository: https://gitlab.com/kalilinux/packages/bruteshark
Architectures: amd64
Version: 1.2.5-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bruteshark
 
  This package contains a Network Forensic Analysis Tool (NFAT) that performs
  deep processing and inspection of network traffic (mainly PCAP files, but it
  also capable of directly live capturing from a network interface). It
  includes: password extracting, building a network map, reconstruct TCP
  sessions, extract hashes of encrypted passwords and even convert them to a
  Hashcat format in order to perform an offline Brute Force attack.
   
  The main goal of the project is to provide solution to security researchers
  and network administrators with the task of network traffic analysis while
  they try to identify weaknesses that can be used by a potential attacker to
  gain access to critical points on the network.
   
  On Linux it is a Command Line Interface tool.
 
 **Installed size:** `80.21 MB`  
 **How to install:** `sudo apt install bruteshark`  
 
 ##### brutesharkcli
 
 
 ```
 root@kali:~# brutesharkcli -h
 Process terminated. Couldn't find a valid ICU package installed on the system. Set the configuration flag System.Globalization.Invariant to true if you want to run with no globalization support.
    at System.Environment.FailFast(System.String)
    at System.Globalization.GlobalizationMode.GetGlobalizationInvariantMode()
    at System.Globalization.GlobalizationMode..cctor()
    at System.Globalization.CultureData.CreateCultureWithInvariantData()
    at System.Globalization.CultureData.get_Invariant()
    at System.Globalization.CultureInfo..cctor()
    at System.Globalization.CultureInfo.get_CurrentCulture()
    at System.Text.RegularExpressions.Regex..ctor(System.String, System.Text.RegularExpressions.RegexOptions, System.TimeSpan, Boolean)
    at System.Text.RegularExpressions.Regex..ctor(System.String)
    at PcapAnalyzer.FtpPasswordParser..ctor()
    at System.RuntimeTypeHandle.CreateInstance(System.RuntimeType, Boolean, Boolean, Boolean ByRef, System.RuntimeMethodHandleInternal ByRef, Boolean ByRef)
    at System.RuntimeType.CreateInstanceDefaultCtorSlow(Boolean, Boolean, Boolean)
    at System.RuntimeType.CreateInstanceDefaultCtor(Boolean, Boolean, Boolean, Boolean)
    at System.Activator.CreateInstance(System.Type, Boolean, Boolean)
    at System.Activator.CreateInstance(System.Type)
    at PcapAnalyzer.PasswordsModule+<>c.<_initilyzePasswordParsersList>b__10_2(System.Type)
    at System.Linq.Enumerable+WhereSelectEnumerableIterator`2[[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]].ToList()
    at System.Linq.Enumerable.ToList[[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]](System.Collections.Generic.IEnumerable`1<System.__Canon>)
    at PcapAnalyzer.PasswordsModule._initilyzePasswordParsersList()
    at PcapAnalyzer.PasswordsModule..ctor()
    at System.RuntimeTypeHandle.CreateInstance(System.RuntimeType, Boolean, Boolean, Boolean ByRef, System.RuntimeMethodHandleInternal ByRef, Boolean ByRef)
    at System.RuntimeType.CreateInstanceDefaultCtorSlow(Boolean, Boolean, Boolean)
    at System.RuntimeType.CreateInstanceDefaultCtor(Boolean, Boolean, Boolean, Boolean)
    at System.Activator.CreateInstance(System.Type, Boolean, Boolean)
    at System.Activator.CreateInstance(System.Type)
    at PcapAnalyzer.Analyzer+<>c.<InitilyzeModulesList>b__17_2(System.Type)
    at System.Linq.Enumerable+WhereSelectEnumerableIterator`2[[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]].ToList()
    at System.Linq.Enumerable.ToList[[System.__Canon, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]](System.Collections.Generic.IEnumerable`1<System.__Canon>)
    at PcapAnalyzer.Analyzer.InitilyzeModulesList()
    at PcapAnalyzer.Analyzer..ctor()
    at BruteSharkCli.BruteSharkCli..ctor(System.String[])
    at BruteSharkCli.Program.Main(System.String[])
 Aborted
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
