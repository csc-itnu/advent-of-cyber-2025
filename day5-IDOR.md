**Room Link:**  
https://tryhackme.com/room/idor-aoc2025-zl6MywQid9

## ▶️ David Ackerman – Day 5 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/geNAA2g-ZnY?si=LOn6plfunNkIichE

---

# 🎄 Advent of Cyber 2025 — Day 5 Write-Up  
## 🧩 IDOR — Santa’s Little IDOR

---

# ✅ Challenge Answers

---

### **1️⃣ What does IDOR stand for?**

```
Insecure Direct Object Reference
```

---

### **2️⃣ What type of privilege escalation are most IDOR cases?**

```
Horizontal
```

---

## 🧪 Step-by-Step Exploitation

### ▶️ Login with given credentials  
<img width="1920" height="985" alt="1login" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/1login.png?raw=true" />

---

### ▶️ Open DevTools → Network tab → Click **view-details**  
This reveals the request containing `user_id`.

<img width="1917" height="991" alt="2viewaccount" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/2viewaccount.png?raw=true" />

---

### ▶️ Modify the `user_id` Parameter  
Changing the value reveals different parents.  
At `user_id=15`, we discover **10 children**.

<img width="1917" height="991" alt="2uid15" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/2uid15.png?raw=true" />

---

### **3️⃣ Exploiting the IDOR found in `view_accounts`: What is the user_id of the parent with 10 children?**

```
15
```

---

# 🎁 Bonus Task 1 — Child Endpoint Enumeration

### **Base64** or **MD5**  
I solved using MD5 endpoint.

<img width="1914" height="997" alt="3md5" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/3md5.png?raw=true" />

I identified the hash as **MD5(11)**.

<img width="1914" height="997" alt="3md511" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/3md511.png?raw=true" />

---

### Uploading number list (1–20) via Burp Intruder  
Follow the steps:

<img width="1919" height="1046" alt="4burpproxy" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/4burpproxy.png?raw=true" />

<img width="734" height="550" alt="5extentionset" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/5extentionset.png?raw=true" />

<img width="1912" height="946" alt="6reqtoburp" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/6reqtoburp.png?raw=true" />

<img width="1919" height="790" alt="7intrudersent" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/7intrudersent.png?raw=true" />

<img width="1918" height="1040" alt="8progress" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/8progress.png?raw=true" />

<img width="1919" height="990" alt="10attack" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/10attack.png?raw=true" />

<img width="1920" height="859" alt="11ans1" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/11ans1.png?raw=true" />

### **4️⃣ Bonus Answer (Child ID):**

```
19
```

---

# 🎁 Bonus Task 2 — Voucher Claim Endpoint

Navigate to:

```
/parents/vouchers/claim
```

<img width="1910" height="984" alt="12claim" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/12claim.png?raw=true" />

Perform the attack:

<img width="1895" height="1018" alt="13startattack" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/13startattack.png?raw=true" />

Success:

<img width="1904" height="1037" alt="14final" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day5/14final.png?raw=true" />

### **5️⃣ Final Bonus Flag**

```
22643e00-c655-11f0-ac99-026ccdf7d769
```

---
