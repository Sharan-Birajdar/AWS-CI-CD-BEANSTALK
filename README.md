# Code2Cloud 🚀

This project demonstrates a fully automated CI/CD pipeline using **AWS Elastic Beanstalk**, **AWS CodePipeline**, and **GitHub**.  
Whenever code is pushed to the GitHub repository, the pipeline automatically builds and deploys the latest version to Elastic Beanstalk.

![Alt text](https://github.com/Sharan-Birajdar/Code2Cloud/blob/main/Doc/Images/architecture%20diagram.png?raw=true)

---

## 🔧 Project Architecture

1. **GitHub (Source Control)**
   - Stores the website/application source code.
   - Any push to the main branch triggers the pipeline.

2. **AWS CodePipeline (CI/CD Orchestrator)**
   - Detects changes in GitHub.
   - Automatically delivers the new version to Elastic Beanstalk.

3. **AWS Elastic Beanstalk (Hosting Platform)**
   - Deploys and manages the application.
   - Provides auto-scaling and load balancing.

---

## ⚙️ Technologies Used

- **AWS Elastic Beanstalk** – Application hosting  
- **AWS CodePipeline** – Continuous Integration & Deployment  
- **GitHub** – Source control and collaboration  
- **HTML / CSS / JavaScript** – Frontend code (replace with your stack if needed)  

---

## 🚀 How It Works

1. Push code changes to the `main` branch of this GitHub repository.  
2. CodePipeline automatically pulls the changes.  
3. Elastic Beanstalk deploys the latest build.  
4. The website updates without manual intervention. 🎉  

---

## 🔑 Key Benefits

- Zero-downtime deployments  
- Automated CI/CD workflow  
- Scalable & managed infrastructure with AWS Beanstalk  
- Easy rollback to previous versions  

---

## 📝 Future Enhancements

- Add automated testing before deployments  
- Enable notifications (Slack/Email) for pipeline events  
- Add monitoring with AWS CloudWatch  


