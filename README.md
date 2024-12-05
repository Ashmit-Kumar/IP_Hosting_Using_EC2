# EC2 S3 Hosting with IAM Role

This project documents how to host a static website using an **EC2 instance** with an **IAM role** for S3 access and an **S3 bucket** for storing static files.

## Overview

In this guide, you'll learn how to:
1. Create an IAM role for your EC2 instance with access to your S3 bucket.
2. Launch an EC2 instance (Amazon Linux 2).
3. Install a web server (Apache or Nginx) on the EC2 instance.
4. Set up the EC2 instance to download static files from your S3 bucket.
5. Serve these files using the web server.
6. Test and ensure the website is publicly accessible.

This project assumes basic knowledge of AWS services like EC2, IAM, and S3. You should also have a static website stored in an S3 bucket.

## Documentation

Detailed steps for each part of the process are available in the `docs/` folder.

- **[Step 1: Set Up IAM Role for S3 Access](docs/1-setup-iam-role.md)**
- **[Step 2: Launch EC2 Instance](docs/2-launch-ec2-instance.md)**
- **[Step 3: Install Apache/Nginx Web Server](docs/3-install-web-server.md)**
- **[Step 4: Download Files from S3](docs/4-download-files-from-s3.md)**
- **[Step 5: Configure Web Server to Serve Files](docs/5-configure-web-server.md)**
- **[Step 6: Test the Website](docs/6-test-website.md)**

## Conclusion

By following these steps, you'll have a fully functional static website hosted from an EC2 instance with content pulled from an S3 bucket using IAM roles for secure access.
