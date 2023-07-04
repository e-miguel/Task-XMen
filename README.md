# Project X-Men Deployment Script (Amazon S3)

This repository contains a deployment script for Project X-Men, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project. The web files are downloaded from Amazon S3.

## Prerequisites

Before running the script, make sure you have the following prerequisites in place:

- An Amazon Linux EC2 instance
- Administrative access to the EC2 instance
- AWS CLI configured with appropriate credentials

## Getting Started

To use this deployment script, follow these steps:

1. Clone this repository to your local machine or directly download the script file.
2. Connect to your Amazon Linux EC2 instance using SSH or any other preferred method.
3. Copy the script file (`deploy.sh`) to your EC2 instance.
4. Open a terminal or SSH session on the EC2 instance and navigate to the location where you copied the script.
5. Make the script executable by running the following command:
   ```
   chmod +x deploy.sh
   ```
6. Execute the script with root privileges using the following command:
   ```
   sudo ./deploy.sh
   ```

The script will perform the following actions:

1. Update the system packages using `yum`.
2. Install the Apache HTTP server (`httpd`) using `yum`.
3. Change the directory to `/var/www/html`.
4. Synchronize the contents of the S3 bucket `project-xmen` with the local directory `/var/www/html` using the AWS CLI `aws s3 sync` command.
5. Unzip the `xmen-main.zip` file.
6. Copy the contents of the `xmen-main` directory to `/var/www/html`.
7. Remove the `xmen-main.zip` file and the `xmen-main` directory.
8. Enable the `httpd` service to start automatically on system boot using `systemctl`.
9. Start the `httpd` service.

# X-Men Deployment Script (GitHub)

This repository contains a deployment script for the X-Men project, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project. The web files are downloaded from GitHub.

## Prerequisites

Before running the script, make sure you have the following prerequisites in place:

- An Amazon Linux EC2 instance
- Administrative access to the EC2 instance

## Getting Started

To use this deployment script, follow these steps:

1. Clone this repository to your local machine or directly download the script file.
2. Connect to your Amazon Linux EC2 instance using SSH or any other preferred method.
3. Copy the script file (`deploy.sh`) to your EC2 instance.
4. Open a terminal or SSH session on the EC2 instance and navigate to the location where you copied the script.
5. Make the script executable by running the following command:
   ```
   chmod +x deploy.sh
   ```
6. Execute the script with root privileges using the following command:
   ```
   sudo ./deploy.sh
   ```

The script will perform the following actions:

1. Update the system packages using `yum`.
2. Install the Apache HTTP server (`httpd`) using `yum`.
3. Change the directory to `/var/www/html`.
4. Download the `main.zip` file from the GitHub repository [e-miguel/xmen](https://github.com/e-miguel/xmen).
5. Unzip the `main.zip` file.
6. Unzip the `xmen-main.zip` file.
7. Copy the contents of the `xmen-main` directory to `/var/www/html`.
8. Remove the `xmen-main.zip` file and the `xmen-main` directory.
9. Enable the `httpd` service to start automatically on system boot using `systemctl`.
10. Start the `httpd` service.

# X-Men Deployment Script

This repository contains a deployment script for the X-Men project, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project.

## Prerequisites

Before running the script, make sure you have the following prerequisites in place:

- An Amazon Linux EC2 instance
- Administrative access to the EC2 instance

## Getting Started

To use this deployment script, follow these steps:

1. Clone this repository to your local machine or directly download the script file.
2. Connect to your Amazon Linux EC2 instance using SSH or any other preferred method.
3. Copy the script file (`deploy.sh`) to your EC2 instance.
4. Open a terminal or SSH session on the EC2 instance and navigate to the location where you copied the script.
5. Make the script executable by running the following command:
   ```
   chmod +x deploy.sh
   ```
6. Execute the script with root privileges using the following command:
   ```
   sudo ./deploy.sh
   ```

The script will perform the following actions:

1. Update the system packages using `yum`.
2. Install the Apache HTTP server (`httpd`) using `yum`.
3. Change the directory to `/var/www/html`.
4. Download the `main.zip` file from the GitHub repository [e-miguel/xmen](https://github.com/e-miguel/xmen).
5. Unzip the `main.zip` file.
6. Unzip the `xmen-main.zip` file.
7. Copy the contents of the `xmen-main` directory to `/var/www/html`.
8. Remove the `xmen-main.zip` file and the `xmen-main` directory.
9. Enable the `httpd` service to start automatically on system boot using `systemctl`.
10. Start the `httpd` service.

## Contact

For any inquiries or further information, please reach me at e32cloud@gmail.com
