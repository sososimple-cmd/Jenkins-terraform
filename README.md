# Jenkins Terraform Project

## Overview
This project deploys a Jenkins server using Terraform on AWS. It includes:
- EC2 instance with Jenkins installed
- Security group allowing SSH and Jenkins access
- S3 bucket for Jenkins artifacts

## Setup Instructions
1. **Terraform Configuration**
   - Ensure you have Terraform installed.
   - Run:
     ```bash
     terraform init
     terraform apply
     ```

2. **SSH into EC2 Instance**
   - Use the `.pem` key file to SSH into the EC2 instance:
     ```bash
     ssh -i yourkey.pem ubuntu@<your-public-ip>
     ```

3. **Retrieve Jenkins Password**
   - Once logged in, run:
     ```bash
     sudo cat /var/lib/jenkins/secrets/initialAdminPassword
     ```

4. **Unlock Jenkins**
   - Open Jenkins in your browser:
     ```
     http://<your-public-ip>:8080
     ```
   - Paste the password and click **Continue**.

5. **Customize Jenkins**
   - Install suggested plugins.
   - Create an admin user.

## Screenshots
<img width="1645" height="738" alt="Jenkins screenshot" src="https://github.com/user-attachments/assets/c1c1f7dd-5e4d-4396-be59-8269a5c16d76" />







## Resources
- [Terraform Documentation](https://www.terraform.io/docs)
- [Jenkins Installation Guide](https://www.jenkins.io/doc/book/installing/linux/)
- [AWS Provider Reference](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)


