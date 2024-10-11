<h1>Personal Portfolio Website Deployment </h1>
This repository contains the setup for deploying a personal Portfolio website using GitHub Actions for continuous deployment to AWS S3.
The site is automatically built and deployed whenever changes are pushed to the main branch, ensuring your portfolio is always live and up-to-date.
<br>
<h2>Table of Contents</h2>

  <ol>Overview</ol>
   <ol>Technologies Used</ol>
   <ol>Prerequisites</ol>
   <ol>AWS S3 Bucket Setup</ol>
   <ol>GitHub Actions Workflow</ol>
   <ol>Deployment</ol>
   <ol>Contributing</ol>
   <ol>License</ol>

<h2>Overview</h2>
This project demonstrates how to build and deploy a DevOps Portfolio website to AWS S3 using GitHub Actions. It automates the deployment process, ensuring your website stays live with the latest changes pushed to your GitHub repository.
The personal Portfolio highlights your skills, projects, certifications, and experience, hosted on AWS infrastructure for reliability and scalability.

<h2>Technologies Used</h2>
<ul><b>GitHub Actions: </b>Automates the deployment pipeline.</ul>
<ul><b>AWS S3: </b>Serves as the static website host for the portfolio.</ul>
<ul><b>AWS CLI:</b>Command-line interface used in automation for interacting with AWS services.</ul>
<ul><b>HTML/CSS/JavaScript: </b>Basic structure and styling of the portfolio.</ul>

<h2>Prerequisites</h2>
Before proceeding with the deployment, ensure the following are in place:
<ul><b>1.AWS Account: </b>You must have an AWS account to create and configure the S3 bucket.</ul>
<ul><b>2.GitHub Repository: </b>Your portfolio website code should be hosted in a GitHub repository.</ul>
<ul><b>3.IAM User with S3 Access:</b>Create an IAM user in AWS with appropriate permissions to access and upload to S3. Obtain the access key and secret key for this user.</ul>
<ul><b>4.S3 Bucket: </b>A dedicated S3 bucket to host your portfolio website.</ul>
<ul><b>5.Basic Knowledge of AWS S3 and GitHub Actions.</b></ul>

<h2>AWS S3 Bucket Setup</h2>
<h3>1. Create an S3 Bucket:</h3>
Go to AWS S3 and create a new bucket. Ensure the name is globally unique.
<h3>2.Enable Static Website Hosting:</h3>
In the bucket settings, enable static website hosting. Configure the index.html as the main entry point.
<h3>3.Bucket Permissions:</h3>
Modify the bucket policy to allow public access to your portfolio files (ensure you are aware of security best practices when enabling public access).
<h3>4.Set Up Permissions for Deployment:</h3>
Create an IAM policy allowing PutObject and GetObject access for your S3 bucket.

<h2>GitHub Actions Workflow</h2>
This repository uses GitHub Actions to automate the build and deployment process. The workflow is triggered whenever there is a push to the main branch. GitHub Actions will:

<ol>1.Build the website (if applicable)</ol>
<ol>2.Deploy the contents of the repository to the S3 bucket.</ol> 
You'll need to configure the AWS credentials (access and secret keys) as GitHub repository secrets to enable GitHub Actions to interact with your AWS environment.

<h2>Deployment</h2>
<ol><b>Push Changes:</b> Push your website updates to the main branch of your GitHub repository.</ol>
<ol><b>Automated Deployment: </b>GitHub Actions will trigger the deployment process, uploading your site files to the S3 bucket.</ol>
<ol><b>Access Your Website:</b> Once the deployment is complete, your portfolio will be live at the S3 bucket’s website URL.</ol>

<h2>Contributing</h2>
If you'd like to contribute to this project, feel free to submit a pull request or open an issue for suggestions. Contributions are welcome to help enhance the deployment process or improve the portfolio content.

<h2>License</h2>
This project is licensed under the MIT License. You are free to use, modify, and distribute the project, as long as you provide attribution.
