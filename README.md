# 🔒 SIEM Internship - Phase 2: Suspicious Activity Detection & Threat Simulation

This repository contains the simulated attack scenarios, log collection, and detection evidence for **Phase 2** of the SIEM Internship Program. All tasks were executed with a focus on **log generation** and validation for **common suspicious activities** and **attacker behaviors**.

---

## 🔧 Lab Environment

- **Windows 10 Home VM** - Victim/Target system  
- **Kali Linux VM** - Attacker system and log collector  
- **Network** - NAT setup with working communication between VMs  
- **Log Collection** - Syslog-ng, Event Viewer, Sysmon used for capturing logs  

---

## ✅ Completed Scenarios

### 1. Privilege Escalation  
Simulated privilege escalation by creating a new user and promoting them to the Administrators group. Verified with Event ID 4728.

📸 `01_priv_esc_user_created`  
📸 `02_priv_esc_user_promoted`  
📸 `03_priv_esc_event_4728_details`

---

### 2. Lateral Movement (PsExec)  
Used PsExec from Sysinternals to simulate a remote command execution, representing lateral movement techniques.

📸 `04_lateral_psexec_downloaded`  
📸 `05_lateral_psexec_command_executed`

---

### 3. Suspicious File Download  
Downloaded a `.zip` file from the internet to simulate suspicious file delivery or malware infection vectors.

📸 `06_suspicious_zip_download`

---

### 4. Malicious PowerShell Execution  
Executed obfuscated PowerShell commands to mimic attacker behavior. Captured logs include Event ID 4104 and Sysmon alerts.

📸 `07_suspicious_powershell_exec`  
📸 `08_suspicious_powershell_exec_4104`  
📸 `09_suspicious_pskill_4688`  
📸 `10_powershell_encoded_execution`

---

### 5. Malicious Archive Execution  
Packed a `.exe` into a `.zip`, extracted and ran it to mimic a hidden malicious payload launch.

📸 `11_malicious_archive_execution_sysmon_1`

---

### 6. C2/Beaconing Simulation  
Simulated outbound beaconing behavior by scheduling periodic pings from Windows to the Kali machine.

📸 `12_Phase2_C2_Beaconing_TaskScheduler`  
📸 `13_Phase2_C2_Beaconing_Logs`

---

### 7. Web Activity & Vulnerability Scan Simulation  
Browsed to a suspicious site and ran vulnerability scans using tools like Nmap and OWASP ZAP to simulate attacker recon.

📸 `14_Internship_Web_Test_Kali_Browser`  
📸 `15_nmap_scan_results`

---

### 8. Unauthorized RDP Login Simulation  
Enabled RDP using RDPWrap and simulated a remote login session on Windows 10 Home to test unauthorized access attempts.

📸 `16_RDPWrap_Remote_Access`

---

### 9. Web Shell / Leak Simulation  
Simulated a basic reverse shell or exfiltration-style activity from Kali to mimic attacker persistence or data leak.

📸 `17_Web_Leak_Simulation_Screenshot`

---

## 📂 Screenshot Order (Final Submission Structure)

screenshot_order:
  - 01_priv_esc_user_created
  - 02_priv_esc_user_promoted
  - 03_priv_esc_event_4728_details
  - 04_lateral_psexec_downloaded
  - 05_lateral_psexec_command_executed
  - 06_suspicious_zip_download
  - 07_suspicious_powershell_exec
  - 08_suspicious_powershell_exec_4104
  - 09_suspicious_pskill_4688
  - 10_powershell_encoded_execution
  - 11_malicious_archive_execution_sysmon_1
  - 12_Phase2_C2_Beaconing_TaskScheduler
  - 13_Phase2_C2_Beaconing_Logs
  - 14_Internship_Web_Test_Kali_Browser
  - 15_nmap_scan_results
  - 16_RDPWrap_Remote_Access
  - 17_Web_Leak_Simulation_Screenshot

