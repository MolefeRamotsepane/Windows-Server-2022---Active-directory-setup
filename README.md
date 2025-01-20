# Windows-Server-2022---Active-directory-setup

## **Project Overview**
This project is part of my learning journey in IT infrastructure, guided by a detailed lecture approach. The goal is to set up a **Windows Server 2022** environment, configure **Active Directory Domain Services (AD DS)**, and manage users and groups within a domain. This is the first step toward building practical IT skills.

---

## **What I Learned**
- How to install and configure Windows Server 2022 on VMware.
- Setting up a static IP and hostname for the server.
- Installing and configuring Active Directory.
- Creating and managing users and groups in a domain.
- Joining a client machine to a domain.

---

## **Setup Requirements**
### **Software and Tools**
1. VMware Workstation Player (or VirtualBox)
2. Windows Server 2022 ISO
3. Optional: Windows 10/11 ISO for a domain client

### **Hardware Requirements**
- Laptop or PC with at least 8GB RAM (16GB recommended)
- 40GB of free disk space for the virtual machine

---

## **Project Steps**

### **1. Setting Up VMware**
- Installed VMware Workstation Player and created a new virtual machine.
- Allocated resources: 4GB RAM, 2 CPUs, 40GB storage.
- Configured the network to **Bridged Mode** for local network access.

### **2. Installing Windows Server 2022**
- Installed Windows Server 2022 using the ISO.
- Set up the Administrator account with a secure password.

### **3. Initial Configuration**
- Changed the server's hostname to `ADServer`.
- Configured a static IP:
  - **IP Address**: `192.168.1.10`
  - **Subnet Mask**: `255.255.255.0`
  - **Default Gateway**: `192.168.1.1`
  - **Preferred DNS Server**: `127.0.0.1`

### **4. Installing Active Directory Domain Services**
- Added the **Active Directory Domain Services (AD DS)** role in Server Manager.
- Promoted the server to a Domain Controller with a new forest.
- Restarted the server after the configuration.

### **5. Managing Active Directory**
- Opened the Active Directory Users and Computers tool.
- Created:
  - A user: `John Doe` (username: `jdoe`).
  - A group: `HR Group`.
- Added `John Doe` to the `HR Group`.

### **6. Testing the Setup**
- Created a Windows 10 virtual machine as a client.
- Joined the client machine to the `example.local` domain.
- Logged in to the client using domain credentials (`example\jdoe`).

---

## **Skills Demonstrated**
- **Virtualization**: Setting up and managing VMs using VMware.
- **Server Administration**: Installing and configuring Windows Server.
- **Networking**: Configuring static IPs and domain connectivity.
- **Active Directory**: Managing users, groups, and domains.

---

## **Challenges I Faced**
1. **Network Configuration**: Initially, the VM couldn't access the network. I resolved this by setting the network mode to **Bridged** in VMware.
2. **Domain Join Issues**: The client VM couldn’t find the domain at first. Restarting both the server and client fixed the issue.

---

## **Future Improvements**
- Add more domain controllers to create redundancy.
- Experiment with Group Policies for advanced domain management.
- Test with multiple clients in the domain.

---
