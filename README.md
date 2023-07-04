# Project X-Men Deployment Script (GitHub)

This repository contains a deployment script for Project X-Men, which automates the installation and configuration of the necessary components on an Amazon Linux EC2 instance to run the project.

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

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions to this project are welcome. If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

## Contact

For any inquiries or further information, please contact the project team at projectxmen@example.com.

---

Feel free to customize the README file according to your needs. Remember to update the contact information, license details, and any additional sections you deem necessary.
