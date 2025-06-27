# task---4-elevate-labs
# 🔐 Task 4 – Setup and Use a Firewall on Windows

## 📝 Objective
The objective of this task is to configure and test basic firewall rules using **Windows Defender Firewall** to block and allow specific network traffic (ports). This helps understand the fundamentals of traffic filtering and basic firewall management.

---

## 🛠 Tools Used
- Windows 10/11
- Windows Defender Firewall with Advanced Security
- Command Prompt
- Telnet Client

---

## 🔧 Steps Performed

### ✅ Step 1: Open Windows Firewall
- Opened **Control Panel**
- Navigated to: Control Panel → System and Security → Windows Defender Firewall

- Clicked on **Advanced settings** to open the rule editor

---

### ✅ Step 2: Enable Telnet Client
Since Telnet is not enabled by default:
1. Opened: `Control Panel → Programs → Turn Windows features on or off`
2. Checked ✅ **Telnet Client**
3. Clicked OK and waited for the installation to complete

---

### ✅ Step 3: Create Inbound Rule to Block Port 23 (Telnet)
1. Clicked **Inbound Rules** → **New Rule**
2. Selected **Port** → Clicked Next
3. Chose **TCP**, specified port: `23`
4. Selected **Block the connection**
5. Applied to: Domain, Private, Public profiles
6. Named it: **Block Telnet Port 23**

---

### ✅ Step 4: Test the Firewall Rule in Command Prompt
Opened Command Prompt and ran:

```bash
telnet localhost 23
Connecting To localhost...Could not open connection to the host, on port 23: Connect failed

