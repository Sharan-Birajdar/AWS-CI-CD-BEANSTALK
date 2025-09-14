# 🚀 Setup Guide: Code2Cloud (CI/CD with AWS Elastic Beanstalk & CodePipeline)

This guide walks you through setting up the project so that pushing code to **GitHub** automatically deploys it to **AWS Elastic Beanstalk** using **AWS CodePipeline**.

---

## ✅ Prerequisites

* AWS Account
* IAM user with:

  * `AdministratorAccess` or required permissions for **Elastic Beanstalk**, **CodePipeline**, **CodeBuild**, and **S3**
* GitHub account with your project repository
* Installed:

  * [Git](https://git-scm.com/)
  * [AWS CLI](https://aws.amazon.com/cli/)

---

## ⚙️ Step 1: Create an Elastic Beanstalk Environment

1. Go to **AWS Console → Elastic Beanstalk**
2. Click **Create Application**
3. Select:

   * Platform: **"PHP"**, **"Node.js"**, or **"Python"** (choose based on your code) OR use **"Static Web"** for HTML/CSS/JS
   * Environment: **Web Server Environment**
4. Upload a sample ZIP of your project (you’ll connect GitHub later).
5. Click **Create** – Beanstalk will launch an environment (EC2, Auto Scaling, Load Balancer).

---

## ⚙️ Step 2: Prepare Your GitHub Repository

1. Push your website code to a **public or private repo** on GitHub. Example:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

2. Confirm code is visible in your GitHub repo.

---

## ⚙️ Step 3: Create a Connection Between AWS and GitHub

1. Go to **AWS Console → Developer Tools → Connections**
2. Click **Create Connection**
3. Choose **GitHub** → Authenticate with OAuth → Authorize AWS to access your repo
4. Save the connection

---

## ⚙️ Step 4: Create a CodePipeline

1. Go to **AWS Console → CodePipeline**

2. Click **Create Pipeline**

3. Enter pipeline name: `Code2CloudPipeline`

4. **Source Stage**:

   * Provider: **GitHub**
   * Select the connection created in Step 3
   * Choose your repo & branch (`main`)

5. **Build Stage**:

   * If just a static site, skip build
   * If dynamic app, use **CodeBuild** with a `buildspec.yml`

6. **Deploy Stage**:

   * Provider: **Elastic Beanstalk**
   * Choose the application & environment created in Step 1

7. Review & **Create Pipeline**

---

## ⚙️ Step 5: Test the Pipeline

1. Push a code change to GitHub:

   ```bash
   git add .
   git commit -m "Updated index.html"
   git push origin main
   ```

2. CodePipeline will automatically trigger:

   * Source → Build (if configured) → Deploy

3. Elastic Beanstalk updates the environment with the new code

---

## 🎉 Done!

Now your project is fully automated:

* Edit code → Push to GitHub → AWS updates website 🚀

