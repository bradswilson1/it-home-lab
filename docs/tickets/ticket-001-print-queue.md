# Ticket 001: Print jobs stuck in queue

**Date:** 2026-09-22
**Category:** Printers
**Priority:** Medium
**Environment:** Windows 10 Home, local workstation

## Reported issue
Documents sent to the network printer never print. No error message
appears in the application, and additional print attempts have no effect.

## Environment setup
A network printer was configured pointing to an unreachable IP address
(192.168.254.254) to simulate an offline printer. Three print jobs were
submitted from Notepad.

## Troubleshooting steps
1. Confirmed the symptom: no error in the application, nothing printed.
2. Opened Settings > Devices > Printers & scanners and confirmed the
   printer was installed.
3. Opened the print queue and found three jobs waiting, with an error
   status on the first job.
4. Noted that Pause Printing was unavailable under standard user
   permissions; reopened the queue using Printer > Open As Administrator.
5. Cancelled all documents in the queue.
6. Opened Services and restarted the Print Spooler service to clear any
   remaining jobs.

## Root cause
The printer was unreachable at its configured address. Jobs accumulated
in the print queue, and the job at the front blocked everything behind it.

## Resolution
Cleared the print queue and restarted the Print Spooler service. Verified
the queue was empty and the spooler was running.

## Time to resolve
15 minutes

## Prevention and user education
Users can be shown how to check the print queue for stuck jobs before
escalating. Clearing the queue and restarting the Print Spooler resolves
a large share of printing issues.

## Notes
Managing the print queue and restarting services requires administrative
rights, which standard users do not have. This is by design in a business
environment.
