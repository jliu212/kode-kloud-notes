# Network Basics

`/etc/hosts` on the system has the DNS

ping, ssh, curl all look into the file and translate into the IP address.

This is called _name resolutions_.
The issue is unit direction and unmanagable.
solution is move to (Domain Name Server)DNS instad of /etc/host file.

The DNS server of in /etc/resolv.conf
/etc/nsswitch.conf has all the files that defines the hosts

/etc/resolv.conf can host public DNS servers by adding to the list of the file
You can also configure your own interal DNS for foward any unknown host names to the public DNS

## Domain Names

Top level domain: .com .net .edu .org .io

Subdomain: mail, drive, maps. apps etc...

## Record types

A record ipv4
AAAA for ipv6
Cname for multiple mapping

## Other commands

`nslookup` to look up ip from a host name
`dig host`

### Switching

need interface on the host to connect to a switch
`ip link` eth0
`ip addr add`
