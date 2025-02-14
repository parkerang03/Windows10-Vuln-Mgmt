# Vulnerability Management Lab with Tenable: A Practical Guide

Welcome to the **Vulnerability Management Lab with Tenable**! This repository contains the resources and steps from a hands-on lab that demonstrates the fundamentals of vulnerability management using Tenable’s vulnerability scanning tools. This lab is designed for cybersecurity enthusiasts and professionals looking to deepen their understanding of vulnerability management and how to use it effectively to secure systems.

---

### Lab Architecture and Overview
This lab is designed to be cloud-based and accessible from any computer. The lab provides actionable skills for your cybersecurity journey, with practical steps to enhance your resume and boost your job prospects. The Tenable Vulnerability Management cloud console was used as the main operating interface and the Tenable Scan Engine as well as the Scan Target were both hosted on Microsoft Azure virtual machines.

<img width="931" alt="image" src="https://github.com/user-attachments/assets/2853aed3-0092-4b4c-be3e-a67cd8dfd9f5" />

---

### Key Concepts Covered
- **Introduction to Vulnerability Management**:
  - What is software vulnerability management?
  - Understanding vulnerabilities, scan engines, and remediation.
  - Overview of compliance standards like DISA/STIG, CIS, etc.

- **Hands-On Steps**:
  - Setting up a virtual machine (VM) for scanning.
  - Configuring a Tenable vulnerability scanner.
  - Performing compliance checks (e.g., DISA/STIG).
  - Identifying vulnerabilities and compliance issues.
  - Creating and remediating vulnerabilities.
  - Observing results and documenting remediation efforts.

- **Tools Used**:
  - Azure (for VM setup with free credits).
  - Tenable Vulnerability Management (free trial available).
  - LogN Pacific Cyber Range (optional, preconfigured environment).

---

### Lab Workflow

**Environment Setup**:
   - Configure a VM in Azure.
   - Prepare the VM for vulnerability scanning.
    ![image](https://github.com/user-attachments/assets/0147f5a6-66bb-48e3-9106-2b509a75b259)

**Scan Configuration**
   - Configure a credentialed Tenable scan to look for all the basic vulnerabilities + *DISA Windows 10 STIG v3r2*
     ![image](https://github.com/user-attachments/assets/95b1b2c5-28e1-44ed-9460-faa6f0073893)



**Initial Scan**:
   - Perform an initial vulnerability and compliance baseline scan.
   - Review and analyze scan results including failed STIGs. For this lab, we will focus on the following STIGs to Fail/Remediate:
     - STIG ID WN10-AU-000505 (Increase size of Security Event Log) - Initial Fail
     - STIG ID WN10-SO-000025 (Rename Guest Account) - Initial Fail
     - STIG ID WN10-SO-000010 (Disable Guest Account) - Initial Pass

![image](https://github.com/user-attachments/assets/f5f58ec0-6fe8-418a-a556-1b67ebd88d29)
![image](https://github.com/user-attachments/assets/b8f62d4e-2487-4e59-9b68-1ea9cb42f6ab)
![image](https://github.com/user-attachments/assets/e2be66c4-7d71-4a52-9a12-5e8505a25127)



**Simulate Vulnerabilities**:
   - Introduce vulnerabilities such as outdated software (Firefox v110) or misconfigured settings (Enabled Guest Account)
     - Intentionally FAIL: STIG ID WN10-SO-000010 by enabling the Guest Account
   - Perform a second scan to detect changes.
     ![image](https://github.com/user-attachments/assets/46f0d7c2-fb90-4014-86e1-8f8528a167f5)

**Remediation**:
   - Fix vulnerabilities and compliance issues (e.g., uninstall outdated software, modify registry settings to increase security event log size, disable Guest account, rename Guest account, fully update Windows).
   - Perform a final scan to confirm remediation.
     
**Document Results**:
   
   ![image](https://github.com/user-attachments/assets/f06f9911-be1c-48ff-903b-155d6df353bb)

   
   - Scan 1: You can see the initial vulnerability baseline with the first scan
   - Scan 2: A spike occurred when we introduced a deprecated version of Firefox
   - Scan 3: A dip in vulnerabilities is observed after removing Firefox
   - Scan 4: A final dip takes place after fully updating Windows

---

### Conclusions
This lab not only provides hands-on experience with vulnerability management but also equips you with practical cybersecurity skills. By completing the lab, you'll gain practice with:
- Real-world vulnerability identification and remediation.
- Compliance frameworks such as DISA/STIG.
- Effective use of Tenable’s tools.

---
