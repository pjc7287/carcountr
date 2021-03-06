# Car Countr

An online cloud system to view traffic livestreams and provide insights on the number of cars over time
  
## Team

- Frank Agnello 
- Peter Carter

## Prerequisites

- Terraform
- AWS CLI

## How to deploy it 

Configuration:
1. Update variables in vars.tf (ACCOUNT_ID to your AWS Account ID and FRONTEND/BACKEND_BUCKET_NAME variables to unique S3 bucket names)
2. run 'aws configure' to set your ./aws/credentials file to your AWS Free Tier credentials

Deployment: 

1. terraform init
2. terraform plan -out "final"
3. terraform apply "final"

## Known bugs and disclaimers
AWS Requires each bucket to have a unique name, if your bucket name already exists on AWS some errors may occur.
This is made for AWS Free Tier, not Academy. Some issues may come up if running in an Academy account.

## How to test/run/access/use it

1. Open in your browser and navigate to the frontend URL given in the terraform output
2. Find a **m3u8** stream link that includes cars (e.g: https://s53.nysdot.skyvdn.com/rtplive/R4_090/playlist.m3u8)
3. Click "Add Camera" to supply a stream name and related link
4. Wait until data comes in, by default cameras are polled every 10 minutes


## License

MIT License

See LICENSE for details.
