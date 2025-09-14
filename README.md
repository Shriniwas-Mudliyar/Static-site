# Static-site

# 🌐 Static Website Hosting on AWS (S3 + CloudFront)

## 📌 Project Overview

This project demonstrates how to host and deliver a static website using **Amazon S3** for storage and **Amazon CloudFront** as a Content Delivery Network (CDN).
The goal was to deploy a fast, secure, and globally distributed portfolio website.

🔗 **Live Demo**: d287zfoj2oggb1.cloudfront.net

---

## 🏗️ Architecture

* **Amazon S3** → Stores static website files (HTML, CSS, JS, Images).
* **Amazon CloudFront** → Distributes content globally with low latency.
* **Route 53 (optional)** → For custom domain mapping.
* **IAM** → For secure access and permissions.

**Architecture Diagram (high-level):**

```
User ---> CloudFront (CDN) ---> S3 (Static Website Hosting)
```

---

## ⚙️ Steps to Deploy

### 1️⃣ Create and Configure S3 Bucket

* Created an **S3 bucket** named `shriniwas-profile`.
* Uploaded website files (`index.html`, `about.html`, `styles.css`, etc.).
* Set **bucket policy** to allow public read access for objects.

### 2️⃣ Set Up CloudFront Distribution

* Created a **CloudFront distribution**.
* Set the **origin** to the S3 bucket.
* Configured **default root object** = `index.html`.
* Enabled **HTTP → HTTPS redirection** for security.

---

## ✅ Key Learnings

* Hosting static websites on **S3** is simple and cost-effective.
* **CloudFront** improves performance by caching content globally.
* Proper **IAM & bucket policies** ensure security.
* Learned how to automate deployments using the **AWS CLI**.

---

## 📌 Next Improvements

* Add **CI/CD pipeline** using GitHub Actions + S3 + CloudFront.
* Integrate **WAF (Web Application Firewall)** for better security.
* Use **Terraform/CloudFormation** for Infrastructure as Code.

---

💡 *This project showcases AWS fundamentals for hosting and delivering static websites efficiently.*
