**Room Link:**  
https://tryhackme.com/room/race-conditions-aoc2025-d7f0g3h6j9

## ▶️ The Bearded I.T. Dad – Day 20 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/PGQNlM45mqQ?si=HpVA-V7xlKHHkOqO

---

# 🎄 Advent of Cyber 2025 — Day 20 Write-Up  
## 🧩 Race Conditions — Toy to The World

---

# ✅ Challenge Answers

---

## 🧸 Exploiting the Race Condition

---

### **1️⃣ What is the flag once the stock becomes negative for _SleighToy Limited Edition_?**

<img width="1358" height="504" alt="initial stock" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/1.png?raw=true" />
<img width="1036" height="311" alt="ordering process" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/2.png?raw=true" />
<img width="735" height="489" alt="burp setup" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/3.png?raw=true" />
<img width="740" height="492" alt="intruder config" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/4.png?raw=true" />
<img width="1363" height="494" alt="race execution" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/5.png?raw=true" />
<img width="969" height="378" alt="stock manipulation" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/6.png?raw=true" />

---

### 🔐  Credentials

<pre>
username: attacker
password: attacker@123
</pre>

<img width="499" height="318" alt="login" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/7.png?raw=true" />
<img width="1142" height="275" alt="order confirm" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/8.png?raw=true" />
<img width="1131" height="289" alt="negative stock" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/9.png?raw=true" />
<img width="1165" height="428" alt="flag process" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/10.png?raw=true" />
<img width="1366" height="443" alt="flag screen" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/11.png?raw=true" />
<img width="685" height="558" alt="race success" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/12.png?raw=true" />
<img width="303" height="322" alt="final step" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/13.png?raw=true" />
<img width="506" height="456" alt="confirmation" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/14.png?raw=true" />
<img width="511" height="514" alt="flag prompt" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/15.png?raw=true" />
<img width="520" height="464" alt="race done" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/16.png?raw=true" />

Once the race condition succeeds the flag is revealed:

<img width="1920" height="1080" alt="flag 1" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/FLAG1.png?raw=true" />

```
THM{WINNER_OF_R@CE007}
```

---

### **2️⃣ Repeat the attack for _Bunny Plush (Blue)_. What is the flag once the stock becomes negative?**

The **same race-condition technique** is reused against **Bunny Plush (Blue)** by rapidly submitting parallel purchase requests.

<img width="1920" height="1080" alt="flag 2" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day20/flag2.png?raw=true" />

```
THM{WINNER_OF_Bunny_R@ce}
```

---
