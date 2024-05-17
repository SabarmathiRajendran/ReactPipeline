# Creating CI Pipeline for React App and Host it using Amazon S3  


Step 1: Create ReactApp    


Step 2: Push ReactApp using Git into Github Repo "https://github.com/SabarmathiRajendran/ReactPipeline"  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/0744dad1-c158-47d7-8352-b73d13d93475)  


Step 3: Create IAM User in AWS. Set two Policies for the User [AmazonS3FullAccess & IAMUserChangePassword]  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/d348a736-5409-43e4-8f16-2d02cd20beb7)  


Step 4: Create an Access key from the security credential section of the newly created user  

Make sure you downloaded the .csv file or note the data some where else, Because we can see it only once.  


Step 5: Create an S3 bucket  

Give a name to the bucket and enable ACLs.  

Untick Block all public access and tick the warning after reading it.  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/c81a1535-2914-45fd-b37b-031317fb8730)  

After this hit create bucket button and you are done with creating a new user and storage.  


Step 6: Go to the settings of your repo and select the secrets from the left section. Add three Secret keys with corresponding Access Key values.  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/3aea10ac-3715-4006-8883-d4e7e116855c)  


Step 7: Add .yaml file in .github/workflows. Go to the Action section and see the process  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/64be8713-96b0-40d5-943b-deabe8004f97)  


Step 8: Configure S3 for web hosting. You can see all uploaded files from GitHub here  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/09ffb190-63c7-452d-a181-88037a35f609)  

Now go to the Properties section and scroll down to the end. You can see the Static website hosting option. Click on edit and enable it and write index.html in the index document section. Then save changes.  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/df7ef6cd-8ad9-49ea-b1c5-03199b5412ae)  


Now you can see a link in the static website hosting section. Open it in a new tab.  

![image](https://github.com/SabarmathiRajendran/ReactPipeline/assets/143160828/b3ccffaf-6ccc-4f77-8c0a-e7df1551b723)  

