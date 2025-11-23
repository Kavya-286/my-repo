# Dynamic Data Table Manager

A dynamic and customizable data table application built using **Next.js**, **Redux Toolkit**, and **Material UI (MUI)**.  
This project allows users to manage table data with features like sorting, searching, pagination, dynamic column visibility, and CSV import/export.

---

## 🚀 Features

### ✅ Core Features
- Display table with default fields: **Name, Email, Age, Role**
- **Sorting** on each column (ASC/DESC toggle)
- **Global search** across all fields
- **Client-side pagination** (10 rows per page)

### 🧩 Dynamic Columns
- “Manage Columns” modal to:
  - Add new fields dynamically (e.g., Department, Location)
  - Show / hide existing columns via checkboxes
- Column visibility is **persisted** using localStorage / Redux Persist

### 📥 CSV Import & 📤 Export
- Import CSV using **PapaParse**
- Validate format and show error feedback
- Export current table view as `.csv`
- Only visible columns are included in the export

---
JENKINS PIPELINE SCRIPT

pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'
    }
    stages {
        stage('Clone Repo & Clean') {
            steps {
                bat "git clone https://github.com/Kavya-286/web-app"
                bat "mvn -f web-app/pom.xml clean"
            }
        }
        stage('Install') {
            steps {
                bat "mvn -f web-app/pom.xml install"
            }
        }
        stage('Test') {
            steps {
                bat "mvn -f web-app/pom.xml test"
            }
        }
        stage('Package') {
            steps {
                bat "mvn -f web-app/pom.xml package"
            }
        }
    }
}

============================================
minikube commands :
minikube start --driver=hyperv

minikube start --driver=docker

minikube status

minikube kubectl -- get pods -A
minikube dashboard
Minikube version
kubectl version –client
minikube logs
minikube update-check
minikube update

Minikube Automation Steps
Step 1: Start Minikube Cluster
Open your terminal and run the command:
minikube start

Step 2: Create and Manage Deployment
Create  an application in Kubernetes:

Command:
kubectl create deployment mynginx --image=nginx
kubectl set image deployment/myngnix nginx=nginx:latest
kubectl get deployments
kubectl get pods
kubectl describe pods
kubectl expose deployment mynginx --type=NodePort --port=80 --target-port=80

Step 3: Scale the Deployment
Command:Scales the Nginx deployment to 4 replicas (pods).
kubectl scale deployment mynginx --replicas=4
kubectl get service mynginx

Step 4: Access the Nginx App
Using Port Forwarding:
Command:
kubectl port-forward svc/mynginx 8081:80
Access the app via http://localhost:8081.
If Error, use this option, Using Minikube Tunnel:
Start the tunnel:
command: minikube tunnel
etrieve the service URL:
command:minikube service mynginx --url
Open the provided URL in your browser.
Open the kubernets dashboard
Open the minikube dashboard	
command : Minikube dashboard

kubectl delete deployment mynginx
kubectl delete service mynginx

Nagios Automation Steps
Step 1: Pull the Nagios Docker Image
Open a terminal and run:
docker pull jasonrivers/nagios:latest

Step 2: Run Nagios
Command:
docker run --name nagiosdemo -p 8888:80 jasonrivers/nagios:latest

Step 3: Access Nagios Dashboard
Open your browser and navigate to:
http://localhost:8888
Login Credentials:
Username: nagiosadmin
Password: nagios

to Delete the Container:
Command:
docker rm nagiosdemo

to Delete the Nagios image:
docker rmijasonrivers/nagios:latest

=======================================================================================

Setting Up  Jenkins CI------using GitHub Webhook with Jenkins 

Step 1: Configure Webhook in GitHub
Go to your GitHub repository
step 2:Navigate to Settings → Webhooks.
step 3:Click “Add webhook”.
step 4:In the Payload URL field:
Enter the Jenkins webhook URL in the format:
http://<jenkins-server-url>/github-webhook/
Note: If Jenkins is running on localhost, GitHub cannot access it directly.
Use ngrok to expose your local Jenkins to the internet:

ngrok.exe http <Jenkins local host:8080>
Use the generated ngrok URL, e.g.:
http://abc123.ngrok.io/github-webhook/
step 5:Set Content type to:
application/json
step 6:Under “Which events would you like to trigger this webhook?”, select:
 Just the push event
step 7:Click “Add webhook” to save.



 Step 2: Configure Jenkins to Accept GitHub Webhooks
1 Open Jenkins Dashboard.

2 Select the job (freestyle or pipeline) you’ve already created

3 Click Configure.

4 Scroll down to the Build Triggers section.

5 Check the box: ✅GitHub hook trigger for GITScm polling

6 Click Save.

Step 3: Test the Setup
1 Make any code update in your local repo and push it to GitHub

2 Once pushed, GitHub will trigger the webhook.
3 Jenkins will automatically detect the change and start the build pipeline


Setting Up   Jenkins Email Notification Setup (Using Gmail with App Password)
Creation of app password
1. Gmail: Enable App Password (for 2-Step Verification)
i. Go to: https://myaccount.google.com

ii. Enable 2-Step Verification
Navigate to:
Security → 2-Step Verification

Turn it ON
Complete the OTP verification process (via phone/email)

iii. Generate App Password for Jenkins
Go to:
Security → App passwords

Select:
App: Other (Custom name)
Name: Jenkins-Demo
Click Generate
Copy the 16-digit app password
Save it in a secure location (e.g., Notepad)

 2.  Jenkins Plugin Installation
i. Open Jenkins Dashboard
ii. Navigate to:
Manage Jenkins → Manage Plugins
iii. Install Plugin:
Search for and install:
Email Extension Plugin


3. Configure Jenkins Global Email Settings
i. Go to:
Manage Jenkins → Configure System

A. E-mail Notification Section
Field
Value
SMTP Server
smtp.gmail.com
Use SMTP Auth
✅ Enabled
User Name
Your Gmail ID (e.g., archanareddykmit@gmail.com)
Password
Paste the 16-digit App Password
Use SSL
✅ Enabled
SMTP Port
465
Reply-To Address
Your Gmail ID (same as above)
➤ Test Configuration
Click: Test configuration by sending test e-mail
Provide a valid email address to receive a test mail
✅ Should receive email from Jenkins

B. Extended E-mail Notification Section
Field
Value
SMTP Server
smtp.gmail.com
SMTP Port
465
Use SSL
✅ Enabled
Credentials
Add Gmail ID and App Password as Jenkins credentials
Default Content Type
text/html or leave default
Default Recipients
Leave empty or provide default emails
Triggers
Select as per needs (e.g., Failure)


4.  Configure Email Notifications for a Jenkins Job
i. Go to:
Jenkins → Select a Job → Configure

ii. In the Post-build Actions section:
Click: Add post-build action → Editable Email Notification
A. Fill in the fields:
Field
Value
Project Recipient List
Add recipient email addresses (comma-separated)
Content Type
Default (text/plain) or text/html
Triggers
Select events (e.g., Failure, Success, etc.)
Attachments
(Optional) Add logs, reports, etc.


iii. Click Save

 Now your Jenkins job is set up to send email notifications based on the build status!

==========================================================================================================================
AWS :::

 sudo apt update 
sudo apt-get install docker.io
 sudo apt install git
sudo apt install nano

 git clone <paste the github link of maven-web-java project>
 Step 4:-  nano Dockerfile 
 Step 1:- build your image 
	docker build –t <imagename> .(dot)
Step 2:- check for images
Step 3:- run image
	docker  run –d  --name app-demo –p 6060:8080 <image name> 

 then use public ip and paste in chrome
 
 
### 1. Clone Repository
```bash
git clone https://github.com/your-username/dynamic-data-table-manager.git
cd dynamic-data-table-manager
