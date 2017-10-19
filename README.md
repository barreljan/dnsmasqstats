# dnsmasqstats(.py)
> dnsmasq statistics, top usage

### Introduction
This is a simple script that helps you understand the requests made to your DNSMasq server. 
It could be helpfull to see which clients requests the most, what record types are queried the most and the request itself.

### How to use
The help function describes all just download or clone and start the it with:
  ./dnsmasqstats
  
For the fun of it, below the 'help' output:
```
Usage: dnsmasqstats -option arguments

Available options:

-h, --help

-a, --all <NR>                          Displays all with optional number of lines per class
-c, --clients <NR>                      Displays clients (descending) with optional number of lines
-i, --inputfile <input_filename>        Differ from the default log file
-r, --records <NR>                      Displays the requested records with optional number of lines
-t, --types                             Displays the types

The default number to display is 10 and displays all classes.

Examples:
dnsmasqstats -c 10                              Shows a top 10 of requesting clients/hosts
dnsmasqstats -r 25 -i /var/log/dnsmasq.1        Shows a top 25 of requested records from the rotated logfile
```


### Example
An example of output of './dnsmasqstats':

```
Displaying all, set to 10 lines

192.168.100.10                          57695
192.168.0.14                            1850
192.168.1.8                             1438
192.168.1.2                             685
192.168.0.7                             535
192.168.0.25                            429
192.168.0.3                             201
192.168.105.1                           154
192.168.1.102                           101
192.168.0.13                            83

A                                       42965
AAAA                                    15780
PTR                                     5759
TXT                                     708
SRV                                     115
SOA                                     32
NS                                      1
MX                                      1

cdn.onenote.net                         48
eas.outlook.com                         46
chart.apis.google.com                   44
nexus.officeapps.live.com               43
safebrowsing.googleapis.com             36
nexusrules.officeapps.live.com          34
aax-eu.amazon-adsystem.com              34
cl2-cdn.origin-apple.com.akadns.net     32
teredo.ipv6.microsoft.com               27
login.live.com                          27
```
