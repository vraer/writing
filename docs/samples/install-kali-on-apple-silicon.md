# Installing Kali Linux on Apple Silicon Macs Using UTM  

## Overview

Learn how to install Kali Linux on an Apple Silicon Mac using UTM. UTM is a hypervisor and emulator based on QEMU that leverages hardware acceleration for enhanced performance.

## Prerequisites

Ensure you have the following before proceeding:

- **Hardware**: Apple Silicon Mac (M1/M2 chip)
- **Disk Space**: At least 50GB of free space
- **Software**: UTM app, Kali Linux ISO (ARM64 version)

## Installation Steps

### 1. Get the UTM App

Download and install the UTM app from [here](https://mac.getutm.app/).

### 2. Download Kali Linux ISO

Grab the ARM64 version of Kali Linux from [Kali's official site](https://www.kali.org/get-kali/).

### 3. Create a New VM in UTM

- Open the UTM app.
- Click the **New** button.

### 4. Configure VM Settings

- Choose **Virtualize**.
- Select Linux as the OS.

### 5. Import Kali Linux ISO

Locate and import the Kali Linux ISO you downloaded.

### 6. Hardware Configuration

Configure the following hardware settings:

- **Memory**: 4GB
- **CPU Cores**: 4
- **Graphics**: Enable OpenGL acceleration

### 7. Allocate Disk Space

Allocate a minimum of 30GB for virtual disk storage.

### 8. Name the VM

Give your virtual machine a name.

### 9. Save VM Configuration

Click **Save** to finalize the VM creation.

### 10. Serial Device Setup

In the VM settings, add a serial device. This is needed for the installation process.

### 11. Boot VM

Start the virtual machine.

### 12. Kali Linux Installation

Follow the on-screen instructions:

- Language selection
- Timezone and keyboard setup
- User account creation
- Virtual disk partitioning
- Desktop environment choice

## Post-Installation

- Power off the VM.
- Remove the serial device from VM settings.
- Eject the Kali Linux ISO.
- Boot the VM.
- Update your package list.

## Verification

Make sure the following work:

- Kali Linux boots in the VM.
- Clipboard sharing between macOS and Kali Linux.

## Troubleshooting

- **Update Errors**: Run `echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" > /etc/apt/sources.list`.
- **Avoid Distribution Upgrades**: Perform a clean install instead.
- **VM Guest Additions**: Run `apt install qb-additions` to add guest features.
