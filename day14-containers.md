**Room Link:**  
https://tryhackme.com/room/container-security-aoc2025-z0x3v6n9m2

## ▶️ David Ackerman – Day 14 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/600aXKJ9oJ8?si=0CDEHOLW-L1i_LqB

---

# 🎄 Advent of Cyber 2025 — Day 14 Write-Up  
## 🧩 Containers — DoorDasher's Demise

---

# ✅ Challenge Answers

---

### **1️⃣ What exact command lists running Docker containers?**

<img width="1913" height="186" alt="docker ps" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/1dockerps.png?raw=true" />

```
docker ps
```

---

## 🌐 Defaced Website

<img width="1920" height="993" alt="defaced website" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/2defacedweb.png?raw=true" />

---

### **2️⃣ What file is used to define the instructions for building a Docker image?**

```
Dockerfile
```

---

### **3️⃣ What’s the flag?**

<img width="1917" height="118" alt="enter container" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/3entercont.png?raw=true" />

<img width="1920" height="124" alt="docker access" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/4access.png?raw=true" />

At this point, it’s clear the container has access to the Docker socket:


<pre>/var/run/docker.sock</pre>


This is a **critical misconfiguration**.

<img width="1918" height="454" alt="docker exec verified" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/5verfiedexecinsidecont.png?raw=true" />

> **Why this is dangerous:**  
> - In a secure Docker setup, containers **cannot** run Docker commands.  
> - Access to `/var/run/docker.sock` allows interaction with the **host Docker daemon**.  
> - The Docker daemon runs as **root**, meaning container access → **host-level control**.  
> - This results in a **Docker escape**.

<img width="1919" height="497" alt="flag" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/6flag.png?raw=true" />

```
THM{DOCKER_ESCAPE_SUCCESS}
```

---

## 🛠️ Recovery Status

<img width="1920" height="995" alt="site recovered" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/7recovered.png?raw=true" />

---

## 🎁 Bonus Question

**There is a secret code inside the news site running on port 5002.**  
This code is also the password for the `deployer` user — a serious security mistake.

<img width="1920" height="994" alt="bonus secret" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day14/8bonus.png?raw=true" />

```
DeployMaster2025!
```

---
