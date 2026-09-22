# Ticket 002: No audio output

**Date:** 2026-09-22
**Category:** OS / services
**Priority:** Medium
**Environment:** Windows 10 Home, local workstation

## Reported issue
Audio not playing from speakers. Only visible message from the application Spotify, just simply says the program can't currently play audio. Speak icon in the taskbar currently has red 'X' displayed, as well as when mouse hovers over icon the message 'The Audio service is not running' appears. 

## Troubleshooting steps
1. Confirmed speakers were not set to 'mute'
2. Opened Services > Windows Audio > Properties and confirmed status is not running
3. Right-clicked Windows Audio, clicked properties
4. Startup type is set to Automatic
5. Service status is Stopped
6. Clicked Start 

## Root cause
The Windows Audio service had been stopped and just needed to be started.

## Time to resolve
5 minutes

## Prevention and user education
Users can be shown how to check Windows services to see if programs have a running status before escalating. A stopped service is a common cause of "feature X suddenly doesn't work", and Automatic startup means it should come back after a reboot. 

## Notes
Windows services is available for any user, the audio icon in taskbar also displayed a message that started services was the problem area. Standard users will be able to notice if a program is A) has a status of running and B) the startup type which can consist of Manual, Automatic, Disabled.
