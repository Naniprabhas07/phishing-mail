# 📧 Cyber Security Internship - Task 2

## 📌 Task: Analyze a Suspicious Email for Phishing Indicators

This repository contains all the files and documentation for **Task 2** of my Cyber Security Internship, which focuses on analyzing a suspicious email to identify phishing characteristics. The objective is to examine headers, links, content, and metadata to uncover phishing tactics and improve email threat analysis skills.

---

## 🛠 Tools Used

- **Outlook** – To extract full email headers  
- **MxToolbox** – Header analysis for SPF, DKIM, and DMARC  
- **URLScan.io** – To inspect embedded links  
- **My Custom Phishing Detection Tool** – Built to detect malicious URLs and text content  
- **VS Code** – For saving and reviewing email content  

---

## 🧪 Steps Followed

### 1️⃣ Extracted Email Headers from Outlook  
- Navigated to: `File > Properties > Show Original`  
- Copied and saved the full email header  

### 2️⃣ Header Analysis (MxToolbox)  
- Pasted the header into [MxToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)  
- Observations:
  - ✅ SPF: **Fail**
  - ✅ DKIM: **Fail**
  - ✅ DMARC: **Fail**
  - ✅ Return Path: `mailer@mailer.netcorecloud.com`
  - 🚩 **Sender mismatch**: `HDFCsecurities@hdfcsec.com` (spoofed)

### 3️⃣ Email Content and Link Analysis  
- Saved full email body as `phishing_sample.txt`  
- Identified a suspicious embedded link:  
  `http://secure-update-hdfc.verification-alerts.ru`  
- Scanned the link using [URLScan.io](https://urlscan.io)  
  - 🔍 Result: Redirects to a phishing landing page  
  - 🌐 Domain hosted in Russia

### 4️⃣ Custom Tool Analysis  
- Ran `phishing_sample.txt` through my own phishing detection tool  
- Results:
  - 🚨 Detected keywords such as: `urgent`, `verify`, `account blocked`
  - ❌ Mismatched URLs flagged from database comparison
  - ✅ Classification: **Scam**

---

## 🔐 Outcome

This task improved my hands-on skills in:
- Email header forensics  
- Sender authenticity and domain validation  
- URL and domain threat analysis  
- Recognizing phishing tactics and language patterns  

---

## 🧠 Key Concepts Demonstrated

- Email spoofing detection using headers  
- SPF, DKIM, and DMARC evaluation  
- Phishing link scanning and domain analysis  
- IP address tracing and mail relay checking  
- Secure email handling awareness  

---

> 📝 **Disclaimer:** All email analysis was performed in a secure, offline lab environment strictly for educational purposes. No real user credentials or personal data were exposed.
