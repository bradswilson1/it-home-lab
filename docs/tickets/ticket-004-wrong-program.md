# Ticket 004: Files opening in the wrong program

**Date:** 2026-09-22
**Category:** OS / applications
**Priority:** Medium
**Environment:** Windows 10 Home, local workstation

## Reported issue
When attempting to open a text file, the wrong program runs and tries to open said file. 

## Environment setup
A test text file was created on windows desktop. Chose to open file with 'WordPad', this caused all text files to now be opened with 'WordPad' rather than 'Notepad'.   

## Troubleshooting steps
1. Verified what program the text file runs in by double clicking the text file to open it. 
2. Opened Settings > Apps > Default Apps ![Settings then Apps](../images/ticket-004-apps.png)
![Then default apps](../images/ticket-004-default-apps.png)
3. Clicked 'Choose default apps by file type', and scrolled down to .txt ![choose default by type](../images/ticket-004-default-by-type.png)
4. WordPad is set as default app for .txt files
5. Clicked WordPad, this opened up a list of apps to choose from. 
6. Chose Notepad as the default app for .txt files. ![Choose new default app](../images/ticket-004-default-txt.png)
7. Verified .txt files were being opened in Notepad by opening a .txt file

## Root cause
The default program had been changed for a single .txt file, this caused the chosen program to now be the default for all .txt files. 

## Resolution
Went into Settings > Apps > Default Apps, changed the default app for .txt files to Notepad.

## Time to resolve
10 min

## Prevention and user education
Users can open a file in a different program without changing the default by right-clicking, choosing Open with, and leaving the 'Always use this app' box unchecked

## Notes
Right-clicking and choosing "Open with" opens a file once in the selected program without changing anything. The default only changes if "Always use this app" is checked in that dialog, which users often select without realizing it applies to every file of that type going forward.
