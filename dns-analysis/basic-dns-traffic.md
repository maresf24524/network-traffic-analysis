# Basic DNS Traffic Analysis

DNS (Domain Name System) translates domain names into IP addresses.
Example:
User requests:
google.com
DNS server responds with:
142.250.74.14

## Wireshark filter
dns

## What to observe
- query name
- response IP address
- response time
- unusual domain names

## Security relevance
DNS traffic can reveal:
- malware communication
- DNS tunneling
- suspicious domains
