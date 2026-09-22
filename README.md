# IT Home Lab

Hands-on labs, projects, and documentation from my path toward a
Systems Administrator career.

## About me

Name: Bradley Wilson

Aspiring systems administrator building skills in hardware, operating
systems, networking, and automation. Currently studying for CompTIA A+.

## Lab environment

- CPU: Intel Core i5-7600K (4 cores, socket FCLGA1151)
- RAM: 8 GB DDR4-2400 (2 x 4 GB, dual-channel, 2 slots free)
- Motherboard: MSI Z270 SLI (4 DIMM slots, 2 M.2 slots, max 64 GB)
- GPU: NVIDIA GeForce GTX 750 Ti
- Storage: 1 TB HDD (7200 RPM)
- OS: Windows 10 Home

## Progress log

- Lesson 1: Identified system hardware using Task Manager
- Lesson 2: Investigated RAM configuration, motherboard, and virtual memory
- Lesson 3: Researched CPU, motherboard, and power supply compatibility
  using vendor documentation
- Lesson 4: Inventoried motherboard and graphics card ports and verified
  the active display adapter in Windows
- Lesson 5: Simulated an offline network printer, cleared a stuck print
  queue, and restarted the Print Spooler service

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
- Action item: confirm which SATA port the existing HDD uses and move it
  to SATA2, 3, or 4 before installing an M.2 drive

**Power requirements (source: Newegg PSU calculator)**
- Recommended: 393 W. The exact motherboard was not listed, so a generic
  ATX board was selected; boards draw roughly 25-50 W, so the
  substitution has minimal impact.
- Conclusion: the existing PSU is adequate. No upgrade needed.

**Recommended upgrades, in priority order**
1. SSD (SATA or NVMe): largest real-world speed improvement over the
   7200 RPM HDD
2. RAM to 16 GB: needed to run multiple VMs at once

### Port inventory (Lesson 4)

- Motherboard: two USB 2.0, PS/2 combo, DVI, SuperSpeed USB 3.0/3.1,
  HDMI, four USB 3.0/3.1, Ethernet, audio jacks
- Graphics card: DisplayPort, DVI-D, HDMI, DVI-I
- The monitor connects via DisplayPort to the NVIDIA GeForce GTX 750 Ti
- Current resolution 1600x900 at 59.978 Hz
- Note: DVI-I carries analog as well as digital, so it supports a passive
  VGA adapter; DVI-D does not
