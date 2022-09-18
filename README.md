# solarman-dissector
Wireshark dissector for the solarmanv5 cloud protocol

## Introduction
This repository provides a wireshark dissector plugin written in Lua.
This dissector has been created to analyze the communication between a Bosswerk MI600 solar inverter and the Solarman cloud server.
It should also work with similar microinverters, e.g. Bosswerk MI300, Deye SUN600G3-EU-230, Deye SUN300G3-EU-230, ...

This project should not be confused with other projects that:
* read inverter data from the solarman cloud using the solarman API,
* scrape data from the built-in webserver of the inverter,
* read data from the inverter using encapsulated Modbus/RTU protocol,
* replace the solarman cloud with a local server/proxy (see references below).

## Usage
### Overview
To make use of this plugin you need to 
* install wireshark on your computer
* install this plugin
* collect communication data
* open data in wireshark

### Install wireshark
See https://www.wireshark.org/docs/wsug_html_chunked/ChapterBuildInstall.html 

### Install plugin
See https://www.wireshark.org/docs/wsug_html_chunked/ChPluginFolders.html

### Collect communication data
The following is an example of a command that can be typed into a Linux computer to open an SSH connection to an OpenWRT router (192.168.1.1) and log data between the solar inverter (192.168.1.100) and the internet. The data will be written to *.pcap files. A new log file will automatically be created every 24 hours. As the solar inverter will only send data while the sun is shining, it is probably a good idea to use this command between sunset and sunrise to have the full data of one day written to each file.

```
ssh root@192.168.1.1 tcpdump -n -U -s0 -w - 'host 192.168.1.100 and not arp' | 
  tcpdump -r - -w ./capture_%Y-%m-%d__%H_%M_%S.pcap  -G 86400 -C 1
```

(Of course, there are many other possible ways of collecting this data. It is even possible to pipe the data directly to wireshark for real-time analysis.) 

### Open data in wireshark
Open one of the *.pcap files in wireshark. Within the whole list of messages that were captured by the router, all messages that were exchanged with port 10000 of the cloud server should be marked with the protocol SOLARMANV5. When you look at the detailed info for these messages, the plugin should translate most data into a human readable format.

## References
### Node-red server/proxy for Sofar solar wifi stick
See https://github.com/serek4/node-red-sofar-ktl-x
This repository provides a node-red server/proxy for the solarman cloud protocol. It also documents the communication between the solarman cloud server and a different inverter than the Bosswerk MI600. (Note: The protocol is similar but slightly different. The dissector plugin would have to be changed to be fully useful with that inverter.) It would be interesting to adapt this server/proxy for usage with Bosswerk MI600 inverters.
