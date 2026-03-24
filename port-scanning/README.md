# Port Scanning Traffic Analysis (nmap + wireshark)

## Objective
The goal of this lab was to observe how a port scan looks on the network level and analyze the traffic using Wireshark

## Tools used
- nmap
- Wireshark
- PowerShell
- Local LAN Network

## Environment
- Windows 11 host
- Local Network (192.168.xx.xx/24)
- Target device 192.168.xx.xx (router)

## Scan commands

Basic fast scan: 

nmap -F 192.168.xx.xx

SYN scan: 

nmap -sS 192.168.xx.xx

HOST scan 

nmap -sn 192.168.xx.xx/24

## Observation in Wireshark

When filtering TCP traffic, a clear port scanning pattern can be observed

Example pattern:

SYN -> port 21
SYN -> port 22
SYN -> port 23
SYN -> port 80

Server responses:

RST, ACK -> port closed
SYN, ACK -> port open

Large amount of SYN packets in a short time period indicate reconnaissance activity

## Open Ports Detected

53/tcp - DNS
80/tcp - HTTP

These services were running on the target device

## Detection insight

Port scanning creates a recognizable traffic patterns:

- high number of SYN packets
- many different destination ports
- very short time interval

This pattern can be detected by nentwork monitoring tools

## Learning outcome

This lab helped me understand:

- how port scanning works
- how SYN scanning behaves on the network level
- how to identify scanning activity in Wireshark
- how reconnaissance activity appears in packet captures

## Work Environment

- Windows 11 host
- WSL environment
- Local LAN Network
- Target device : home router

## Notes and Additional Screenshots

This lab was repeated to capture clearer traffic patterns and improve analysis
The screenshots were taken later to better demonstrate th traffic patterns and analysis.
