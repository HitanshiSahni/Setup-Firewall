# Setup and Use a Firewall (UFW on Ubuntu via WSL)

## 🎯 Objective
Configure and test basic firewall rules to allow or block network traffic using **UFW (Uncomplicated Firewall)** on a Linux system (Ubuntu via WSL on Windows).

---

## 🛠 Tools Used
- **UFW** (Uncomplicated Firewall)
- **Ubuntu on WSL (Windows Subsystem for Linux)**
- **Telnet** (for connection testing)
- **Terminal / Bash**

---

## 🔧 Steps Performed

1. **Enabled UFW**
   ```bash
   sudo ufw enable

2. **Check Current Firewall Rules**
   ```bash
   sudo ufw status numbered

3. **Block Inbound Traffic on Port 23 (Telnet)**
   ```bash
   sudo ufw deny 23

4. **Install Telnet (if not installed)**
   ```bash
   sudo apt install telnet

5. **Test the Blocking Rule Using Telnet**
   ```bash
   telnet localhost 23
Expected: Connection refused

6. **Allow SSH on Port 22**
   ```bash
   sudo ufw allow 22

7. **Remove the Telnet Blocking Rule (Unblock Port 23)**
   ```bash
   sudo ufw delete deny 23
