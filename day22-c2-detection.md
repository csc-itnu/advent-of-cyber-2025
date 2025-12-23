**Room Link:**  
https://tryhackme.com/room/detecting-c2-with-rita-aoc2025-m9n2b5v8c1

## ▶️ Grant Collins – Day 22 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/_aezrep95mo?si=5EV70b264rx4_Wnp

---

# 🎄 Advent of Cyber 2025 — Day 22 Write-Up  
## 🧩 C2 Detection — Command & Carol

---

## 📘 Review the Theory from tryhackme

Refer to the theory section of tryhackme before starting the investigation.

<img width="1920" height="942" alt="theory 1" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/1.png?raw=true" />
<img width="1204" height="179" alt="theory 2" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/2.png?raw=true" />
<img width="1910" height="266" alt="theory 3" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/3final.png?raw=true" />
<img width="1920" height="56" alt="theory 4" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/4.png?raw=true" />

---

# ✅ Challenge Answers

---

### **1️⃣ How many hosts are communicating with `malhare.net`?**

<img width="1356" height="367" alt="hosts communicating" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/5ans1.png?raw=true" />

```
6
```

---

### **2️⃣ Which threat modifier indicates the number of hosts communicating with a destination?**

```
prevalence
```

---

### **3️⃣ What is the highest number of connections to `rabbithole.malhare.net`?**

<img width="1920" height="949" alt="connections count" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/6ans3.png?raw=true" />

```
40
```

---

### **4️⃣ What query was used to identify high-frequency beaconing behavior?**

<img width="1919" height="916" alt="beacon query" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/7final.png?raw=true" />

```
dst:rabbithole.malhare.net beacon:>=70 sort:duration-desc
```

---

### **5️⃣ Which port did host `10.0.0.13` use to connect to `rabbithole.malhare.net`?**

<img width="1920" height="911" alt="destination port" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day22/8.png?raw=true" />

```
80
```

---
