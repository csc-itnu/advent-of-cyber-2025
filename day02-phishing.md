

**Room Link**: [https://tryhackme.com/room/phishing-aoc2025-h2tkye9fzU](https://tryhackme.com/room/phishing-aoc2025-h2tkye9fzU)

## ▶️ John Hammond – Day 2 Video Walkthrough  
We are providing the official Day 2 walkthrough video for quick onboarding:

🔗 **YouTube Link:** [https://youtu.be/w8O8FcRgDXU?si=y_AI4wT_e4s6Bm1P](https://youtu.be/w8O8FcRgDXU?si=y_AI4wT_e4s6Bm1P)

<br>




# 🎣 Advent of Cyber 2025 — Day 2 Write-Up  
## 🧩 Social Engineering & Phishing
<img width="1022" height="567" alt="banner" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/banner.png?raw=true" />
---

## 🧠 Social Engineering — Quick Overview  
Social engineering is **human hacking** — manipulating people into making security mistakes like:

- Giving passwords  
- Clicking malicious links  
- Opening infected attachments  
- Approving fake payments  
- Sharing sensitive info  

Attackers exploit **urgency**, **fear**, **curiosity**, **authority**, and **carelessness**.  
It has nothing to do with hacking computers — it’s about hacking **people**.

---

## 🎯 Phishing  
Phishing = **social engineering through messages** (email, SMS, QR codes, phone calls, DMs).

Goal:  
👉 Make the victim **click**, **open**, or **reply**, so the attacker can steal credentials, money, or access.

---

## 🧠 Anti-Phishing Mnemonic: **S.T.O.P.**

### 1️⃣ First S.T.O.P. — Ask Yourself  
- **S**uspicious?  
- **T**elling me to click?  
- **O**ffering amazing deal?  
- **P**ushing urgency?  

### 2️⃣ Second S.T.O.P. — Do This  
- **S**low down  
- **T**ype the URL manually  
- **O**pen nothing unexpected  
- **P**rove the sender  

If you just follow this, you avoid 90% of phishing attacks.

---

## 🪤 Building the Trap — Fake Login Page  

The attacker hosts a fake TBFC login portal using:

```
./server.py
```
<img width="1079" height="152" alt="1serverisrunning" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/1serverisrunning.png?raw=true" />


Any submitted credentials appear **directly in your terminal** — no database needed.

---

## 📧 Delivering the Phish Using S.E.T. (Social-Engineer Toolkit)

Launch the tool:

```
setoolkit
```
<img width="1208" height="44" alt="2setoolkit" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/2setoolkit.png?raw=true" />

Choose:

```
1) Social-Engineering Attacks
5) Mass Mailer Attack
1) Single Email Address
```
<img width="953" height="345" alt="3SEattacks" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/3SEattacks.png?raw=true" />
<img width="1736" height="736" alt="4final" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/4final.png?raw=true" />


### Required Inputs

| Prompt | Value |
|--------|--------|
| Send to | factory@wareville.thm |
| Use server/open relay | 2 |
| From address | updates@flyingdeer.thm |
| From name | Flying Deer |
| SMTP server | target-ip |
| SMTP port | 25 |
| High priority | no |
| Attach file | n |
| Inline file | n |
| Subject | Shipping Schedule Changes |


### 📜 Email Body (Plaintext)

```
Hello,
Kindly note that there have been significant changes to the shipping schedules due to increased shipping orders.
Please confirm the new schedule by visiting http://10.49.101.188:8000
Best regards,
Flying Deer
END
```
<img width="1543" height="880" alt="5mail" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/5mail.png?raw=true" />

<b><p>SET sends the email to the target machine and it (AI-Agent) will automatically click the url and enter the creds that will come to us on our attacker machine.
Your server terminal immediately shows the captured credentials.</p></b>

<img width="1767" height="412" alt="6logs" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/6logs.png?raw=true" />

---

# ✅ Challenge Answers

### 1️⃣ TBFC Portal Password  
```
unranked-wisdom-anthem
```

---

### 2️⃣ Total Toys Expected for Delivery  
Visit:

```
http://<target-ip>
```

Use harvested creds → read mailbox → find shipment stats.

<img width="1892" height="930" alt="7loginpage" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/7loginpage.png?raw=true" />
<img width="1912" height="776" alt="8final" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day2/8final.png?raw=true" />


Answer:

```
1984000
```

---

🎅 **Keep practicing — phishing kills companies more often than malware.**  
🔐 Stay alert, stay skeptical, stay safe.
