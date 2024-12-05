# Step 3: Install Apache/Nginx Web Server

Now, let's install and configure a web server on the EC2 instance to serve the static content.

## Steps:

1. **SSH into EC2 Instance**:
   - Open a terminal and SSH into the EC2 instance using the following command:
     ```bash
     ssh -i /path/to/your-key.pem ec2-user@<your-ec2-public-ip>
     ```

2. **Install Apache Web Server** (for example):
   - Run the following command to install Apache:
     ```bash
     sudo yum install httpd -y
     ```

3. **Start and Enable Apache**:
   - Start the Apache web server:
     ```bash
     sudo systemctl start httpd
     ```
   - Enable Apache to start automatically on boot:
     ```bash
     sudo systemctl enable httpd
     ```

   Or, if you prefer **Nginx**, you can install it instead:
   ```bash
   sudo amazon-linux-extras install nginx1.12 -y
   sudo systemctl start nginx
   sudo systemctl enable nginx
