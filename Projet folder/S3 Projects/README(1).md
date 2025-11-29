<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use S3 to host a static website. I am doing this project to learn about AWS and cloud services and how they can be used to store objects in the cloud AND even host websites (how does that work?!)

### Tools and concepts

hosted your very own static website on Amazon S3.

### Project reflection

This project took me approximately 1h

---

## How I Set Up an S3 Bucket

Creating an S3 bucket took us less than 5 minutes – we needed to learn a few new concepts like block public access and ACLs, but once that learning is done, we can create buckets in even shorter time in the future!


The Region I picked for my S3 bucket was Virginia because It is the Region that is close to me.

S3 bucket names are globally unique!
This means no two Amazon S3 buckets in the entire world can have the same name.
They have to be completely unique (just like you), regardless of the region or the account ID.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### index.html and image assets

I uploaded two files to my S3 bucket - they were index.html and folder contains images and others files.

Both files are necessary for this project as index.html determines the structure, but the structure alone does not illustrate the contents of the website. 

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

Website hosting is what makes your website public on the internet.

Configure the following settings:

Static web hosting: Choose Enable.

Hosting type: Choose Host a static website.

Index document: Enter index.html

An ACL is a set of rules that decides who can get access to a resource.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

Once static website is enabled, S3 produces a bucket endpoint URL, which is http://pelagiemfunga-websiteproject.s3-website-us-east-1.amazonaws.com/

When I first visited the bucket endpoint URL, I saw... The reason for this error was 403 Forbidden

    Code: AccessDenied
    Message: Access Denied
    RequestId: JN2Y3CDJYYCX6HG1
    HostId: Q/jocjDfa6stWV6y+2un4P7eq0Sdv9hQm25GQeNEaQBiLeLW5ZpjQoyWTlush+DfyV8scISBkmc=


![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

To resolve this 403 Forbidden error, I make it public with Acls

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

---

---
