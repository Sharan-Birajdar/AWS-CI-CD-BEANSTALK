# AWS Elastic Beanstalk CI/CD with CodePipeline & Route 53

This project demonstrates a **fully automated deployment pipeline** for a web application using **AWS Elastic Beanstalk**, **AWS CodePipeline**, **GitHub**, and **Amazon Route 53** for domain management.  

Whenever new code is pushed to the GitHub repository, CodePipeline automatically builds and deploys it to Elastic Beanstalk. The application is accessible through a custom domain configured in Route 53.


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
  
4. **Amazon Route 53** 
   - Provides custom domain name mapping to the Beanstalk environment. 

---

## ⚙️ Technologies Used

-**AWS Elastic Beanstalk** – Application hosting & scaling  
- **AWS CodePipeline** – Continuous integration & deployment (CI/CD)  
- **GitHub** – Source code repository & version control  
- **Amazon Route 53** – Domain name system (DNS) management    

---

## 🚀 How It Works

1. **Code Push to GitHub**  
   - Developer commits and pushes changes to the GitHub repository.  

2. **CodePipeline Triggers**  
   - AWS CodePipeline detects the new commit via the GitHub connection.  
   - Pipeline automatically starts the deployment process.   

3. **Deployment to Elastic Beanstalk**  
   - Elastic Beanstalk deploys the latest build to the environment.  
   - The application is now live and automatically scaled based on traffic.  

4. **Route 53 Domain Mapping**  
   - A custom domain managed by Amazon Route 53 points to the Elastic Beanstalk environment.  
   - Users can access the app directly through `https://yourdomain.com`.  

**Flow Summary:**  
`GitHub (source code) ➝ CodePipeline (CI/CD) ➝ Elastic Beanstalk (hosting) ➝ Route 53 (custom domain)`  
 
---

## 🔑 Key Benefits

1. **Automated Deployments**
    – No manual intervention needed; every GitHub push is deployed automatically.  
2. **Scalability**
    – Elastic Beanstalk automatically handles scaling based on application load.  
3. **Custom Domain Integration**
    – Route 53 provides a professional, easy-to-remember domain name.  
4. **Reduced Downtime**
    – Blue/Green or Rolling updates in Beanstalk minimize downtime during deployments.  
5. **Centralized Pipeline**
    – CodePipeline provides a single place to manage CI/CD.  
6. **Cost-Effective**
    – Pay only for the AWS resources you use, with built-in monitoring and logging.  
7. **Flexibility**
    – Works with multiple programming languages (Node.js, Java, Python, PHP, etc.).  
8. **Secure**
    – Integrated with AWS IAM for fine-grained access control and GitHub connection security.  
 

---

## 📝 Future Enhancements

- Add automated testing before deployments  
- Enable notifications (Slack/Email) for pipeline events  
- Add monitoring with AWS CloudWatch  


