![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Create IAM Access Keys & Configure AWS CLI

## Introduction

In this hands-on lab, you will generate **access keys** for an IAM user, install the **AWS CLI**, and configure it using the generated access keys.

## **Pre-Requisites**

- A valid **AWS account** (free-trial or pay-as-you-go subscription).
- Access to the **AWS Management Console**.
- **Administrator privileges** to create IAM users and access keys.

## Lab Instructions

### **Step 1: Log in to AWS Console**
1. Open a web browser and navigate to [AWS Console](https://aws.amazon.com/console/).
2. Enter your **AWS credentials** and log in.

### **Step 2: Create an IAM User**
1. In the AWS Console, search for **IAM** and select the service.
2. In the **left pane**, click on **Users**.
3. Click **Create User**.
4. Enter the following details:
   - **User name**: `user1`
   - **Enable AWS Management Console access** (check the box).
   - **Set a custom password** or generate a new one.
5. Click **Next**, keeping all default settings.
6. Click **Create User**.
7. **Download the .csv file** with login credentials.

### **Step 3: Generate IAM Access Keys**
1. In the **IAM service**, select the newly created user (`user1`).
2. Navigate to the **Security Credentials** tab.
3. Scroll down to **Access Keys** and click **Create Access Key**.
4. Choose **Command Line Interface (CLI)** as the use case and click **Next**.
5. Click **Create Access Key**.
6. Download the **.csv file** containing the **Access Key ID** and **Secret Access Key**.

### **Step 4: Install AWS CLI**
#### **Check if AWS CLI is Installed**
- Open a terminal or command prompt and run:
  ```bash
  aws --version
  ```
- If AWS CLI is installed, the version number will be displayed.

#### **Install AWS CLI**
**Windows:**
1. Download the **AWS CLI installer** from [AWS Official Site](https://aws.amazon.com/cli/).
2. Run the installer and follow the on-screen instructions.
3. Verify installation with:
   ```bash
   aws --version
   ```

**macOS:**
1. Install AWS CLI using Homebrew:
   ```bash
   brew install awscli
   ```
2. Verify installation:
   ```bash
   aws --version
   ```

**Linux:**
1. Install AWS CLI using the package manager for your distribution:
   ```bash
   sudo apt install awscli  # Debian/Ubuntu
   sudo yum install awscli  # RHEL/CentOS
   ```
2. Verify installation:
   ```bash
   aws --version
   ```

### **Step 5: Configure AWS CLI ⚙️**
1. Open a terminal or command prompt.
2. Run the following command:
   ```bash
   aws configure
   ```
3. Enter the credentials downloaded earlier:
   - **Access Key ID**: (Paste from `.csv` file)
   - **Secret Access Key**: (Paste from `.csv` file)
   - **Default region**: (e.g., `us-east-1` or `eu-west-1`)
   - **Default output format**: (`json`, `table`, or `text`)

### **Step 6: Verify AWS CLI Configuration**
1. Run the following command to list all S3 buckets:
   ```bash
   aws s3 ls
   ```
2. If correctly configured, the command should return a list of available S3 buckets (or an empty response if none exist).

## Submission Guidelines

To complete this lab:

1. Take **screenshots** of:
   - IAM User creation.
   - Access Key generation.
   - AWS CLI installation.
   - AWS CLI configuration process.
   - Successful execution of `aws s3 ls`.
2. Paste the screenshots into a **Google Doc**.
3. Upload the document to **Google Drive**.
4. Share the **Google Drive link** with your instructor.

This lab provides **practical experience** in configuring AWS CLI and securely managing IAM credentials, ensuring controlled access to AWS services.

