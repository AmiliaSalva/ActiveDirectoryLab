# Active Directory Lab Using VirtualBox

![10](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/dcbbd122-9cf7-42af-9513-841eb780f96f)


## Overview

To simulate a real-world Active Directory environment, I attempted this lab to walk through the essentials of setting up and configuring a Windows-based network. The objective is two-fold: first, to provide a granular understanding of how Active Directory functions, and second, to explore the broader aspects of Windows networking. By leveraging Oracle's VirtualBox, I've orchestrated a simulated environment comprising two virtual machines. One machine runs Windows Server 2019, acting as the Domain Controller, and the other runs Windows 10 to emulate a client experience.

## Objectives

![11](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/77004a99-0187-4cf5-8bf4-0ecfc373c4ec)

During this lab, we will:

- Set up Active Directory Domain Services from scratch.
- Create a dedicated Domain Admin account, ensuring security and control.
- Deploy a DHCP server to allocate IP addresses dynamically.
- Show the creation of an Organizational Unit for better user management.
- Delve into the intricacies of Routing and Remote Access to emulate a corporate intranet.
- Configure the Network Interface Card (NIC), ensuring local and internet connectivity.
- Demonstrate mass user management by leveraging PowerShell to batch-add over 1000 users.
- Interact with our client machine, simulating a login process using one of our newly added users.

## Technologies Used:

- Oracle VirtualBox
- ISO Files for Windows Server 2019 and Windows 10
- Powershell

## Installation

### Create Virtual Machines in VirtualBox

- Open Oracle VirtualBox and click "New."
- Name the first machine as "DC" and select Microsoft Windows as the type and Windows (64-bit) as the version.
- Assign at least 2 GB of RAM and create a new virtual hard disk of at least 50 GB.
- Repeat the process for our Windows 10 machine and name it "CLIENT."

### Installing the Operating Systems and Initial Setup

I initiated the installations by attaching the ISO files to their respective VMs. Windows Server 2019 required additional attention during setup to ensure proper administrative access. Here are the specifics:

- **Install Windows Server 2019:** Follow the on-screen instructions until you reach the account setup stage.
  
  ![IMG_1735](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/9ddc81f9-b45e-4b8c-ba31-9aa044cf92ba)
  
- **Create an Admin Account:** As part of the installation, you'll be prompted to create an administrator account. Here, I provided a username and a robust and unique password for enhanced security. This account will have elevated permissions, so it's crucial to protect it adequately.

  ![IMG_1737](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/67547c2b-797c-4ca2-b4d1-b1a71897ad13)

  ![IMG_1739](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/4d16f5ae-3b6c-4ca8-be5a-ff8476ba66b4)

### Laying Down the Operating Systems and Configuring NICs

I initiated the installation process after attaching the ISO files to their respective VMs. The on-screen instructions are generally straightforward, leading to a successful installation of both operating systems.

In addition, for our Domain Controller, it's imperative to configure dual Network Interface Cards (NICs) for effective network management. Here's how I set them up

- **NIC for Open Internet:** The first NIC is configured to use Network Address Translation (NAT), enabling our Domain Controller to connect to the open Internet.
  
- **NIC for Internal Network:** The second NIC is allocated exclusively to our internal virtual network, ensuring isolated communication within our simulated environment.

This dual NIC setup equips the Domain Controller with the network versatility needed for real-world applications, aligning perfectly with our lab's objectives. 

Doing so has established a secure yet flexible network topology indispensable for our Active Directory Lab.




## Integrating Active Directory Domain Services

- Upon booting up Windows Server, I ventured into the Server Manager, and from there, I meticulously added the "Active Directory Domain Services" role.

![ACTIVEDIRECTORY LAB2](https://github.com/AmiliaSalva/ActiveDirectoryLab/assets/132176058/5877e1da-97c1-4d92-86ce-1c09d133d956)


## Crafting a Domain Admin Account

- Open Active Directory Users and Computers.
- Right-click and select New > User.
- Provide details for your new Domain Admin account and set a strong password.

## Set Up DHCP Server

- Back in the Server Manager, I incorporated the "DHCP Server" role, ensuring our client machine would receive an IP address dynamically.

## Structuring the Organizational Unit

- Open Active Directory Users and Computers.
- Right-click on your domain, go to New > Organizational Unit, and create an OU.

## Configure Routing and Remote Access

- Go to Server Manager and add the "Routing" role.
- Configure Routing and Remote Access to set up an internal network.

## Configure NIC for Internet Access

- Open Network and Sharing Center and go to "Change adapter settings."
- Configure the NIC to connect to the outside internet.

## Add Users via PowerShell

  
