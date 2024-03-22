## Hosting an HTML Website on an EC2 Instance



In this task, challenge your learning in hosting an HTML website on an EC2 instance and AWS services. This repository contains a deployment script for Task X-Men, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project.

### Requirements

Before doing the Task, please make sure you have the following prerequisites in place:

- Complete my previous industry projects and task to build your knowledge, skills, and troubleshooting.
- Administrative access to the EC2 instance
- AWS CLI configured with appropriate credentials

### Reference Architecture

![Task 2 - Project X-Men - AOS](https://github.com/e-miguel/Task-XMen/assets/134418850/3e573390-6cc1-461f-8f30-6a32a058729f)

### Task

1. Deploy the provided HTML website on an EC2 instance using the attached reference architecture.
2. Implement all the services mentioned in the reference architecture to ensure successful deployment.
3. Utilize a launch template to create auto scaling groups for efficient resource management.
4. Ensure that the website is accessible using your own domain name.
5. Ensure secure communication to the site by enabling HTTPS.
6. Store the web files in either your S3 bucket or GitHub repository. Your deployment script should be able to download the files from the chosen location. **Avoid using my script.**
7. Publish your completed task on your preferred online publsihing platform such as Git Hub or Medium.

### Deployment Script

- #!/bin/bash
- yum update -y
- yum install -y httpd
- cd /var/www/html
- wget https://github.com/e-miguel/Task-XMen/raw/main/xmen-main.zip
- unzip xmen-main.zip
- cp -r /var/www/html/xmen-main/* /var/www/html
- rm -rf xmen-main.zip xmen-main
- systemctl enable httpd
- systemctl start httpd

### Acceptance Criteria

1. Provide a screenshot of the deployed site, demonstrating that it is fully secured with HTTPS.
2. Include the URL of the deployed site in your online publishing platform.
3. Share the deployment script that you used for hosting the site.

### HTML Website

This is the HTML website deployed on an EC2 instance using the attached reference architecture. I implemented all the resources outlined in the task and reference architecture.

![image](https://github.com/e-miguel/Task-XMen/assets/134418850/3e72a9d3-959b-4cba-8681-82ed8a1823fe)

![image](https://github.com/e-miguel/Task-XMen/assets/134418850/7895a728-2192-4cc2-b884-13fb9e43053d)

### Resources

Some of the resources I utilized during the deployment of the web site such as EC2 Instance, Application Load Balancer, Auto Scaling Group, Launch Template, and more.

![image](https://github.com/e-miguel/Task-XMen/assets/134418850/f08de90b-291b-4855-849d-d775219703a6)

![image](https://github.com/e-miguel/Task-XMen/assets/134418850/def43c36-ce4e-4ff9-bf6d-b01d27459c07)

![image](https://github.com/e-miguel/Task-XMen/assets/134418850/cdce5f5c-fd64-4c3d-9740-64e989c25c57)

### Conlusions

Congratulations for successfully completing this industry task! Stay tuned for more Cloud Engineering and DevOps tutorial. Contributions to this project are welcome. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

---
