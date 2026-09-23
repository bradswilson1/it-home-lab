# Ticket 003: No network connectivity

**Date:** 2026-09-22
**Category:** Networking
**Priority:** High
**Environment:** Windows 10 Home, local workstation

## Reported issue
Network not responding. Attempting to load a webpage results in error 'Internet Disconneted'. Network icon in taskbar states 'Not connected - No connections are available'.

## Environment setup
The network was intentionally disabled to simulate a period of no connectivity. Websites were attempted to load, and ipconif/all was used in command prompt to see a before and after of having the network enabled. 

## Troubleshooting steps
1. Confirmed the lack of connectivity of the network 
2. Clicked on the network taskbar icon, then clicked on Network & internet settings
3. Clicked on status, saw that my network was not listed in 'Show available networks' list
4. Went into Control Panel > Network and Internet > Network Connections, noticed my Ethernet status was disabled.
5. Enabled the Ethernet

## Root cause
The network was disabled and unable to connect

## Time to resolve
15 min

## Prevention and user education
Users can use control panel > Network and Internet to verify the status of their network. If unavailable, then user can use 'connect to a network'.
