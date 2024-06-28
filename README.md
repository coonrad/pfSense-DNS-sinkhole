# pfSense-DNS-sinkhole
pfSense DNS forwarder configuration for blocking hosts and domains.

You may find this configuration useful if you don't want to install pfBlockerNG on your firewall, or manage an external DNS sinkhole like Pi-hole. It also has the advantage of being able to manage a large number of dns overrides without having to manually add and remove them from the pfSense GUI.

## Setup

- enable DNS forwarder: [DNS Forwarder Configuration](https://docs.netgate.com/pfsense/en/latest/services/dns/forwarder-config.html)
- enable SSH to pfSense: [Enable SSH via GUI](https://docs.netgate.com/pfsense/en/latest/recipes/ssh-access.html#enable-ssh-via-gui)

ssh to the firewall to create the dnsmasq directory and script directory:

```sh
[24.03-RELEASE][admin@pf100.local]/root: mkdir bin
[24.03-RELEASE][admin@pf100.local]/root: mkdir -p /usr/local/etc/dnsmasq/dnshole
[24.03-RELEASE][admin@pf100.local]/root: mkdir /usr/local/etc/dnsmasq/hosts
```
