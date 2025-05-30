SIEM Internship - Phase 2: Suspicious Activity Detection & Threat Simulation
This repository contains the simulated attack scenarios, log collection, and detection evidence for Phase 2 of the SIEM Internship Program. All tasks were executed with a focus on log generation and validation for common suspicious activities and attacker behaviors.

🔧 Lab Environment
Windows 10 Home VM - Victim/Target system(10.0.2.4)

Kali Linux VM - Attacker system and log collector(10.0.2.15)

Network - NAT setup with working communication between VMs

Log Collection - Syslog-ng, Event Viewer, Sysmon used for capturing logs

✅ Completed Scenarios & Proofs
1. Privilege Escalation
Note: A new user account was created and manually added to the local Administrators group. This simulates privilege escalation and triggers Event ID 4728, showing group membership changes.

Screenshots:

01_priv_esc_user_created

02_priv_esc_user_promoted

03_priv_esc_event_4728_details

2. Lateral Movement (PsExec)
Note: Used Sysinternals PsExec tool to execute a command remotely, mimicking attacker lateral movement behavior over the network.

Screenshots:

04_lateral_psexec_downloaded

05_lateral_psexec_command_executed

3. Suspicious File Download
Note: A suspicious ZIP archive was downloaded from a test web server, simulating file delivery by phishing or external threat actors.

Screenshot:

06_suspicious_zip_download

4. Malicious PowerShell Execution
Note: Executed obfuscated PowerShell commands and scripts using encoded strings and suspicious flags. Logs were captured via Sysmon (Event ID 1) and Windows Event ID 4104 for script block logging.

Screenshots:

07_suspicious_powershell_exec

08_suspicious_powershell_exec_4104

09_suspicious_pskill_4688

10_powershell_encoded_execution

5. Malicious Archive Execution
Note: A password-protected archive containing a .exe file was extracted and executed to simulate delivery and execution of malware from archive formats.

Screenshot:

11_malicious_archive_execution_sysmon_1

6. C2/Beaconing Simulation
Note: A scheduled task was created on the Windows machine to ping the attacker's Kali IP every 5 minutes, simulating Command & Control beaconing behavior in malware.

Screenshots:

12_Phase2_C2_Beaconing_TaskScheduler

13_Phase2_C2_Beaconing_Logs

7. Web Activity & Vulnerability Scan Simulation
Note: Simulated browsing activity to unknown/malicious-looking websites and scanned the Windows machine using Nmap to trigger logs related to vulnerability probing.

Screenshots:

14_Internship_Web_Test_Kali_Browser

15_nmap_scan_results

8. Unauthorized RDP Login Simulation
Note: Enabled RDP on Windows 10 Home using RDPWrap, then performed a login attempt over RDP to simulate unauthorized remote access. Events like 4624 (Type 10) were observed.

Screenshot:

16_RDPWrap_Remote_Access

9. Web Shell / Leak Simulation
Note: Simulated data exfiltration or reverse shell execution from the target system to the attacker using simple web-based or Netcat tools to show outbound connection behavior.

Screenshot:

17_Web_Leak_Simulation_Screenshot

📂 Folder & Screenshot Structure (Final Order)
01_priv_esc_user_created
02_priv_esc_user_promoted
03_priv_esc_event_4728_details
04_lateral_psexec_downloaded
05_lateral_psexec_command_executed
06_suspicious_zip_download
07_suspicious_powershell_exec
08_suspicious_powershell_exec_4104
09_suspicious_pskill_4688
10_powershell_encoded_execution
11_malicious_archive_execution_sysmon_1
12_Phase2_C2_Beaconing_TaskScheduler
13_Phase2_C2_Beaconing_Logs
14_Internship_Web_Test_Kali_Browser
15_nmap_scan_results
16_RDPWrap_Remote_Access
17_Web_Leak_Simulation_Screenshot

