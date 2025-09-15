⚙️ Setup Steps
=
1. Prepare Your Application

2.Add your application code to this repository.

  Ensure dependencies are listed (requirements.txt, package.json, or build file depending on language).
3. Create Elastic Beanstalk Environment


 -In the AWS Management Console, go to Elastic Beanstalk.

  Create a new application and environment (Web-deploy-env).
 Select the correct platform (Node.js, Python, Java, etc.).
 Note the Web-deploy and Web-deploy-env
 <img width="1917" height="920" alt="image" src="https://github.com/user-attachments/assets/c46033d8-c30d-4640-94ea-183d90e4cea7" />
<img width="1903" height="969" alt="Screenshot 2025-09-15 120014" src="https://github.com/user-attachments/assets/cb6db092-739f-4129-8660-88c1b514a73a" />

3. Configure IAM Role
=

Open **IAM Role ** in the console.
Create Role (Elastic Benstalk Role).
Add policies in the Role. 
<img width="1907" height="913" alt="image" src="https://github.com/user-attachments/assets/8e4a22cd-06ef-4aaf-9257-31213a359a79" />

4. Configure CodePipeline
=

Open AWS CodePipeline in the console.
Create connection to github.
Create a new pipeline and give it a name.
Source Stage: Choose GitHub and connect to this repository.
Build Stage (Optional): You can add a build step with AWS CodeBuild if your app needs compiling or testing.
Deploy Stage: Choose Elastic Beanstalk and select your application and environment.
Save and create the pipeline.

