#STEP1
Fork the sample php app from https://github.com/shreenu1995/ecs-demo-php-simple-app.git and generate the access key token in your github account.
#STEP2
Download the code/yml files from https://github.com/shreenu1995/ecs-refarch-continuous-deployment.
#STEP3
Create a S3 bucket and upload the code/yml file,which is downloaded from https://github.com/shreenu1995/ecs-refarch-continuous-deployment.
#STEP4
Now go to s3 and copy the object url for ecs-refarch-continuous-deployment.yml.
#STEP5
Create a cloudformation stack and give template source as s3 url,which we have copied from step4.Then give the parameters
*Cluster Configuration
Launch Type: Farget/EC2:
*GitHub Configuration:
Repo:
Branch:
User:
Personal Access Token:
*Stack Configuration
TemplateBucket:
And then create stack.It will automatically create VPC,ALB,Cluster,ASG,Service,Deployement pipline.



