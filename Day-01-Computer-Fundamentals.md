 📚 Day 1 — Computer Fundamentals
> Phase 1 – Foundations | Date: 19 July 2026  
> Author: Haseeb | GitHub(https://github.com/HaseebCybersec) | IMSciences, Peshawar  
> Status: ✅ Completed



 📋 Topics Covered
1. What is a Computer?
2. Hardware vs. Software
3. Input, Output, Processing, Storage
4. CPU – Central Processing Unit
    ALU
    Control Unit
    Registers
    Cache
5. RAM vs. ROM
6. HDD vs. SSD
7. Motherboard
8. GPU
9. Power Supply Unit
10. BIOS / UEFI
11. Operating Systems – Introduction
12. Binary and Hexadecimal



 1. What is a Computer?

 📖 Definition
A computer is an electronic device that accepts data (input), processes it according to instructions, stores results, and produces output.

 🔑 Key Components
 Input devices (keyboard, mouse, network card)
 Processing unit (CPU)
 Memory (RAM, ROM)
 Storage (SSD, HDD)
 Output devices (monitor, speaker)

 ⚙️ How it Works
```
INPUT → PROCESSING → OUTPUT
              ↕
           STORAGE
```

 📌 Important Terms
| Term | Meaning |
|||
| Data | Raw facts — numbers, text, files |
| Information | Processed, meaningful data |
| Program | Set of instructions for the computer |
| IPO Model | Input → Processing → Output |

 🔐 Cybersecurity Example
You enter a password (INPUT) → server hashes and compares it (PROCESSING) → grants or denies access (OUTPUT) → logs the attempt to disk (STORAGE). Attackers target every stage of this flow.

 ✅ Summary
A computer does exactly what it is instructed — nothing more, nothing less. Bad instructions = bad outcomes. This is why cybersecurity exists.

 
  



 2. Hardware vs. Software

 📖 Definition
 Hardware — physical components you can touch (CPU, RAM, SSD)
 Software — instructions (programs) that tell hardware what to do

 🔑 Key Components
Hardware: CPU, RAM, SSD, motherboard, keyboard, monitor, network card  
Software types:
 System software — OS, drivers, BIOS/UEFI
 Application software — browser, Wireshark, Nmap, VS Code
 Malicious software — viruses, ransomware, trojans, spyware

 ⚙️ How it Works
```
YOU (user)
    ↓
APPLICATION SOFTWARE  (Nmap, browser, terminal)
    ↓
OPERATING SYSTEM      (Windows, Linux, macOS)
    ↓
HARDWARE              (CPU, RAM, Storage, Network card)
```

 📌 Important Terms
| Term | Meaning |
|||
| Driver | Software letting OS communicate with specific hardware |
| Firmware | Software permanently stored in hardware (e.g. BIOS) |
| Malware | Malicious software designed to exploit or damage |
| Volatile | Loses data when power is off (RAM) |
| Nonvolatile | Keeps data without power (SSD, ROM) |

 🔐 Cybersecurity Example
Almost every cyberattack targets software, not hardware. A hacker finds a bug in a web application's code (software) and exploits it — without ever touching the physical server (hardware).

 ✅ Summary
Hardware is useless without software. Software is powerless without hardware. Security vulnerabilities live in the software layer.

 
  



 3. Input, Output, Processing, Storage

 📖 Definition
The four fundamental operations of every computer — how data enters, gets processed, gets stored, and results are produced.

 🔑 Key Components
| Operation | Examples |
|||
| Input | Keyboard, mouse, network packets, USB, microphone |
| Processing | CPU executing instructions |
| Output | Monitor, speakers, outgoing network packets |
| Storage | RAM (temporary), SSD/HDD (permanent) |

 ⚙️ How it Works
Example — logging into a website:
1. You type password → INPUT
2. CPU hashes and compares password → PROCESSING
3. Screen shows "Login successful" → OUTPUT
4. Session saved in RAM, log saved to SSD → STORAGE

 📌 Important Terms
| Term | Meaning |
|||
| I/O Device | Input/Output device — does both (e.g. network card) |
| Buffer | Temporary storage area during data transfer |
| Throughput | How much data is processed per second |
| Latency | Delay between input and output |

 🔐 Cybersecurity Example
SQL Injection attacks the INPUT stage. A hacker types malicious SQL code into a login field. If the app doesn't validate input, the malicious code gets processed and attacks the database. Rule: Never trust user input.

 ✅ Summary
Security vulnerabilities exist at every stage — INPUT (injection attacks), PROCESSING (logic flaws), OUTPUT (information disclosure), STORAGE (data breaches).

 
  



 4. CPU — Central Processing Unit

 📖 Definition
The brain of the computer. Executes every instruction from every program running on the system.



 4a. ALU — Arithmetic Logic Unit

 📖 Definition
Performs all calculations and logical decisions inside the CPU.

 ⚙️ How it Works
 Arithmetic: addition, subtraction, multiplication, division
 Logic: comparisons — is A = B? Is X > Y? → YES / NO

 📌 Important Terms
| Term | Meaning |
|||
| Operand | The value being operated on |
| Boolean logic | AND, OR, NOT — true/false outcomes |
| Bitwise operation | Operations on individual bits |

 🔐 Cybersecurity Example
Brute force attacks make the ALU perform billions of password comparisons per second — trying every possible combination until one matches.



 4b. Control Unit (CU)

 📖 Definition
Manages and directs all CPU operations — the manager of the CPU.

 ⚙️ How it Works — FetchDecodeExecute Cycle
```
FETCH   → Get instruction from RAM
   ↓
DECODE  → Understand what it means
   ↓
EXECUTE → Carry out the instruction
   ↓
REPEAT  → Billions of times per second
```

 📌 Important Terms
| Term | Meaning |
|||
| Instruction set | All commands a CPU understands |
| Clock speed | Cycles per second — GHz = billion cycles/sec |
| Pipeline | Processing multiple instructions simultaneously |

 🔐 Cybersecurity Example
When you run Nmap, the Control Unit manages thousands of instructions per second — sending packets, receiving responses, logging results.



 4c. Registers

 📖 Definition
Tiny, extremely fast memory locations built directly inside the CPU that hold data being actively used right now.

 ⚙️ How it Works
CPU loads values into registers → performs the operation → stores result. Registers are faster than any other memory in the system.

 📌 Important Terms
| Register | Purpose |
|||
| Program Counter (PC) | Address of the NEXT instruction to execute |
| Accumulator | Holds ALU operation results |
| Instruction Register (IR) | Holds current instruction being executed |
| Memory Address Register (MAR) | Address in RAM being accessed |
| Memory Data Register (MDR) | Data being moved to/from RAM |

 🔐 Cybersecurity Example
Buffer overflow attacks overwrite the Program Counter register. If an attacker controls the PC, they control which instruction the CPU runs next — hijacking the entire program. This is one of the most fundamental exploit techniques.



 4d. Cache

 📖 Definition
Small, very fast memory built into the CPU that stores frequently used data to avoid slow RAM accesses.

 ⚙️ How it Works
```
CPU needs data
     ↓
L1 Cache → Hit? Use it ✅  |  Miss? ↓
     ↓
L2 Cache → Hit? Use it ✅  |  Miss? ↓
     ↓
L3 Cache → Hit? Use it ✅  |  Miss? ↓
     ↓
RAM → Fetch from here (slower) ⚠️
```

 📌 Important Terms
| Level | Size | Speed |
||||
| L1 Cache | 32–64 KB | Fastest |
| L2 Cache | 256 KB – 1 MB | Very fast |
| L3 Cache | 4–64 MB | Fast |
| RAM | 8–64 GB | Slower |

| Term | Meaning |
|||
| Cache hit | Data found in cache → fast |
| Cache miss | Data not in cache → fetch from RAM |

 🔐 Cybersecurity Example
Spectre & Meltdown (2018) exploited cache timing to read protected memory. By measuring how long cache hits vs misses take, attackers extracted encryption keys from memory they were never supposed to access. Affected nearly every CPU built in the last 20 years.



 ✅ CPU Summary
| Component | Role |
|||
| ALU | Math and logic operations |
| Control Unit | Manages fetchdecodeexecute cycle |
| Registers | Fastest storage — holds active data |
| Cache | Bridges speed gap between CPU and RAM |

 
  



 5. RAM vs. ROM

 📖 Definition
 RAM (Random Access Memory) — fast, temporary working memory. Lost when power is off
 ROM (Read Only Memory) — permanent memory. Keeps data without power. Stores BIOS/UEFI

 🔑 Key Components
 RAM: memory sticks in motherboard slots — holds active OS + running apps
 ROM: small flash chip on motherboard — holds boot firmware

 ⚙️ How it Works
RAM:
```
Power ON → OS loads from SSD into RAM
App opens → loaded from SSD into RAM
CPU works → reads/writes directly to RAM
Power OFF → RAM wiped completely
```
ROM:
```
Power ON → CPU reads ROM first
ROM runs POST (hardware check)
ROM finds boot drive
ROM hands control to OS bootloader
```

 📌 Important Terms
| Term | Meaning |
|||
| Volatile | Loses data without power (RAM) |
| Nonvolatile | Keeps data without power (ROM, SSD) |
| EEPROM | Electrically Erasable ROM — can be updated |
| Firmware | Software stored in ROM/flash |
| Firmware update | Rewriting the ROM chip with new code |

 🔐 Cybersecurity Example
 RAM — Mimikatz: Extracts plaintext passwords from RAM (Windows LSASS process). Works because Windows keeps auth credentials in active memory. Defence: enable Windows Credential Guard.
 ROM — LoJax (2018): First UEFI rootkit found in the wild. Written into UEFI flash (modern ROM). Survived complete OS reinstallation and even hard drive replacement.

 ✅ Summary
RAM = your desk (fast, temporary, cleared on shutdown). ROM = instructions printed on the desk (permanent, always there). Attackers target RAM for live credentials, ROM for deep persistent access.

 
  



 6. HDD vs. SSD

 📖 Definition
 HDD (Hard Disk Drive) — storage using spinning magnetic platters and a moving read/write head
 SSD (Solid State Drive) — storage using flash memory chips with no moving parts

 🔑 Key Components
 HDD: spinning platter, read/write arm, magnetic coating, motor
 SSD: NAND flash chips, controller chip — no moving parts

 ⚙️ How it Works
HDD:
```
Data requested → arm physically moves to correct disk position
→ magnetic head reads 0s and 1s → sends to RAM → CPU uses it
```
SSD:
```
Data requested → controller reads from flash memory cells electrically
→ sends to RAM → CPU uses it (nearinstant, no movement)
```

 📌 Important Terms
| Term | Meaning |
|||
| TRIM | SSD feature — wipes deleted data immediately |
| Sector | Smallest HDD storage unit (512 bytes) |
| RPM | Rotations per minute — HDD speed (7200 RPM = faster) |
| NVMe | Fastest SSD — connects via PCIe (up to 7,000 MB/s) |
| SATA SSD | Slower SSD — connects via SATA port (500 MB/s) |
| File slack | Unused space at end of a sector — can hide forensic data |

 🔐 Cybersecurity Example
 HDD Forensics: Deleting a file only removes the pointer. Data stays on the magnetic platter until overwritten. Tool: Autopsy recovers "deleted" files — used in criminal investigations.
 SSD Forensics: TRIM immediately wipes deleted data blocks — making file recovery nearly impossible. Investigators must capture SSD data while powered on.

 ✅ Summary
| Feature | HDD | SSD |
||||
| Speed | Slow (100–150 MB/s) | Fast (500–7000 MB/s) |
| Moving parts | Yes — fragile | No — durable |
| Price | Cheap | More expensive |
| File recovery | Easy (data lingers) | Hard (TRIM wipes fast) |
| Best for | Bulk storage | OS drive, performance |

 
  



 7. Motherboard

 📖 Definition
The main circuit board that physically connects and allows communication between all computer components.

 🔑 Key Components
| Component | Purpose |
|||
| CPU Socket | Where CPU is installed (LGA1700, AM5) |
| RAM Slots | Where RAM sticks plug in (2–4 slots) |
| PCIe Slots | GPU, NVMe SSD, network cards |
| SATA Ports | SATA SSD and HDD connections |
| BIOS/UEFI Chip | Stores boot firmware |
| Chipset | Controls data flow between CPU and components |
| CMOS Battery | Keeps BIOS settings and clock alive when PC is off |
| 24pin Power | Main power connector from PSU |

 ⚙️ How it Works
```
PSU → powers motherboard
CPU → sits in socket → communicates via chipset
RAM → plugs into slots → CPU accesses directly
SSD/HDD → connects via SATA or PCIe
GPU → plugs into PCIe x16 slot
All components ↔ communicate through motherboard traces
```

 📌 Important Terms
| Term | Meaning |
|||
| Form factor | Motherboard size standard (ATX, MicroATX, MiniITX) |
| Chipset | Controls bandwidth and speed between components |
| CMOS | Small memory storing BIOS settings (batterypowered) |
| PCIe | Highspeed connection standard (GPU, NVMe) |
| SATA | Connection standard for HDDs and SATA SSDs |

 🔐 Cybersecurity Example
 CMOS Battery Reset: Removing the battery resets BIOS — including BIOS passwords. Physical access = game over for software protections.
 Cold Boot Attack: RAM retains data for seconds after power loss (especially when cooled). Attackers remove RAM sticks and read them on another machine — extracting encryption keys from BitLocker/FileVault.

 ✅ Summary
The motherboard is the backbone connecting everything. Physical access to the motherboard bypasses almost all softwarelevel security — which is why physical security is the foundation of all security.

 
  



 8. GPU — Graphics Processing Unit

 📖 Definition
A specialized processor with thousands of small cores designed for parallel computing — doing many simple tasks simultaneously.

 🔑 Key Components
 Thousands of small GPU cores (vs CPU's few powerful cores)
 VRAM — GPU's own dedicated fast memory
 Shader processors — handle parallel calculations
 Display outputs — HDMI, DisplayPort

 ⚙️ How it Works
```
CPU: 8–32 powerful cores → best at complex sequential tasks
GPU: 3,000–16,000 small cores → best at thousands of simple tasks at once
```
Rendering pixels, training AI models, and cracking passwords are all highly parallel tasks — perfect for GPU.

 📌 Important Terms
| Term | Meaning |
|||
| VRAM | GPU's own RAM (4–24 GB) — stores textures and frame data |
| CUDA | NVIDIA's parallel computing platform |
| OpenCL | Open standard for GPU computing (AMD + NVIDIA) |
| Hash rate | Password guesses per second |
| Parallel processing | Doing many operations simultaneously |

 🔐 Cybersecurity Example
Password cracking with Hashcat:
| Hardware | MD5 Guesses/Second |
|||
| CPU | ~1 million/sec |
| RTX 4090 GPU | ~164 billion/sec |

A GPU is 164,000x faster than a CPU at cracking password hashes. An 8character password a CPU takes 10 years to crack — a GPU cracks in under 1 hour.

> Tool you will use: Hashcat — world's most powerful password recovery tool. Runs on GPU. Covered in Phase 3.

 ✅ Summary
GPU = massively parallel processor. CPU handles complex thinking. GPU handles massive repetition at speed. In cybersecurity, GPU power is used for cracking password hashes at speeds impossible for a CPU.

 
  



 9. Power Supply Unit (PSU)

 📖 Definition
Converts alternating current (AC) from the wall socket into direct current (DC) voltages that computer components require.

 🔑 Key Components
 Transformer — steps down voltage
 Rectifier — converts AC to DC
 Output cables — 24pin ATX, CPU 8pin, PCIe 8pin, SATA power

 ⚙️ How it Works
```
Wall socket: 220V AC (Pakistan)
        ↓
PSU converts to:
  → 12V DC  (CPU, GPU, fans, drives)
  → 5V DC   (USB ports, some chips)
  → 3.3V DC (RAM, motherboard chips)
```

 📌 Important Terms
| Term | Meaning |
|||
| Wattage | Total power PSU delivers (450W, 650W, 850W) |
| 80+ Rating | Efficiency rating (Bronze 82%, Gold 90%, Platinum 92%) |
| Modular PSU | Only attach cables you need — cleaner build |
| UPS | Uninterruptible Power Supply — battery backup |
| Ripple | AC fluctuation in DC output — too much damages hardware |

 🔐 Cybersecurity Example
Power Analysis / SideChannel Attack: Sophisticated attackers measure tiny fluctuations in a device's power consumption to extract cryptographic keys. Used against hardware security modules (HSMs) and smart cards.

Practical (Pakistanspecific): Power fluctuations are common. A UPS protects your hardware and prevents data corruption during security labs.

 ✅ Summary
PSU powers everything. Without stable, sufficient power — crashes, data corruption, hardware damage. For a GPUbased password cracking machine, PSU selection is critical.

 
  



 10. BIOS / UEFI

 📖 Definition
 BIOS (Basic Input/Output System) — firmware stored in ROM, first software to run at poweron
 UEFI (Unified Extensible Firmware Interface) — modern replacement for BIOS with advanced security features

 🔑 Key Components
 Firmware chip (flash memory on motherboard)
 POST — PowerOn Self Test routine
 Boot manager — selects which drive to boot from
 Setup interface — settings you can configure
 CMOS — stores your settings between boots

 ⚙️ How it Works
```
Power button pressed
        ↓
BIOS/UEFI chip activates (before anything else on the system)
        ↓
POST — checks CPU, RAM, keyboard, storage
        ↓
Hardware initialized
        ↓
Boot device selected (SSD, USB, network)
        ↓
Bootloader loaded from drive
        ↓
OS (Windows / Linux) takes control
```

 📌 Important Terms
| Term | Meaning |
|||
| POST | PowerOn Self Test — hardware check at startup |
| Boot order | Which drive BIOS checks first for OS |
| Secure Boot | UEFI feature — only runs digitally signed bootloaders |
| CMOS | Memory holding BIOS settings (cleared by removing battery) |
| Beep codes | Audio error signals from BIOS during POST failure |
| MBR | Master Boot Record — old partition style (BIOS era) |
| GPT | GUID Partition Table — modern partition style (UEFI) |

 🔐 Cybersecurity Example
Kali Linux setup (Phase 2):
1. Press F2 / DEL / F10 at startup → enter UEFI
2. Disable Secure Boot (otherwise Kali USB won't boot)
3. Change Boot Order — set USB as first device
4. Save and exit → boot into Kali Linux

LoJax UEFI Rootkit (2018):  
First known UEFI rootkit in the wild. Written directly into UEFI flash chip. Survived complete OS reinstallation, new hard drive, full disk wipe. Only removal: physically reflash the firmware chip. Most dangerous persistence mechanism known.

 ✅ Summary
BIOS/UEFI runs before everything — before the OS, before any software security. It controls Secure Boot, hardware init, and boot device selection. You will interact with UEFI constantly as a security professional.

 
  



 11. Operating Systems — Basic Introduction

 📖 Definition
System software that manages all computer hardware, provides services for applications, and acts as the interface between the user and hardware.

 🔑 Key Components
| Component | Role |
|||
| Kernel | Core of OS — directly controls hardware |
| Shell | Interface between user and kernel (GUI or CLI) |
| File System | How files are organized and stored |
| Process Manager | Controls which programs run and when |
| Memory Manager | Controls how RAM is shared between apps |
| Device Drivers | Lets OS talk to hardware |

 ⚙️ How it Works
```
YOU (user)
    ↓
SHELL  (Windows desktop GUI or Linux terminal CLI)
    ↓
OS KERNEL  (core — manages everything below)
    ↓
HARDWARE  (CPU, RAM, Storage, Network)
```
The kernel is the only software with direct hardware access. Everything else goes through it.

 📌 Important Terms
| Term | Meaning |
|||
| Kernel | Core of OS — direct hardware access |
| Shell | Interface for user to send commands to OS |
| Process | A running program in memory |
| Thread | A subtask within a process |
| File system | How OS organizes files (NTFS, ext4, FAT32) |
| Privilege levels | Ring 0 (kernel/highest) to Ring 3 (user apps/lowest) |
| System call | How apps request services from the kernel |

 🔐 Cybersecurity Example
Privilege Escalation:  
Normal users run at Ring 3 (lowest privileges). Kernel runs at Ring 0 (highest). A privilege escalation attack exploits a vulnerability to jump from Ring 3 to Ring 0 — giving an attacker full system control. One of the most common postexploitation techniques covered in Phase 3 and 4.

OS you will use:
| OS | Purpose |
|||
| Windows 10/11 | Target machine — learn to attack and defend |
| Ubuntu Linux | Learn Linux fundamentals |
| Kali Linux | Hacking platform — all tools preinstalled |

 ✅ Summary
The OS is the manager of the entire computer. The kernel is its core. Without understanding processes, memory management, file systems, and privilege levels — you cannot understand how attacks work or how to defend against them.

 
  



 12. Binary and Hexadecimal

 📖 Definition
 Binary (Base 2) — number system using only 0 and 1. The native language of all computers
 Hexadecimal (Base 16) — number system using 0–9 and A–F. Humanreadable shorthand for binary

 🔑 Key Components
| Term | Meaning |
|||
| Bit | Single binary digit (0 or 1) |
| Byte | 8 bits grouped together |
| Nibble | 4 bits — equals exactly one hex digit |
| LSB | Least Significant Bit — rightmost bit |
| MSB | Most Significant Bit — leftmost bit |

 ⚙️ How it Works

Binary place values (8bit):
```
Position: 128  64  32  16   8   4   2   1
```

Convert 45 → Binary:
```
32 + 8 + 4 + 1 = 45
Position: 128  64  32  16   8   4   2   1
Bit:         0   0   1   0   1   1   0   1
Result: 0010 1101
```

Convert binary 1010 0110 → Decimal:
```
Position: 128  64  32  16   8   4   2   1
Bit:         1   0   1   0   0   1   1   0
128 + 32 + 4 + 2 = 166
```

Hex conversion table:
| Decimal | Binary | Hex |
||||
| 0 | 0000 | 0 |
| 9 | 1001 | 9 |
| 10 | 1010 | A |
| 11 | 1011 | B |
| 12 | 1100 | C |
| 13 | 1101 | D |
| 14 | 1110 | E |
| 15 | 1111 | F |
| 16 | 0001 0000 | 10 |
| 255 | 1111 1111 | FF |

Each hex digit = exactly 4 bits:
```
Binary:  1111  1010
Hex:       F     A
Result:        FA  (= 250 decimal)
```

 📌 Important Terms
| Term | Meaning |
|||
| Base 2 | Binary number system |
| Base 16 | Hexadecimal number system |
| 0x prefix | Indicates hexadecimal value (e.g. 0xFF = 255) |
| Hash | Fixedlength hex string output of a hash function |

 🔐 Cybersecurity Example
| Context | Example | Meaning |
||||
| IP Addresses | 192.168.1.1 | Each number 0–255 = 1 byte = 8 bits |
| MAC Addresses | 00:1A:2B:3C:4D:5E | 6 bytes written in hex |
| Password Hash | 5f4dcc3b5aa765d6... | MD5 — 32 hex chars = 128 bits |
| Memory Address | 0x7FFE0000 | RAM location in hex |
| Shellcode | EB 04 74 65 73 74 | Machine code bytes in hex |
| Web Colors | FF5733 | RGB values in hex |
| XOR Cipher | 0x41 XOR 0x20 = 0x61 | Basic encryption in hex |

Practice conversions:
| Decimal | Binary | Hex |
||||
| 10 | 0000 1010 | 0A |
| 64 | 0100 0000 | 40 |
| 200 | 1100 1000 | C8 |
| 255 | 1111 1111 | FF |

 ✅ Summary
Binary is the language computers actually use. Hexadecimal is shorthand for binary that humans can read. You will see both constantly — in IP addresses, MAC addresses, password hashes, memory addresses, and malware analysis. Master this early and everything in cybersecurity becomes easier.

 
  



 ✅ Day 1 Completion Checklist

   Read all 12 topics
   Filled Questions/Doubts for each topic
   Converted 10, 64, 200, 255 to binary and hex manually
   Copied notes into Notion
   Updated Progress Tracker (study hours)
   Updated Daily Log in Planner



 🔗 Resources Used
| Resource | Link |
|||
| Professor Messer CompTIA A+ | https://www.professormesser.com/freeaplustraining/2201101/2201101video/2201101trainingcourse/ |
| Khan Academy — Binary Numbers | https://www.khanacademy.org/computing/computersandinternet |
| Linux Journey | https://linuxjourney.com/ |
| TryHackMe | https://tryhackme.com/ |



Part of my public cybersecurity learning journey — haseebcybersecurityjourney(https://github.com/HaseebCybersec/haseebcybersecurityjourney)
