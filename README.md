# IT Home Lab

Hands-on labs, projects, and documentation from my path toward a
Systems Administrator career.

## About me
Name: Bradley Wilson

Aspiring systems administrator building skills in hardware, operating
systems, networking, and automation. Currently studying for CompTIA A+.

## Lab environment
- CPU: Intel Core i5-7600K (4 cores)
- RAM: 8 GB DDR4-2400 (2 × 4 GB, dual-channel, 2 slots free)
- Motherboard: MSI Z270 SLI (4 DIMM slots, 2 M.2 slots, max 64 GB)
- Storage: 1 TB HDD
- OS: Windows 10 Home

## Progress log
- Lesson 1: Identified system hardware using Task Manager
- Lesson 2: Investigated RAM configuration, motherboard, and virtual memory
- Lesson 3: Researched CPU, motherboard, and power supply compatibility using vendor documentation
- Lesson 4: Determined both the motherboard's and graphics card's ports

## Research notes

### System research (Lesson 3)
Goal: determine upgrade options and power requirements for the lab PC.

**CPU (source: Intel ARK)**
- Socket: FCLGA1151, TDP: 91 W
- Supported memory: DDR4-2133/2400 (the board has DDR4 slots only)
- Max memory: 64 GB, matching the motherboard limit

**Storage upgrade path (source: MSI Z270 SLI manual)**
- Both M.2 slots support PCIe 3.0 x4 NVMe and SATA 6 Gb/s drives
- Port conflict: an M.2 SATA drive disables SATA1 and SATA5;
  an M.2 NVMe drive disables SATA5 and SATA6
- Action item: confirm which SATA port the existing HDD uses and
  move it to SATA2, 3, or 4 before installing an M.2 drive

**Power requirements (source: Newegg PSU calculator)**
- Recommended: 393 W. The exact motherboard was not listed, so a
  generic ATX board was selected; boards draw roughly 25-50 W, so
  the substitution has minimal impact.
- Conclusion: the existing PSU is adequate. No upgrade needed.

**Recommended upgrades, in priority order**
1. SSD (SATA or NVMe): largest real-world speed improvement over the 7200 RPM HDD
2. RAM to 16 GB: needed to run multiple VMs at once

**Port Inventory**
- Motherboard: Two USB 2.0, PS/2 Combo, DVI, SuperSpeed (SS) USB 3.0/3.1, HDMI,
  Two USB 3.0/3.1, Ethernet,  Two USB 3.0/3.1, Audio jacks
- Graphics Card: Display, DVI-D, HDMI, DVI-I
- The current monitor is using the display port on the NVIDIA GeForce GTX 750 Ti.
- The current resolution is 1600x900, and has a refresh rate of 59.978 Hz.
