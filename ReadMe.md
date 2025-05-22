# 💻 Exercise 1 - Create a VM Using Hyper-V

## 🧠 Overview

In this lab, we used **Hyper-V** (a Type 1 hypervisor) on **ACIWIN11** to create and install an Ubuntu 22.04.3 virtual machine. Although it appears as an app in Windows, Hyper-V runs directly on the system hardware, making it a "bare metal" hypervisor.

Click here for the videos https://drive.google.com/drive/folders/1vrC4GxIE4cjkrucxKB6M98ZYFyNYOiC9?usp=sharing
---

## 🎯 Objectives

- Create a VM in Hyper-V  
- Start Ubuntu installation

---

## 🖥️ Lab Devices

| Device   | OS Version        | Role                    |
|----------|-------------------|-------------------------|
| ACIDC01  | Windows Server 2022 | Domain Controller     |
| ACIWIN11 | Windows 11 Pro      | Hyper-V Host Workstation |

---

## ⚙️ Task 1: Create the VM

1. Log in to **ACIWIN11**  
   - **User:** `ACIPLAB\Administrator`  
   - **Pass:** `Passw0rd`

2. Open **Hyper-V Manager** > Actions > **New > Virtual Machine**

3. Complete the wizard:
   - **Name:** `Ubuntu 22.04.3`
   - **Generation:** `Generation 2`  
     > Modern OS support with UEFI and better performance.
   - **Memory:** `2048 MB`
   - **Network:** `Default Switch`  
     > Allows VM to reach other VMs, host, and internet.
   - **Hard Disk:** `25 GB`
   - **Install from ISO:**  
     Browse to `Documents > Module_7_Folder` and select `ubuntu-22.04.3-desktop-amd64.iso`

4. In **VM Settings > Security**  
   - Uncheck **Enable Secure Boot**  
     > Ubuntu may fail to boot with Secure Boot enabled in Hyper-V.

---

## 🚀 Task 2: Install Ubuntu

1. In **Hyper-V Manager**, right-click the VM > **Connect** > **Start**

2. Ubuntu boot menu: Press **Enter**

3. Click **Install Ubuntu**

4. **Keyboard layout:** Leave default > Continue  
   > Default layout works for most users.

5. **Updates and Software:**
   - Leave **Normal installation**
   - Uncheck **Download updates** > Continue  
   > Speeds up install and avoids update errors.

6. **Installation type:** Click **Install Now** > Continue  
   > Auto-partitions the virtual disk.

7. **Location:** Leave default > Continue  
   > Time syncs with host.

8. **User setup:**
   - Name: `ACIAdmin`
   - Password: `Passw0rd`
   - Select **Log in automatically** > Continue  
   > Simplifies login during labs.

---

## ✅ Challenge Questions

**Q1:** Why is Hyper-V a Type 1 hypervisor?  
**A:** It runs directly on hardware before the OS loads.

**Q2:** Why disable Secure Boot?  
**A:** It can block Linux from booting in Hyper-V.

---

