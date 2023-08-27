# Active Directory Lab Using VirtualBox

![10](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/dcbbd122-9cf7-42af-9513-841eb780f96f)


## Overview

In my endeavors to simulate a real-world Active Directory environment, I attempted this lab to walk through the essentials of setting up and configuring a Windows-based network. The objective is two-fold: first, to provide a granular understanding of how Active Directory functions, and second, to explore the broader aspects of Windows networking. By leveraging Oracle's VirtualBox, I've orchestrated a simulated environment comprising two virtual machines. One machine runs Windows Server 2019, acting as the Domain Controller, and the other runs Windows 10 to emulate a client experience.

## Objectives

![11](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/77004a99-0187-4cf5-8bf4-0ecfc373c4ec)

During this lab we will:

- Set up Active Directory Domain Services from scratch.
- Create a dedicated Domain Admin account, ensuring security and control.
- Deploy a DHCP server to dynamically allocate IP addresses.
- Show the creation of an Organizational Unit for better user management.
- Delve into the intricacies of Routing and Remote Access to emulate a corporate intranet.
- Configure the Network Interface Card (NIC) ensuring both local and internet connectivity.
- Demonstrate mass user management by leveraging PowerShell to batch-add over 1000 users.
- Interact with our client machine, simulating a login process using one of our newly added users.

## Technologies Used:

- Oracle VirtualBox
- ISO Files for Windows Server 2019 and Windows 10

## Installation

### Step 1: Create Virtual Machines in VirtualBox

- Open Oracle VirtualBox and click "New".
- Name the first machine as "DC" and select Microsoft Windows as the type and Windows (64-bit) as the version.
- Assign at least 2 GB of RAM and create a new virtual hard disk of at least 50 GB.
- Repeat the process for our Windows 10 machine and name it "CLIENT".
  
### Step 2: Install Operating Systems

- 




  
