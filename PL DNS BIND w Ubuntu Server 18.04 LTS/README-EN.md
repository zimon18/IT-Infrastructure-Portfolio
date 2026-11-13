# BIND DNS Lab on Ubuntu Server 18.04

An educational virtual lab documenting the setup of a BIND9 DNS server with forward and reverse lookup zones, two network interfaces, and Linux and Windows clients.

## Lab scope

- Configured a server with NAT access and an internal lab network.
- Assigned a static address to the internal interface.
- Installed BIND9 and configured forwarders and DNS zones.
- Added host records and reverse lookup records for lab clients.
- Checked the service and queried records with `dig`, `nslookup`, and `ping`.
- Investigated a resolver configuration issue and verified name resolution from clients.

## Environment

- Ubuntu Server 18.04 LTS
- VirtualBox
- BIND9
- One Windows client and one Ubuntu client

## Evidence and original walkthrough

The full step-by-step walkthrough, with screenshots, is available in [readme.md](readme.md). It was written in Polish and is preserved as the original lab record.

## Limitations

This is a historical learning exercise on Ubuntu 18.04, which is no longer a current server platform. Network and resolver configuration details are specific to that lab. Do not apply them to a production system without checking current Ubuntu and BIND documentation. The original notes include manual resolver-file changes that should be treated as troubleshooting history, not recommended general practice.
