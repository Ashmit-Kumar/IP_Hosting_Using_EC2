# Step 6: Test the Website

Let's ensure the website is up and running.

## Steps:

1. **Access the Website**:
   - Open a browser and navigate to the EC2 instance's public IP:
     ```
     http://<your-ec2-public-ip>
     ```

2. **Troubleshooting**:
   - If the site doesn't load, ensure the following:
     - The web server is running (`systemctl status httpd` or `systemctl status nginx`).
     - The EC2 security group allows inbound traffic on port 80 (HTTP).
     - The permissions on `/var/www/html/` are correct.

Once the website is accessible, you're done!
