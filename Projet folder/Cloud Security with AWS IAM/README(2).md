<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

In this project, I will learn ho wto create IAM role and launch EC2 instance, I'm doing this project to learn and streghen my skills on AWS Cloud.

### Tools and concepts

Services I used were IAM and EC2 Key concepts I learnt include Policy, creating user and group and much more.

### Project reflection

This project took me approximately 2hours The most challenging part was deleting alias and recreating as I only modify the existing one It was most rewarding to do it.

---

## Tags

Tags are  like labels you can attach to AWS resources for organization.

The tag I’ve used on my EC2 instances is called... The value I’ve assigned for my instances are Envirroment and Production.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

IAM Policies are rules that say who can or can't do what.

### The policy I set up

For this project, I’ve set up a policy using Jason.

I’ve created a policy that allows a user to fully manage only EC2 resources tagged Env=development, read all EC2 resources, and prevents them from modifying any tags or managing resources not tagged Env=development.

### When creating a JSON policy, you have to define its Effect, Action and Resource.

The Effect, Action, and Resource attributes of a JSON policy means : ² Effect specifies whether the action is allowed or denied, Action defines what operations are permitted or blocked, and Resource indicates the specific AWS resources those actions apply to.

---

## My JSON Policy

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_1c864649)

---

## Account Alias

An account alias is a nickname log in in our aws account.

Creating an account alias took me... Now, my new AWS console sign-in URL is pelagie-aws-v1


![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### Users

IAM users represents a person or an application that needs access to your AWS environment.

### User Groups

IAM User Groups are like folders that organize users with similar permission needs, allowing you to apply policies to all of them at once.

I attached the policy I created to this user group, which means all users in the group will inherit those permissions.


---

## Logging in as an IAM User

The first way is by sharing in E-mail or by downloading the csv file.

Once I logged in as my IAM user, I noticed that I had not permission This was because the policy applied.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

I tested my JSON IAM policy by stoping instances.

### Stopping the production instance

When I tried to stop the production instance, It is not stopping This was because I have no permission.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_0e7a9d6a)

---

## Testing IAM Policies

### Stopping the development instance

Next, when I tried to stop the development instance, It stopped This was because I have permission on it. 

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-iam_1811801c)

---

## The IAM Policy Simulator

### How I used the simulator

---

---
