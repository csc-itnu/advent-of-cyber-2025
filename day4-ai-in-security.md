**Room Link**: [https://tryhackme.com/room/AIforcyber-aoc2025-y9wWQ1zRgB](https://tryhackme.com/room/AIforcyber-aoc2025-y9wWQ1zRgB)

## ▶️ UnixGuy | Cyber Security – Day 4 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/L_jhH_PucX4?si=GoqQCiKFOK4ic8rm

---

# 🎄 Advent of Cyber 2025 — Day 4 Write-Up  
## 🧩 AI in Security — *old sAInt nick*

<img width="1022" height="567" alt="banner" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/banner4.png?raw=true" />

---

## 🚀 Step 1 — Visit the Challenge Machine  
Navigate to:

```
http://MACHINE_IP
```

Generate the malicious script using the AI tool.

<img width="1920" height="1080" alt="generate script" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/0begin.png?raw=true" />

---

## 🛠️ Step 2 — Save & Modify the Script  
Replace `MACHINE_IP` inside the generated script with **your actual target IP**.

<img width="1920" height="1080" alt="script edit" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/1script.png?raw=true" />

---

## ▶️ Step 3 — Execute the Script or Perform Manual SQLi  
Option A — Run the script and retrieve the flag.  
Option B — Manually visit:

```
http://<target-ip>:5000
```

Use the SQL injection payload provided by AI to log in.

<img width="1920" height="1080" alt="login" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/3login.png?raw=true" />

<img width="1920" height="1080" alt="flag" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/4flag.png?raw=true" />

---

## 🧩 Step 4 — Complete All Stages  
Finish the sequence of AI-assisted tasks to unlock the final flag.

<img width="1920" height="1080" alt="final flag" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day4/5flag.png?raw=true" />

---

# ✅ Challenge Answers

---

### **1️⃣ Complete the AI showcase by progressing through all stages. What is the final flag?**

```
THM{AI_MANIA}
```

---

### **2️⃣ What flag is printed by the script after execution?**

```
THM{SQLI_EXPLOIT}
```

---

