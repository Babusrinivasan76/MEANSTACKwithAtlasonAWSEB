
# Application modernization with MongoDB Atlas and AWS Elastic Beanstalk

## Introduction: 
This is a technical repo to demonstrate the application deployment using MongoDB Atlas and AWS Elastic Beanstalk.
This tuotorial is intended for those who wants to
1. Have a rapid application deployment
2. Test out the features of an application
3. Fail fast in their development cycle
4. Want to try out the AWS Elastic Beanstalk and MongoDB Atlas 

## [MongoDB Atlas](https://www.mongodb.com/atlas) 
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
         
**Step2: Set up the EB CLI ** 

Set up the EB Cli based on the your environment using the [link](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html#eb-cli3-install.scripts)


  
**Step3: Set up the AWS Elastic Beanstalk environment**
 
 
 a. Git Clone the code from Repo   
        
 b. Select database parameters in .env file
  
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBSMeanstackupdatedbs-2.png) 
 
  
 c. Set up the Elastic Beanstalk initialization paramters
 
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp10.png)
 
        
 d. Create the environment with 'eb create'.
 
 Point for attention: Provide the "Application Name" same af the one defined in the Private URL in the code (employee.services.ts).
 
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp17.png)
 
 
 e. Ensure the successful creation of environment.
 
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp16.png)
 
        
 f. Update the configuration parameters for Loadbalancer / listeners
 
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp14.png)
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp15.png)
 
 
 g. Ensure the configuration changes are applied successfully
 ![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBcreateasampleapp15.png)


**Step4: Test the application**

 i. Using the endpoint created by EBS , test the application by adding the proper node (ie /api/v1/health)

![](https://github.com/Babusrinivasan76/ebintegrationwithatlas/blob/main/images/16.EBSMeanstackOutput-1.png)

## Summary:

 Any contanirized application can be deployed within no time using this template. 
 Instead of ebsdemoapp.zip , you can use your application zip file and deploy the application.
 Pls share your feedback / queries to partners@mongodb.com
 
