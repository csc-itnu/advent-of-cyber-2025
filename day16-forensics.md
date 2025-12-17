**Room Link:**  
https://tryhackme.com/room/registry-forensics-aoc2025-h6k9j2l5p8

## ▶️ cyb3rvalkyrie – Day 16 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/wQaa8Fj52EA?si=dqXPVygVDEamBwFh

---

# 🎄 Advent of Cyber 2025 — Day 16 Write-Up  
## 🧩 Forensics - Registry Furensics

---


# ✅ Challenge Answers

---
<img width="1920" height="666" alt="0START" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/0START.png?raw=true" />
<img width="3216" height="1844" alt="01" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/01.png?raw=true" />
<img width="2560" height="1616" alt="02" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/02.png?raw=true" />
<img width="2564" height="1610" alt="03" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/03.png?raw=true" />
same way load SOFTWARE, NTUSER.DAT Hives also.



### **1️⃣ What application was installed on the dispatch-srv01 before the abnormal activity started?**

<img width="1590" height="150" alt="2before1ans" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/2before1ans.png?raw=true" />

<img width="1920" height="893" alt="1stans" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/1stans.png?raw=true" />

```
DroneManager Updater
```

---

### **2️⃣ What is the full path where the user launched the application (found in question 1) from?**

<img width="1558" height="216" alt="4before2ndans" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/4before2ndans.png?raw=true" />
<img width="1920" height="878" alt="5ans2" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/5ans2.png?raw=true" />


```
C:\Users\dispatch.admin\Downloads\DroneManager_Setup.exe
```

Which value was added by the application to maintain persistence on startup?

<img width="1578" height="235" alt="7before3" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/7before3.png?raw=true" />
<img width="1526" height="1033" alt="8ans3" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day16/8ans3.png?raw=true" />


```
"C:\Program Files\DroneManager\dronehelper.exe" --background
```



---
