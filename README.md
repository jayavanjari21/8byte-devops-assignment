# 8byte-devops-assignment
8byte-devops-assignment

## Project Overview
This project demonstrates deploying a containerized Node.js application on AWS using Terraform and GitHub Actions.

## Tech Stack
- AWS EC2
- Terraform
- Docker
- GitHub Actions
- Node.js (Express)

## Architecture
Developer → GitHub → GitHub Actions → Docker Build  
Terraform → AWS EC2 → Docker Container → Public Access

## Run Locally
```bash
npm install
node app.js

## Docker
docker build -t 8byte-intern-app .
docker run -p 3000:3000 8byte-intern-app

## Terraform
terraform init
terraform plan
terraform apply

##Deployment
ssh ubuntu@<EC2_PUBLIC_IP>
docker run -d -p 3000:3000 8byte-intern-app
