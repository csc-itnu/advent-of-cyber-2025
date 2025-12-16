**Room Link:**  
https://tryhackme.com/room/webattackforensics-aoc2025-b4t7c1d5f8

## ▶️ CYBERWOX – Day 15 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/Gf68YnVjy7k?si=x1xKWxwN-3sB_tAz

---

# 🎄 Advent of Cyber 2025 — Day 15 Write-Up  
## 🧩 Web Attack Forensics — Drone Alone

---

## 🔐 Logging into Splunk

<img width="617" height="195" alt="splunk login" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/1final.png?raw=true" />

---

## 🚨 Detect Suspicious Web Commands

**Query:**
```
index=windows_apache_access (cmd.exe OR powershell OR "powershell.exe" OR "Invoke-Expression")
| table _time host clientip uri_path uri_query status
```

<img width="1460" height="313" alt="apache access logs" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/2access.png?raw=true" />

---

## ⚠️ Check Apache Error Logs for Command Execution

**Query:**
```
index=windows_apache_error ("cmd.exe" OR "powershell" OR "Internal Server Error")
```

<img width="1462" height="454" alt="apache error logs" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/3errors.png?raw=true" />

---

## 🧬 Trace Suspicious Process Creation via Sysmon

**Query:**
```
index=windows_sysmon ParentImage="*httpd.exe"
```

<img width="1464" height="592" alt="sysmon apache spawn" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/4sysmon.png?raw=true" />

Normally, Apache should only spawn worker threads — **not** system binaries.

Example of malicious behavior:
<pre>
ParentImage = C:\Apache24\bin\httpd.exe
Image       = C:\Windows\System32\cmd.exe
</pre>

This confirms **successful command injection**.

---

## 🔍 Confirm Attacker Enumeration Activity

**Query:**
```
index=windows_sysmon *cmd.exe* *whoami*
```

<img width="1461" height="644" alt="sysmon whoami" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/5sysmonconfirm.png?raw=true" />

---

## 🧠 Identify Base64-Encoded PowerShell Payloads

**Query:**
```
index=windows_sysmon Image="*powershell.exe"
(CommandLine="*enc*" OR CommandLine="*-EncodedCommand*" OR CommandLine="*Base64*")
```

<img width="1457" height="281" alt="base64 powershell" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/6base.png?raw=true" />

This detects obfuscated PowerShell payloads using Base64 encoding.  
If defenses are working properly, **no results should appear**, meaning the payload (e.g., “Muahahaha”) never executed.

---

# ✅ Challenge Answers

---

### **1️⃣ What is the reconnaissance executable file name?**

<img width="1919" height="768" alt="recon exe" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/7ans1.png?raw=true" />

```
whoami.exe
```

---

### **2️⃣ What executable did the attacker attempt to run via command injection?**

<img width="1920" height="410" alt="powershell execution" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day15/8ans2.png?raw=true" />

```
powershell.exe
```

---
