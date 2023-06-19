# Correvate's Devops engineer test

# Overview

This project is based on automation of Docker image build and upload into DockerHub using declarative Jenkins pipeline

- Automating Jenkins instance creation and docker installation
- Automating Docker image creation
- Automating Docker container provisioning

You can configure pipeline in your Jenkins instance by creating a Declarative pipeline.

# Pre-requisites


1. Create scripted pipeline using Jenkinsfile from this repo
2. Install Maven & Docker Plugins 


# Steps

Create an EC2 instance, install Jenkins and Docker manually or using Terraform
Jenkins Configuration & plugins
Install Docker Plugins 
Create scripted pipeline using Jenkinsfile from this repo
Docker Image Build

# Automation Steps on Jenkins:
 
1. Login to Jenkins. Click on New item.
2. Enter an item name --> select Pipeline.
3. Create scripted pipeline using Jenkinsfile from this repo
4. Click on Build - Build the pipeline
5. Optional - Create webhook for automated code push



Use endpoint URL http://34.228.80.183:5601/app/kibana#/dashboard/ to access the page

