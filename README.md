# 🎓 Academic Suite Pro: Ultra-Notes

### *A Cloud-Native, AI-Enhanced Productivity Tool*

## 🌟 Project Overview

This project is a high-performance, distraction-free note-taking application designed for academic environments. It leverages **Cloud Computing** principles to provide a stateless, high-availability experience with integrated AI summarization and professional document generation.

## 📺 Project Walkthrough & Demo
Experience the full workflow of the **Academic Suite Pro**, including real-time AI summarization.

<div align="center">
  <a href="https://youtu.be/inZwOIxI-1Y">
    <img src="https://img.youtube.com/vi/inZwOIxI-1Y/maxresdefault.jpg" alt="Watch the Demo Video" width="800" style="border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.2);">
  </a>
  <p><em>Click the image above to watch the demo on YouTube</em></p>
</div>


## 🚀 Key Features

* **Glassmorphism UI:** A modern, premium interface using CSS variables and professional typography.
* **AI Summarization:** Integrated with **Google Gemini (via OpenRouter)** to provide instant lecture summaries.
* **Data Persistence:** Utilizes **JavaScript LocalStorage** for persistent data safety even after browser restarts.
* **PDF Engine:** Professional export functionality using `html2pdf.js`.
* **Dark Mode & Utilities:** Integrated theme switching and real-time word counting.

---

## 🏗️ Architecture & DevOps Pipeline

To demonstrate industry-standard deployment practices, this project follows a modern **CI/CD workflow**.

### ☁️ Infrastructure

* **Cloud Provider:** AWS (Amazon Web Services)
* **Compute:** EC2 (Elastic Compute Cloud) running **Amazon Linux 2023**.
* **Web Server:** **Nginx** (High-performance reverse proxy and static file server).
* **Security:** Configured via AWS Security Groups (Ports 80 & 22) and restricted IAM access.

### 🤖 Automation (Git Flow)

This project uses **GitHub Actions** for automated deployment.

1. **Secret Injection:** During deployment, GitHub Actions securely injects the `OPENROUTER_API_KEY` into the source code from GitHub Secrets.
2. **Automated SCP:** The pipeline automatically transfers assets to the production directory on EC2.
3. **Permissions Management:** Automated handling of Linux file ownership and security descriptors.

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3 (Modern Flexbox/Grid), JavaScript (ES6+).
* **AI Backend:** OpenRouter API (Gemini 2.0 Flash).
* **DevOps Tools:** Git, GitHub Actions, Linux (SSH/Bash).

---

## 📖 Deployment Instructions

### Prerequisites

* An active **AWS EC2** instance with **Nginx** installed.
* The web directory ownership set to `ec2-user`:
```bash
sudo chown -R ec2-user:ec2-user /usr/share/nginx/html

```



### Local Setup

1. Clone the repository:
```bash
git clone https://github.com/Lihini0202/Simple-Quick-Notes-Web-with-Cloud-computing-basic-parts.git

```


2. Configure GitHub Secrets:
* `EC2_HOST`: Your Public IPv4.
* `EC2_SSH_KEY`: Your `.pem` private key content.
* `OPENROUTER_API_KEY`: Your API key for AI features.



---

## 🛡️ Security Best Practices

* **Principle of Least Privilege:** SSH keys are restricted using `icacls` (Windows) and `chmod` (Linux).
* **Secret Management:** No API keys are hard-coded in the repository; all sensitive data is managed via encrypted GitHub environment variables.

---

## 👤 Author

**Lihini**

* *IT Undergraduate Student*
* Focus: AI/ML, Cloud Computing, and DevOps.

