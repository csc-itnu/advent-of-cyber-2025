**Room Link:**  
https://tryhackme.com/room/yara-aoc2025-q9w1e3y5u7

## ▶️ GingerHacker – Day 13 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/NAYtCSUHR8M?si=BcrBFSlC0giDQdIP

---

# 🎄 Advent of Cyber 2025 — Day 13 Write-Up  
## 🧩 YARA Rules — *YARA Mean One!*

---

# ✅ Challenge Answers

---

## 🛠️ Creating the YARA Rule

<img width="1171" height="782" alt="nano yara file" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day13/1nano.png?raw=true" />

The YARA rule file is saved as **TBFC**:

```
rule TBFC_Simple
{
    meta:
        description = "Testing"

    strings:
        $var = /TBFC:[A-Za-z0-9]+/

    condition:
        $var
}
```

<img width="860" height="334" alt="yara rules" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day13/2rules.png?raw=true" />

<img width="922" height="312" alt="yara findings" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day13/3findings.png?raw=true" />

---

## 🔍 YARA Command Explanation

- `yara` → runs the YARA scanner  
- `-r` → recursively scan subdirectories  
- `-s` → print matched strings and offsets  
- `TBFC` → YARA rule file  
- `/home/ubuntu` → directory being scanned  

This scans everything under `/home/ubuntu` using the **TBFC** YARA rule and prints exact string matches and locations.

---

### **1️⃣ How many images contain the string `TBFC`?**

```
5
```

---

### **2️⃣ What regex would match a string starting with `TBFC:` followed by alphanumeric characters?**

```
/TBFC:[A-Za-z0-9]+/
```

---

### **3️⃣ What is the message sent by McSkidy?**

```
Find me in HopSec Island
```

---
