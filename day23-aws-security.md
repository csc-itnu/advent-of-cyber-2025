**Room Link:**  
https://tryhackme.com/room/cloudenum-aoc2025-y4u7i0o3p6

## ▶️ Tech with Jono – Day 23 Video Walkthrough  
Official walkthrough for quick onboarding:

🔗 **YouTube Link:**  
https://youtu.be/9ZLS4iUFi00?si=4hxj_umEeklFyRBL

---

# 🎄 Advent of Cyber 2025 — Day 23 Write-Up  
## 🧩 AWS Security — S3cret Santa

---

## 📘 Review the Theory

Refer to the TryHackMe theory section before starting this.

---

# ✅ Challenge Answers

---

### **1️⃣ Run `aws sts get-caller-identity`. What is the value of the `Account` parameter?**

<img width="1880" height="858" alt="aws sts identity" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/1.png?raw=true" />

```
123456789012
```

---

### **2️⃣ What IAM component is used to describe permissions assigned to a user or group?**

```
policy
```

<img width="1008" height="365" alt="iam policy" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/2.png?raw=true" />
<img width="1402" height="447" alt="policy details" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/3.png?raw=true" />

---

### **3️⃣ What is the name of the policy assigned to `sir.carrotbane`?**

<img width="1920" height="827" alt="policy name" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/4ans.png?raw=true" />

```
SirCarrotbanePolicy
```

---

<img width="1205" height="696" alt="assume role" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/5.png?raw=true" />
<img width="1524" height="322" alt="role permissions" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/6.png?raw=true" />

---

### **4️⃣ Apart from `GetObject` and `ListBucket`, what other action can be performed by assuming the `bucketmaster` role?**

<img width="1900" height="860" alt="bucketmaster permissions" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/7.png?raw=true" />

```
ListAllMyBuckets
```

<img width="1902" height="336" alt="list buckets" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/8.png?raw=true" />

---

### **5️⃣ What are the contents of the `cloud_password.txt` file?**

<img width="1393" height="509" alt="cloud password file" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/9.png?raw=true" />
<img width="1700" height="819" alt="file contents" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/10.png?raw=true" />
<img width="1910" height="380" alt="final flag" src="https://github.com/csc-itnu/advent-of-cyber-2025/blob/main/images/day23/11.png?raw=true" />

```
THM{more_like_sir_cloudbane}
```

---
