# How to Install Kali Linux on an Apple Silicon Mac Using UTM

## Overview

This guide shows you how to install Kali Linux on an Apple Silicon Mac by using UTM. UTM is a QEMU-based hypervisor and emulator that uses hardware acceleration for better performance.

## Before you begin

Make sure you have the following:

- An Apple Silicon Mac with an M1 or M2 chip
- At least 50 GB of free disk space
- The UTM app
- The ARM64 version of the Kali Linux ISO image

## Installation steps

### Download software

- **UTM app**: Go to the [UTM official site](https://mac.getutm.app/) and download the app.

- **Kali Linux ISO**: Visit the [Kali Linux download page](https://www.kali.org/get-kali/) and download the ARM64 version.

### Configure the virtual machine

3. **Open UTM**: Start the UTM app and select **Create a New Virtual Machine**.

    ![Create a new VM](../assets/images/install-kali-on-apple-silicon/01-create-a-new-vm.png)

4. **Set up the virtual machine**: Choose **Virtualize**, and then select Linux as the operating system.

    ![Virtualize](../assets/images/install-kali-on-apple-silicon/02-virtualize.png)

5. **Import the Kali Linux ISO**: Add the ISO image you downloaded earlier.

    ![Add downloaded ISO](../assets/images/install-kali-on-apple-silicon/03-select-iso-file.png)

### Install Kali Linux

6. **Configure hardware settings**: Set the memory to 4 GB, the number of CPU cores to 4, and enable OpenGL acceleration.

7. **Allocate disk space**: Provide at least 30 GB of disk space for the virtual machine.

8. **Name the virtual machine**: Enter a name for your virtual machine.

9. **Save your settings**: Choose **Save** to create the virtual machine.

10. **Add a serial device**: Go to the settings for your virtual machine and add a serial device. You'll need this for the installation process.

11. **Start the installation**: Turn on the virtual machine and follow the on-screen prompts to:
    - Choose a system language
    - Set up your timezone and keyboard
    - Create a user account
    - Partition the virtual disk
    - Choose a desktop environment

## After the installation

1. Turn off the virtual machine.
2. Remove the serial device from your virtual machine settings.
3. Eject the Kali Linux ISO image.
4. Turn on the virtual machine.
5. Once you're logged in, open a terminal and run the following command to update the list of available packages and their versions:

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

## Troubleshooting and fixes

### Resolve update command failures

You might run into update command failures after installing Kali Linux. Often, the issue arises from outdated or incorrect repository links in your sources list. To fix this:

1. Open the terminal.
2. Run the following command to update your sources list:

   ```bash
   echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" > /etc/apt/sources.list
   ```

This command replaces your existing sources list with a verified repository.

### Choose a clean installation when necessary

If you experience system inconsistencies that are hard to pinpoint, a clean installation might be your best course of action. This can resolve issues ranging from software conflicts to corrupted files.

To perform a clean installation:

1. Back up any important data.
2. Open the UTM control panel.
3. Delete the existing virtual machine.
4. Follow the initial setup instructions to create a new virtual machine.

### Enhance your virtual machine with Guest Additions

After setting up Kali Linux and resolving any initial issues, consider enhancing your system with Guest Additions. This add-on improves performance and adds new features.

To install Guest Additions:

1. Open the terminal in your Kali Linux virtual machine.
2. Run the following command:

   ```bash
   apt install qb-additions
   ```

This installs the Guest Additions package, enabling functionalities like seamless mouse integration, improved display resolutions, and more efficient file sharing between the host and the virtual machine.

## Further resources and learning paths

### Exploring advanced tools in Kali Linux

After setting up Kali Linux on your Apple Silicon Mac, explore a variety of cybersecurity tools available for tasks like network analysis, penetration testing, and digital forensics. Here are some tools worth checking out:

- **[Wireshark](https://www.wireshark.org/)**: Analyze network protocols.
- **[Metasploit](https://www.metasploit.com/)**: Develop, test, and execute exploit code.
- **[Nmap](https://nmap.org/)**: Scan networks and inventory devices.
- **[Hashcat](https://hashcat.net/hashcat/)** and **[John the Ripper](https://www.openwall.com/john/)**: Crack passwords.
- **[Kismet](https://www.kismetwireless.net/)**: Scan wireless networks.
- **[Zed Attack Proxy (ZAP)](https://www.zaproxy.org/)**: Scan web apps.
- **[Aircrack-ng](https://www.aircrack-ng.org/)**: Assess WiFi network security.
- **[Burp Suite](https://portswigger.net/burp)**: Test web application security.
- **[Hydra](https://github.com/vanhauser-thc/thc-hydra)**: Perform password cracking and brute force attacks.
- **[SQLmap](http://sqlmap.org/)**: Automate the detection and exploitation of SQL injection flaws.
- **[Snort](https://www.snort.org/)**: Act as a network intrusion prevention system.
- **[Nessus](https://www.tenable.com/products/nessus)**: Conduct vulnerability scanning.
  
These tools can enhance your Kali Linux experience, helping you tackle various cybersecurity challenges.
