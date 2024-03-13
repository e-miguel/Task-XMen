# Hosting an HTML Website on an EC2 Instance



In this task, challenge your learning in hosting an HTML website on an EC2 instance and AWS services. This repository contains a deployment script for Task X-Men, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project.

## Prerequisite

Before running the script, make sure you have the following prerequisites in place:

- Complete my previous industry projects and task to build your knowledge, skills, and troubleshooting.
- Administrative access to the EC2 instance
- AWS CLI configured with appropriate credentials

# Reference Architecture

![Task 2 - Project X-Men - AOS](https://github.com/e-miguel/Task-XMen/assets/134418850/f2efc3fe-4c55-470f-a0ca-f292bd81e06a)

## Task

1. Deploy the provided HTML website on an EC2 instance using the attached reference architecture.

## Summary of Scripts

- #!/bin/bash
- sudo su
- yum update -y
- yum install -y httpd
- cd /var/www/html
- aws s3 sync s3://project-xmen /var/www/html
- unzip xmen-main.zip
- cp -r /var/www/html/xmen-main/* /var/www/html
- rm -rf xmen-main.zip xmen-main
- systemctl enable httpd 
- systemctl start httpd

## Contributing

Contributions to this project are welcome. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

## Contact

For any inquiries or further information, please contact me at e32cloud@gmail.com.

---
