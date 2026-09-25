# IT Fundamentals

System research (Lesson 3)
Goal: determine upgrade options and power requirements for the lab PC.

CPU (source: Intel ARK)

Socket: FCLGA1151, TDP: 91 W
Supported memory: DDR4-2133/2400 (the board has DDR4 slots only)
Max memory: 64 GB, matching the motherboard limit
Storage upgrade path (source: MSI Z270 SLI manual)

Both M.2 slots support PCIe 3.0 x4 NVMe and SATA 6 Gb/s drives
Port conflict: an M.2 SATA drive disables SATA1 and SATA5; an M.2 NVMe drive disables SATA5 and SATA6
Action item: confirm which SATA port the existing HDD uses and move it to SATA2, 3, or 4 before installing an M.2 drive
Power requirements (source: Newegg PSU calculator)

Recommended: 393 W. The exact motherboard was not listed, so a generic ATX board was selected; boards draw roughly 25-50 W, so the substitution has minimal impact.
Conclusion: the existing PSU is adequate. No upgrade needed.
Recommended upgrades, in priority order

SSD (SATA or NVMe): largest real-world speed improvement over the 7200 RPM HDD
RAM to 16 GB: needed to run multiple VMs at once
Port inventory (Lesson 4)
Motherboard: two USB 2.0, PS/2 combo, DVI, SuperSpeed USB 3.0/3.1, HDMI, four USB 3.0/3.1, Ethernet, audio jacks
Graphics card: DisplayPort, DVI-D, HDMI, DVI-I
The monitor connects via DisplayPort to the NVIDIA GeForce GTX 750 Ti
Current resolution 1600x900 at 59.978 Hz
Note: DVI-I carries analog as well as digital, so it supports a passive VGA adapter; DVI-D does not
