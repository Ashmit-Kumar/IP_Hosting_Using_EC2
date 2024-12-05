
---

#### **`docs/4-download-files-from-s3.md`**

```markdown
# Step 4: Download Files from S3

Next, we'll download the static files from our S3 bucket to the EC2 instance.

## Steps:

1. **Install AWS CLI** (if not already installed):
   - On the EC2 instance, install the AWS CLI:
     ```bash
     sudo yum install aws-cli -y
     ```

2. **Sync Files from S3 to EC2**:
   - Run the following command to sync files from your S3 bucket to the EC2 instance:
     ```bash
     aws s3 sync s3://your-bucket-name/ /var/www/html/
     ```

   This will download all files from the S3 bucket into the web server's root directory (`/var/www/html/` for Apache).

3. **Set Proper Permissions**:
   - Ensure the files have the correct permissions:
     ```bash
     sudo chown -R ec2-user:ec2-user /var/www/html/
     sudo chmod -R 755 /var/www/html/
     ```

Now, your files are ready to be served by the web server.
