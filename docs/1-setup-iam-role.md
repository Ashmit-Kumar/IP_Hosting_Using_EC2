# Step 1: Set Up IAM Role for S3 Access

To allow the EC2 instance to read files from the S3 bucket, we need to create an IAM role with appropriate permissions and attach it to the EC2 instance.

## Steps:

1. **Go to the IAM Console**:
   - Navigate to the [IAM Console](https://console.aws.amazon.com/iam/).

2. **Create a New Role**:
   - Click on **Roles** in the sidebar, then click **Create role**.
   - Choose **AWS service** as the trusted entity type, then select **EC2**.
   - Click **Next: Permissions**.

3. **Attach S3 Permissions**:
   - In the search bar, type `AmazonS3ReadOnlyAccess` (for read-only access to your S3 bucket).
   - Select `AmazonS3ReadOnlyAccess`. You can also choose `AmazonS3FullAccess` if you need both read and write access to the S3 bucket.
   - Click **Next: Tags**.

4. **Name the Role**:
   - Provide a name for the role, e.g., `EC2-S3-Access-Role`.
   - Click **Create role**.

5. **Attach the Role to the EC2 Instance**:
   - Go to the **EC2 Console** and select your instance.
   - In the **Actions** dropdown, click **Security** > **Modify IAM role**.
   - Attach the IAM role you just created.

Your EC2 instance is now ready to access S3 using this role.
