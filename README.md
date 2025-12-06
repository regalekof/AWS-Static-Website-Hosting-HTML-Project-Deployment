# Deploying a Static HTML Website on AWS S3 (Step-by-Step Guide)
This project demonstrates how to host a fully public static HTML website on Amazon Web Services (AWS) S3 using Static Website Hosting.
It is perfect for beginners learning cloud deployment, AWS fundamentals, or static web hosting.

🚀 Features

Deploy a static website using Amazon S3

Enable public access to website files

Configure Static Website Hosting

Upload and serve an HTML webpage

Generate a public website URL hosted on AWS

🧰 Prerequisites

Before you begin, you need:

An AWS account

A simple HTML file (example: index.html)

📝 Deployment Steps
Step 1: Log in to AWS Console

Visit aws.amazon.com

Sign in to your AWS account

In the search bar, type “S3”

Click on Amazon S3

Step 2: Create an S3 Bucket

Click Create bucket

Enter a unique bucket name
Example: cat-conspiracy-website

Choose a region (e.g., US East 1)

Scroll to Block Public Access settings

Uncheck Block all public access

Check the confirmation box

Click Create bucket

Step 3: Upload Your Website Files

Open the bucket you created

Click Upload

Click Add files (or drag & drop)

Select your index.html

Click Upload

Step 4: Enable Static Website Hosting

Go to the Properties tab

Scroll to Static website hosting

Click Edit

Choose Enable

Set:

Index document: index.html

Error document: index.html

Click Save changes

Step 5: Make Your Files Public

Go to the Permissions tab

Scroll to Bucket policy

Click Edit

Paste this policy (replace YOUR-BUCKET-NAME):

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}


Click Save changes

Step 6: Get Your Live Website URL

Go back to the Properties tab

Scroll down to Static website hosting

Copy your Bucket website endpoint link

🎉 Your HTML website is now live on AWS!

🌐 Example (Replace with Your Link)
http://cat-conspiracy-website.s3-website-us-east-1.amazonaws.com

📚 What You Learned

Creating an S3 bucket

Uploading and managing files

Configuring public access and bucket policies

Enabling static website hosting

Deploying a website using AWS infrastructure

📄 License

This project is open-source and free to use for learning and educational purposes.
