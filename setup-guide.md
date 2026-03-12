# CYBERKIT Setup Guide

This guide explains how to recreate the CYBERKIT portable cybersecurity and IT recovery toolkit.

The toolkit integrates multiple operating environments onto a single bootable USB drive for system recovery, diagnostics, and security testing.

---

## 1. Hardware Requirements

* USB Flash Drive (64GB recommended minimum)
* Computer capable of USB boot
* Internet connection to download ISO files
* Virtual machine software for testing (optional but recommended)

---

## 2. Required Software

The following operating environments are included in CYBERKIT:

| Environment     | Purpose                                     |
| --------------- | ------------------------------------------- |
| WinPE           | Windows system recovery and troubleshooting |
| Kali Linux Live | Cybersecurity testing and network analysis  |
| Ubuntu Live     | Linux troubleshooting and data recovery     |
| MemTest86       | Memory hardware diagnostics                 |

You will also need a **multi-boot USB creation tool** such as:

* Ventoy
* YUMI
* Easy2Boot

*(CYBERKIT was designed to work with most multi-boot solutions.)*

---

## 3. Preparing the USB Drive

1. Insert the USB drive into your computer.
2. Back up any existing files on the drive.
3. Format the drive using the recommended format for your boot tool.
4. Install the multi-boot bootloader (example: Ventoy).

Example using Ventoy:

1. Download Ventoy.
2. Run the Ventoy installation tool.
3. Select the USB drive.
4. Install the Ventoy bootloader to the device.

---

## 4. Download Required ISO Files

Download the latest ISO images for the following:

* Kali Linux Live
* Ubuntu Live
* Windows PE environment
* MemTest86

Verify file integrity using SHA256 hashes when available.

---

## 5. Adding Operating Systems to the USB

1. Copy the ISO files directly onto the USB drive.
2. Place them in organized folders if desired:

```
/ISO
/ISO/Linux
/ISO/Diagnostics
```

Example layout:

```
/ISO
   kali-linux-live.iso
   ubuntu-live.iso
   memtest86.iso
   winpe.iso
```

Most multi-boot tools automatically detect ISO files and add them to the boot menu.

---

## 6. Testing the Toolkit

Before using CYBERKIT on physical machines, test the USB in a virtual machine.

Suggested platforms:

* VirtualBox
* VMware Workstation

Testing checklist:

* Verify USB boots successfully
* Confirm boot menu appears
* Test launching each environment
* Ensure tools load correctly

---

## 7. Deployment

Once testing is complete:

1. Safely eject the USB drive.
2. Insert the drive into a target system.
3. Enter the BIOS or boot menu.
4. Select the USB devic
