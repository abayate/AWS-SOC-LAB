# 🛡️ AWS Cloud SOC Lab

This lab simulates a real-world **Security Operations Center (SOC)** using AWS services. It showcases:

- 🖥️ EC2 (simulated asset)
- 🕵️ GuardDuty (threat detection)
- 🧩 Security Hub (alert aggregation)


## 🚀 Step-by-Step Setup

### 1️⃣ Launch an EC2 Instance

Use EC2 to simulate a vulnerable cloud asset.

#### Configuration:
- **AMI:** Amazon Linux 2
- **Instance type:** t2.micro (free tier)
- **Inbound rule:** SSH (port 22) open to `0.0.0.0/0`  
  > This allows us to simulate SSH brute-force attacks

[EC2 Screenshot](ec2.pdf)

---

### 2️⃣ Enable Amazon GuardDuty

GuardDuty is AWS’s intelligent threat detection service.

#### Setup:
- Go to **Amazon GuardDuty**
- Click **Enable**
- It auto-monitors: VPC Flow Logs, CloudTrail, and DNS logs

#### Example Finding:
> 🛑 `UnauthorizedAccess:EC2/SSHBruteForce`

![GuardDuty Screenshot]()

---

### 3️⃣ Set Up AWS Security Hub

Security Hub collects and correlates findings from GuardDuty and other services.

#### Setup:
- Go to **AWS Security Hub**
- Click **Enable**
- Integrates with GuardDuty by default

#### Benefits:
- Single-pane view of alerts
- Prioritize alerts by severity

![Security Hub Screenshot]()

---

## 🔍 What I Learned

- How to simulate threat detection using AWS
- The role of each AWS service in cloud security
- How alerts are generated, visualized, and triaged

---

## 🧠 Technologies Used

- AWS EC2  
- Amazon GuardDuty  
- AWS Security Hub  

---

## 👨‍🎓 Author

**Anthony Bayate Jr.**  
Cybersecurity & IT Student, Kean University  
[LinkedIn](https://linkedin.com/in/abayate) • [GitHub](https://github.com/abayate)

---

## 📜 License

This project is under the [MIT License](./LICENSE)
