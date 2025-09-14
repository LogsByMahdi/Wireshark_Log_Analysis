# Installing the Virtual Machines

## Objectives
- **Part 1:** Prepare a Personal Computer for Virtualization  
- **Part 2:** Import a Virtual Machine into VirtualBox Inventory  

---

## Background / Scenario
Modern computers are powerful enough to run multiple virtual machines (VMs) on a single physical host.  
Virtualization allows security professionals to simulate real-world environments for testing, training, and analysis without risking the host system.  

In this lab, I set up the **CyberOps Workstation VM** and **Security Onion VM** using Oracle VirtualBox. These VMs form the foundation for all subsequent labs, allowing me to capture, analyze, and investigate network traffic safely.

---

## Required Resources
- Host computer with at least **8 GB RAM** and **40 GB free disk space**  
- **High-speed internet connection**  
- **Oracle VirtualBox** (latest version)  
- **CyberOps Workstation VM** (`cyberops_workstation.ova`)  
- **Security Onion VM** (`security_onion.ova`)  

---

## Part 1: Prepare a Host Computer for Virtualization

### Step 1: Install VirtualBox
1. Download VirtualBox from:  
   [https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html](https://www.oracle.com/virtualization/technologies/vm/downloads/index.html)  
2. Select the correct installation file for your host operating system (Windows, macOS, or Linux).  
3. Run the installer and accept the default installation settings.  

**Screenshot to include:** VirtualBox installed successfully on your system.

---

### Step 2: Download the Virtual Machine Images
1. Log in to [Cisco NetAcad](https://www.netacad.com).  
2. Navigate to the **CyberOps Associates Virtual Machines (VMs)** page.  
3. Download the following OVA files and save them locally:  
   - `cyberops_workstation.ova`  
   - `security_onion.ova`  

**Screenshot to include:** The downloaded OVA files visible in your folder.

---

## Part 2: Import the Virtual Machine into VirtualBox Inventory

### Step 1: Import the VM
1. Open **VirtualBox**.  
2. Go to **File > Import Appliance…**  
3. Select the downloaded `.ova` file (for example, `cyberops_workstation.ova`).  
4. Review the default VM settings, then click **Import**.  

**Screenshot to include:**  
- Import Appliance window with the `.ova` file selected  
- VM successfully added in the VirtualBox Manager  

---

### Step 2: Start and Log into the VM
1. Select the imported **CyberOps Workstation VM** in VirtualBox.  
2. Click **Start** (green arrow).  
3. If prompted, configure the network adapter as either:  
   - **Bridged Adapter** (preferred)  
   - **NAT** (if DHCP is not available)  
4. Once the VM boots, log in with the credentials:  
   - Username: `analyst`  
   - Password: `cyberops`  

**Screenshot to include:**  
- VM login screen  
- Successful login into the CyberOps Workstation desktop  

---

### Step 3: Verify Network Connectivity
1. Open the **Terminal Emulator** in the VM.  
2. Run the following command to view IP address information:  
   ```bash
   ip address
3. Launch the FireFox browser from within the VM.
4. Navigate to any website to confirm internet connection (in my case i used https://www.google.com)

---

### Step 4: Shut down the VM
When finished, shut down the VM properly.
   - Option A (GUI): From the VirtualBox window, click **Close** and then **Power Off**.
   - Option B : Open terminal inside the VM
     ```bash
     sudo shutdown -h now



