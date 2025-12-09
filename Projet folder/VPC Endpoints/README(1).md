<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Endpoints

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-endpoints)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

## VPC Endpoints

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_09bcaa8a)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a virtual private network inside AWS, and it is useful because it allows you to securely control and isolate your cloud resources.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create Endpoint etc.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was much scenario of troubleshooting.

### This project took me...

This project took me 1h.

---

## In the first part of my project...

### Step 1 - Architecture set up

In this step, I will create a VPC from scratch, launch an EC2 instance that I will later connect to using EC2 Instance Connect, and set up an S3 bucket.

### Step 2 - Connect to EC2 instance

In this step, I will Connect directly to your EC2 instance.

### Step 3 - Set up access keys

In this step, I will Give your EC2 instance access to your AWS environment.

### Step 4 - Interact with S3 bucket

In this step, I will Head back to your EC2 instance.
Get your EC2 instance to access your S3 bucket.

---

## Architecture set up

I started my project by launching EC2.


I also set up S3.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_4334d777)

---

## Access keys

### Credentials

To set up my EC2 instance to interact with my AWS environment, I configured Keys access etc..

Access keys are key-based credentials that allow a user or application to programmatically access AWS services through the AWS CLI, SDKs, or APIs.

The secret access key is like the password that pairs with your access key ID (your username). You need both to access AWS services.

### Best practice

Although I'm using access keys in this project, a best practice alternative is to use IAM roles with temporary security credentials.

---

## Connecting to my S3 bucket

The command I ran was aws s3 ls This command is used to list the S3 buckets in my account.

The terminal responded with positively, This indicated that the access keys I set up worked well.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_4334d778)

---

## Connecting to my S3 bucket

I also tested the command aws s3 ls which returned list bucket inside of my S3.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_4334d779)

---

## Uploading objects to S3

sudo touch /tmp/jmtech.txt

The second command I ran was aws s3 cp /tmp/jmtech.txt  s3://jmtech-s3/, this command will allow upload files in my S3 Bucket

The third command I ran was which validated that aws s3 ls s3://jmtech-s3-project

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_3e1e79a2)

---

## In the second part of my project...

### Step 5 - Set up a Gateway

In this step, I will Set up a way for your VPC and S3 to communicate direclty.

### Step 6 - Bucket policies

Limit your S3 bucket access's to only traffic from your endpoint.

### Step 7 - Update route tables

In this step, I will Test your VPC endpoint set up.
Troubleshoot a connectivity issue.

### Step 8 - Validate endpoint conection

In this step, I will Test your VPC endpoint set up (again).
Restrict your VPC's acccess to your AWS environment.

---

## Setting up a Gateway

I set up an S3 Gateway, which is a service that is accessible via internet.

### What are endpoints?

An endpoint is a connection point that allows resources in your VPC to privately access AWS services without using the public internet.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_09bcaa8a)

---

## Bucket policies

A bucket policy is a set of permissions that controls who can access an S3 bucket and what actions they are allowed to perform.

My bucket policy will deny all access.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_7316a13d)

---

## Bucket policies

Right after saving my bucket policy, my S3 bucket page showed 'denied access' warnings. This was because I dont now have access to my S3 bucket.

I also had to update my route table because I need to speficify that the traffic should pass through Endpoints.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_4ec7821f)

---

## Route table updates

To update my route table, I point it to Endpoint.

After updating my public subnet's route table, my terminal could return the best result showing accessing my S3 bucket through Endpoint.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_d116818e)

---

## Endpoint policies

An endpoint policy is an IAM-style policy applied to a VPC endpoint that defines what actions and resources are allowed or denied when traffic flows through that endpoint. It adds an extra layer of access control on top of IAM and bucket policie

I updated my endpoint's policy by deny I could see the effect of this right away, because I can no longer access my S3.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-endpoints_3e1e79a3)

---

---
