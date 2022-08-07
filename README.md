
# Application modernization with MongoDB Atlas and AWS Elastic Beanstalk

## Introduction: 
This is a technical repo to demonstrate the application deployment using MongoDB Atlas and AWS Elastic Beanstalk.
This tuotorial is intended for those who wants to
1. Have a rapid application deployment
2. Test out the features of an application
3. Fail fast in their development cycle
4. Want to try out the AWS Elastic Beanstalk and MongoDB Atlas 

## [MongoDB Atlas](https://www.mongodb.com/atlas) :
MongoDB Atlas is an all purpose database having features like Document Model, Geo-spatial , Time-seires, hybrid deployment, multi cloud services.
It evolved as "Developer Data Platform", intended to reduce the developers workload on development and management the database environment.
It also provide a free tier to test out the application / database features.


## [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)
AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

## Architecture Diagram:
![AWS EBS with MongoDB Atlas](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/EBS%20Atlas%20Architecture.png)

## Step by Step Deployment:

**Step1: Set up the MongoDB Atlas cluster**
         
   MongoDB Atlas provides a free cluster setup. Pls follow the link to setup the [free cluster](https://www.mongodb.com/docs/atlas/getting-started/)
         
**Step2: Download and containerize the application**        

  Download the sample application from this repository  - " [ebsDemoApp.zip](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/raw/main/ebsDemoApp.zip) ". 
         
  This application is having 3 APIs to register the user details to MongoDB Atlas(./app/v1/users) , to Query the user (./app/v1/login) and to check the health of the application (./app/v1/health)
         
  Change the .env parameters as per the MongoDB Database and collections you created in step1
         
  Change the database connection details in app.py
  
**Step3: Set up the AWS Elastic Beanstalk environment**
 
 
 a. Navigate to the AWS Elastic Beanstalk by typing "Elastic Beanstalk" in the search bar of AWS Console and click "Create a new Environment"
       
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/01.EBS-CreateEnv1-upd.png)     
        
 b. Select "Web Server Environment"
        
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/02.EBS-CreateEnv2-upd.png)
  
 c. Type the "Application Name" , "Environment Name" and "Domain". Validate the Domain availability
  
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/03.EBS-CreateEnv3-upd.png)
        
 d. Choose the platform details as the docker container
        
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/04.EBS-CreateEnv4-upd.png)
  
 e. Download the code - "ebsDemoApp.zip" and upload the same by clicking " Choose File". Provide a version details of the file
 
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/05.EBS-CreateEnv5-upd.png)
  
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/06.EBS-CreateEnv6-upd.png)
        
 f. Ensure the file is sucessfully upload and provide the tag details(optional)
 
 ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/07.EBS-CreateEnv7-upd.png)
 
 g. Click "Create Environment". It will take 15mins to complete.
 
![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/08.EBS-CreateEnv8-upd.png)

 h. Ensure the application is deployed successfuly. For any troubleshooting, use the logs from the left side menu.
        
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/13.EBS-CreateEnv13-upd.png)
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/14.EBS-CreateEnv14-upd.png)


**Step5: Test the application**

 i. Using the endpoint created by EBS , test the application by adding the proper node (ie /api/v1/health)
  ![](https://github.com/Babusrinivasan76/ebsintegrationwithatlas/blob/main/images/15.EBS-CreateEnv15-upd.png)


## Summary:

 Any contanirized application can be deployed within no time using this template. 
 Instead of ebsdemoapp.zip , you can use your application zip file and deploy the application.
 Pls share your feedback / queries to partners@mongodb.com
 
