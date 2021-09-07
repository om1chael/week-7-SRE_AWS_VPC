# AWS S3
Amazon s3:

![image](https://www.freecodecamp.org/news/content/images/2020/08/Screenshot-2020-08-10-at-6.26.31-PM.png)

Amazon S3 or Amazon Simple Storage Service is a Services that provides object storage through a web service interface.
it makes the data presistant 




## Configure the AWS instance 
```
sudo apt-get update -y 
sudo apt-get upgrade -y
sudo apt-get install python -y
sudo apt-get install python3-pip -y
alias python=python3
```


python --version 
``` it should equal 3.5.2  ```
python3 -m pip install awscli

`aws configure `


input Key ID and AWS secret Access key from:
 - ``` excel file ```

location:
 - ``` eu-west-1 ```

defualt output format: 
 - `json`

![img](https://i.stack.imgur.com/D3eMF.png)

Final command find the files in the bucket:

- ` aws s3 ls  `

If eveything is valid, a list of folders will appear.
___
## Making a bucket 
     Underscores and special charaters are not allowed

``aws s3 ls``

``aws s3 mb s3://[bucket name]``


# CRUD: create, read, update, delete 

![img](https://www.dorusomcutean.com/wp-content/uploads/2020/03/crud.jpg)


## Copy

- aws s3 sync s3://[bucket name]
## Upload to Bucket
- aws s3 cp s3://[Bucket name] [file name]
## Upload from Bucket
- aws s3 mp [file name] s3://[bucket name]

## Delete bucket
- aws s3 rb s3://[bucket name]--force


# Install:
`pip3 install boto3`

To use Boto3, you must first import it and indicate which service or services you're going to use:

import boto3

### Let's use Amazon S3
s3 = boto3.resource('s3')

### Print out bucket names
```
for bucket in s3.buckets.all():
        print(bucket.name)
```
# Upload a new file
```
data = open('file.jpg', 'rb')
s3.Bucket('my-bucket').put_object(Key='file.jpg', Body=data)
```


- Create S3 bucket using python-boto3
- Upload data/file to S3 bucket using python-boto3
- Retrieve content/file from S3 using python-boto3
- Delete Content from S3 using python-boto3
- Delete the bucket using python-boto3.**