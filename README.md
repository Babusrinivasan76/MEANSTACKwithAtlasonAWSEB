
# Application modernization with MongoDB Atlas and AWS Elastic Beanstalk

## Introduction: 
This is a technical repo to demonstrate the application deployment using MongoDB Atlas and AWS Elastic Beanstalk.
This tuotorial is intended for those who wants to
1. Have a rapid application deployment
2. Test out the features of an application
3. Fail fast in their development cycle
4. Want to try out the AWS Elastic Beanstalk and MongoDB Atlas 

## MongoDB Atlas:
MongoDB Atlas is an all purpose database having features like Document Model, Geo-spatial , Time-seires, hybrid deployment, multi cloud services.
It evolved as "Developer Data Platform", intended to reduce the developers workload on development and management the database environment.
It also provide a free tier to test out the application / database features.


## AWS Elastic Beanstalk:
AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

## Architecture Diagram:
![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/EBS%20Atlas%20Architecture.png)

## Step by Step Deployment:

**Step1: Set up the MongoDB Atlas cluster**
         MongoDB Atlas provides a free cluster setup. Pls follow the link to setup the free cluster
         
**Step2: Develop and containerize the application**         
  
**Step3: Set up the AWS Elastic Beanstalk environment**
        a. Navigate to the AWS Elastic Beanstalk
        ![AWS Console - Elastic Beanstalk]([https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/01.EBS%20-%20Create%20Env.png)
        b. Create a Web Server Environment
        ![EBS - Environment Creation1](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/02.EBS%20-%20Create%20Env%202.png)
        ![EBS - Environment Creation2](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/03.EBS-%20CCreate%20CEnv3.png)
        c. Choose the application to deploy 
        ![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/04.EBS%20-%20Create%20Env4.png)
        ![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/04.EBS%20-%20Create%20Env6.png)
        ![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/04.EBS%20-%20Create%20Env7.png)
        d. Troubleshoot
        ![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/14.EBS%20-%20Logs.png)

**Step4: Deploy the application**

**Step5: Test the application**

## Summary:

