## Step 1: Verify installation: 
aws --version

## Step 2: Configure AWS CLI: 
aws configure

## Step 3: Login with Access key: 
AWS Access Key ID [None]: AKIAUXXXXXXXXXXXXXXXX
AWS Secret Access Key [None]: r9hwLuvUJiRoWkhIc8B/WVtyLohtBxxxxxxxxxxx
Default region name [None]: eu-north-1
Default output format [None]: json

## Step 4: Create S3 bucket
aws s3 mb s3://my-bucket-alausa-2025 --region eu-north-1

## Step 5 Create a folder in the S3 bucket
aws s3api put-object --bucket my-bucket-alausa-2025 --key alausa-folder/

## Step 6 Verify the contents of the folder
aws s3 ls s3://my-bucket-alausa-2025/alausa-folder/

## Step 7 Upload Files into the Bucket
aws s3 cp "/c/Users/USER/Desktop/CLOUD ENGINEERING/Curriculum/Curriculum 3.jpg" s3://my-bucket-alausa-2025/alausa-folder/
aws s3 cp "/c/Users/USER/Desktop/CLOUD ENGINEERING/Curriculum/Curriculum 4.jpg" s3://my-bucket-alausa-2025/alausa-folder/
aws s3 cp "/c/Users/USER/Desktop/CLOUD ENGINEERING/Curriculum/Curriculum 5.jpg" s3://my-bucket-alausa-2025/alausa-folder/

## Step 8 Download the files from the Bucket
aws s3 cp s3://my-bucket-alausa-2025/alausa-folder/Curriculum\ 3.jpg "/c/Users/USER/Desktop/"
aws s3 cp "s3://my-bucket-alausa-2025/alausa-folder/Curriculum 4.jpg" "/c/Users/USER/Desktop/"
aws s3 cp "s3://my-bucket-alausa-2025/alausa-folder/Curriculum 5.jpg" "/c/Users/USER/Desktop/CLOUD ENGINEERING/Curriculum/"
aws s3 cp s3://my-bucket-alausa-2025/alausa-folder/ "/c/Users/USER/Desktop/Downloaded-from-S3/" --recursive (Download all)

## Step 9 Delete the files from S3 Bucket
aws s3 rm s3://my-bucket-alausa-2025/alausa-folder/Curriculum\ 3.jpg
aws s3 rm s3://my-bucket-alausa-2025/alausa-folder/ --recursive (Delete all)

## Step 10 Delete the Folder from S3 Bucket
aws s3 rm s3://my-bucket-alausa-2025/alausa-folder/ --recursive


## Step 11 Delete the S3 Bucket
aws s3 rb s3://my-bucket-alausa-2025 --force







