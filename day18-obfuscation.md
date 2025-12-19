**Room Link:**  
https://tryhackme.com/room/obfuscation-aoc2025-e5r8t2y6u9

## ▶️ The Social Dork – Day 18 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/gOj13IC39hA?si=aVW5hQiUbOgZFRg3

---

# 🎄 Advent of Cyber 2025 — Day 18 Write-Up  
## 🧩 Obfuscation — The Egg Shell File

---

# ✅ Challenge Answers

---

### **1️⃣ What is the first flag after deobfuscating the C2 URL and running the script?**

<img width="1917" height="1080" alt="c2 obfuscation" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/1first.png?raw=true" />

The variable names provide a strong hint that the value is **Base64-encoded**.

<img width="1920" height="1079" alt="base64 decode" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/2decode.png?raw=true" />

After decoding the C2 URL and executing the script:

<img width="1918" height="1079" alt="script execution" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/3run.png?raw=true" />

```
THM{C2_De0bfuscation_29838}
```

---

### **2️⃣ What is the second flag after obfuscating the API key and running the script again?**

<img width="1917" height="1080" alt="api obfuscation" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/4prog.png?raw=true" />

<img width="1920" height="1076" alt="api decode" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/5decode.png?raw=true" />

<img width="1920" height="1073" alt="final flag" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day18/6final.png?raw=true" />

```
THM{API_Obfusc4tion_ftw_0283}
```

---
