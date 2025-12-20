**Room Link:**  
https://tryhackme.com/room/ICS-modbus-aoc2025-g3m6n9b1v4

## ▶️ Claus for Concern – Day 19 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/-RyO0yn3pZ8

---

# 🎄 Advent of Cyber 2025 — Day 19 Write-Up  
## 🧩 ICS / Modbus — Claus for Concern

---

## 📘 Scenario Overview

Day 19 of Advent of Cyber 2025 focuses on **Industrial Control Systems (ICS)** and **Operational Technology (OT)** security.  
The scenario simulates a compromised PLC-controlled drone delivery system responsible for shipping Christmas presents.

Although system dashboards report everything as *operational*, customers receive **chocolate eggs instead of Christmas gifts**.  
This discrepancy indicates a **logic-level attack**, not a hardware failure.

The attacker exploited **Modbus TCP**, a legacy industrial protocol, to directly manipulate PLC registers and coils.

---

## 🎯 Objectives

- Identify malicious Modbus configuration changes  
- Investigate PLC holding registers and coils  
- Avoid triggering a hidden trap mechanism  
- Safely restore Christmas deliveries  
- Capture the final flag  

---

## 🔍 Initial Reconnaissance

An Nmap scan of the target system revealed the following exposed services:

- **22/tcp** → SSH  
- **80/tcp** → HTTP (CCTV monitoring interface)  
- **502/tcp** → Modbus TCP (PLC communications)  

Modbus TCP is particularly dangerous because it provides:
- ❌ No authentication  
- ❌ No encryption  
- ❌ No authorization  

Any user with network access can directly read or write PLC values.

---

## 📷 CCTV Visual Confirmation

Accessing the web interface on port 80 revealed a live CCTV feed showing:

- Conveyor belts actively running  
- Drones loading packages  
- **Chocolate eggs** on the production line  
- System status marked as **Compromised**  

This confirmed the issue was caused by **malicious logic manipulation**.

---

## 🏭 PLC & Modbus Investigation

The PLC communicates using standard Modbus data structures:

- **Holding Registers** → Numeric configuration values  
- **Coils** → Boolean control flags  

---

## 📌 Key Holding Registers

**HR0 — Package Type Selection**  
- `0` = Christmas Gifts  
- `1` = Chocolate Eggs  
- `2` = Easter Baskets  

**HR1 — Delivery Zone**  
- `1–9` = Normal Zones  
- `10` = Ocean Dump Zone  

**HR4 — System Signature**  
- Used to identify system compromise  

---

## 📌 Key Coils

- **C10** — Inventory Verification  
- **C11** — Protection / Trap Mechanism  
- **C12** — Emergency Dump Protocol  
- **C13** — Audit Logging  
- **C14** — Christmas Restored Flag  
- **C15** — Self-Destruct Armed Status  

---

## 📊 Compromised System State



HR0 = 1 → Chocolate Eggs forced
HR1 = 5 → Normal delivery zone
HR4 = 666 → Eggsploit signature detected

C10 = False → Inventory verification disabled
C11 = True → Protection mechanism ENABLED
C12 = False → Emergency dump inactive
C13 = False → Audit logging disabled
C15 = False → Self-destruct not yet armed


The presence of **666** confirms the use of the **Eggsploit** framework.

---

## 🚨 Trap Mechanism Analysis

The attacker implemented a **booby-trap** using PLC logic.

If **HR0 is modified while C11 = True**:
- C15 arms immediately  
- A 30-second countdown begins  
- C12 activates (emergency dump)  
- HR1 switches to Zone 10 (Ocean)  
- All inventory is destroyed  
- The challenge must be restarted  

This mirrors how real-world ICS safety mechanisms can be weaponized.

---

## 🛠️ Safe Remediation Process

The restoration **must follow a strict order**.

### Step 1 — Disable Protection Mechanism


C11 = False


### Step 2 — Restore Christmas Package Type


HR0 = 0


### Step 3 — Enable Inventory Verification


C10 = True


### Step 4 — Enable Audit Logging


C13 = True


### Step 5 — Final Verification


C12 = False → No emergency dump
C15 = False → Self-destruct never armed
C14 = True → Christmas restored


---

## 📈 Post-Remediation Confirmation

- CCTV feed updates in real time  
- Conveyor belts now show Christmas presents  
- Drones load correct items  
- System status returns to **Operational**  

---

# ✅ Challenge Answers

---

### **1️⃣ What port is commonly used by Modbus TCP?**


502


### **2️⃣ What value in HR0 caused incorrect deliveries?**


1


### **3️⃣ What value confirmed Eggsploit compromise?**


666


### **4️⃣ Which coil acted as the protection trap?**


C11


### **5️⃣ What is the final flag?**


THM{eGgMas0V3r}


---

## 🧠 Key Takeaways

- Modbus TCP is inherently insecure  
- Exposed OT services pose severe risks  
- Register-level attacks bypass UIs entirely  
- Safety mechanisms can be weaponized  
- Order of operations is critical in ICS response  
- Logic attacks can have real-world physical impact  

---

## 🎉 Conclusion

Day 19 provides a realistic and educational ICS incident response scenario.  
It demonstrates how legacy industrial protocols can be abused and why defenders must fully understand system logic before making changes.

Christmas was saved — not by brute force, but by **careful, informed remediation**.

---

✅ **Challenge Completed Successfully**