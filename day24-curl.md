**Room Link:**  
https://tryhackme.com/room/webhackingusingcurl-aoc2025-w8q1a4s7d0

## ▶️ CYBERWOX – Day 24 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/nbJ_tuXZa24?si=0YQF4nU9Jjn2BiJ2

---

# 🎄 Advent of Cyber 2025 — Day 24 Write-Up  
## 🧩 Exploitation with cURL — Hoperation Eggsploit

---

## 📘 Review the Theory

Refer to the TryHackMe theory section before starting this challenge.

---

# ✅ Challenge Answers

---

### **1️⃣ Make a POST request to `/post.php` using `admin:admin`. What flag do you receive?**

<img width="1524" height="138" alt="post flag" src="https://github.com/user-attachments/assets/bb7f5af1-463e-4d69-aefd-eec60b43ca29" />

```
THM{curl_post_success}
```

---

### **2️⃣ Send credentials to `/cookie.php`, save the session cookie, then reuse it. What flag do you receive?**

<img width="1446" height="248" alt="cookie flag" src="https://github.com/user-attachments/assets/3236ef3e-e384-491d-9e17-7a85f175b654" />

```
THM{session_cookie_master}
```

---

### **3️⃣ After brute-forcing `/bruteforce.php`, what is the admin password?**

<img width="1585" height="621" alt="bruteforce" src="https://github.com/user-attachments/assets/a35a72f2-60d9-4d8d-84dd-99ffaa617019" />
<img width="734" height="285" alt="admin password" src="https://github.com/user-attachments/assets/1cc79bdd-b852-4058-8c3c-0014e272e57f" />

```
secretpass
```

---

### **4️⃣ Make a request to `/agent.php` with the User-Agent set to `TBFC`. What flag do you receive?**

<img width="806" height="124" alt="user-agent flag" src="https://github.com/user-attachments/assets/1505cd9b-1dd7-44d1-bae3-01c7bd2b5441" />

```
THM{user_agent_filter_bypassed}
```

---
