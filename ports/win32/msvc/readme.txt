lwIP for Win32

This is a quickly hacked port and example project of the lwIP library to
Win32/MSVC9.

It doesn't (yet?) include support for dhcp, autoip, slipif, ppp or pppoe. This
is simply because none of the active developers using this port are using these
interfaces right now.

To get this compiling
- the lwIP core repository must be in a folder "lwip" next to the "contrib" folder
- you have to set an environment variable PCAP_DIR pointing to the WinPcap Developer's
  Pack (containing 'include' and 'lib')

You also will have to copy the file 'lwipcfg_msvc.h.example' to
'lwipcfg_msvc.h' and modify to suit your needs (WinPcap adapter number,
IP configuration, applications...).

Included in the contrib\ports\win32 directory is the network interface driver
using the winpcap library.

lwIP: http://savannah.nongnu.org/projects/lwip/
WinPCap: http://netgroup-serv.polito.it/winpcap/

To compile the unittests, download check (tested with v0.11.0) from
https://github.com/libcheck/check/releases/
and place it in a folder "check" next to the "contrib" folder.