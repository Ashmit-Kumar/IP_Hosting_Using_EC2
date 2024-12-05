# Step 2: Launch EC2 Instance

Now, we will launch an EC2 instance that will act as the server for our static website.

## Steps:

1. **Go to the EC2 Console**:
   - Navigate to the [EC2 Console](https://console.aws.amazon.com/ec2/).

2. **Launch Instance**:
   - Click **Launch Instance** and choose **Amazon Linux 2 AMI**.
   - Select an instance type (e.g., `t2.micro` for testing purposes).
   - Configure instance settings (you can leave default settings for testing).
   - **Security Groups**: Ensure that you allow:
     - **SSH (port 22)** for remote access.
     - **HTTP (port 80)** for web traffic.

3. **Key Pair**:
   - Select or create a new key pair to SSH into the instance.

4. **Launch the Instance**:
   - Review your settings and click **Launch**.

5. **Attach IAM Role**:
   - After launching, attach the IAM role (`EC2-S3-Access-Role`) created in Step 1.

Once the instance is running, note the public IP of the EC2 instance for later use.
