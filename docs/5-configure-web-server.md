# Step 5: Configure Web Server to Serve Files

After downloading the static files, let's configure the web server to serve them.

## Steps:

1. **Verify Files in the Web Directory**:
   - Make sure your files are in the correct directory:
     ```bash
     ls /var/www/html/
     ```

2. **Check Apache/Nginx Configuration**:
   - If you're using **Apache**, ensure the configuration is set to serve files from `/var/www/html/`.
   - If you're using **Nginx**, the default directory should be `/usr/share/nginx/html/`, so update the Nginx config if necessary.

3. **Restart Web Server**:
   - Restart the web server to apply any changes:
     ```bash
     sudo systemctl restart httpd  # For Apache
     sudo systemctl restart nginx  # For Nginx
     ```

Your web server is now configured to serve static content from your S3 bucket.
