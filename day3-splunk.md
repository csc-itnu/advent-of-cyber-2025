**Room Link**: [https://tryhackme.com/room/splunkforloganalysis-aoc2025-x8fj2k4rqp](https://tryhackme.com/room/splunkforloganalysis-aoc2025-x8fj2k4rqp)

## ▶️ Mad Hat – Day 3 Video Walkthrough  
We are providing the official Day 3 walkthrough video for quick onboarding:

🔗 **YouTube Link:** [https://youtu.be/0cuAsDTfNbA?si=Sz6V86u9fB3isdf1](https://youtu.be/0cuAsDTfNbA?si=Sz6V86u9fB3isdf1)

<br>




# 🎄 Advent of Cyber 2025 — Day 3 Write-Up  
## 🧩 Splunk Basics - Did you SIEM?
<img width="1022" height="567" alt="banner" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/banner3.png?raw=true" />
---




## ✅ Challenge Answers — Log Analysis

### **1️⃣ Attacker IP found attacking and compromising the web server**
<img width="1920" height="1080" alt="1clientip" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/1clientip.png?raw=true" />

```
index=main 
```


<h3>Answer:</h3>

```
198.51.100.55
```

---

### **2️⃣ Peak traffic day in the logs (YYYY-MM-DD)**
<img width="1920" height="1080" alt="2finaldate" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/2finaldate.png?raw=true" />


```
index=main sourcetype=web_traffic | timechart span=1d count |  sort -count
```


<h3>Answer:</h3>

```
2025-10-12
```

---

### **3️⃣ Count of `Havij` user_agent events**
<img width="1920" height="1080" alt="3havij" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/3havij.png?raw=true" />
<h3>Answer:</h3>

```
993
```

---

### **4️⃣ Number of path-traversal attempts observed**
<img width="1920" height="1080" alt="4pathtraversal" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/4pathtraversal.png?raw=true" />
<h3>Answer:</h3>

```
658
```

---

### **5️⃣ Bytes transferred to the C2 server from the compromised web server**
<img width="1920" height="1080" alt="5bytestransfer" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day3/5bytestransfer.png?raw=true" />

```
index=main sourcetype=firewall_logs src_ip="10.10.1.5" dest_ip="198.51.100.55" AND action="ALLOWED" | stats sum(bytes_transferred) by src_ip
```


<h3>Answer:</h3>

```
126167
```
