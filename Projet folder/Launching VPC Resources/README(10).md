<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-ec2)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

## Launching VPC Resources

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a virtual private cloud that lets you create and control your own isolated network inside AWS, and it is useful because it gives you full control over IP addressing, subnets, routing, and security to securely run your applications in the cloud.

### How I used Amazon VPC in this project

I used Amazon VPC to create staff like, subnet, NACL SG etc...

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was that I was troubleshooting some staff.

### This project took me...

This project took me 1h.

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means to have access on it.

### SSH is a key method for directly accessing a VM

SSH traffic means allowing access to my instances.

### To enable direct access, I set up key pairs

Key pairs help engineers directly access their virtual machines, like EC2 instances.

Just like how documents can be saved in various file formats like PDF, DOCX, or TXT, each suited for different applications or systems, private keys also come in different file formats. Not every system or application can process all these formats, so choosing the right one is crucial. Format of my private key what  .pem 

---

## Launching a public server

I had to change my EC2 instance's networking settings by going in the networking section.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has its own dedicated security group because I dont need it to access anywhere.

My private server's security group's source is JMtech-Private-SG which means resources that are part of the JMtech-Private-SG can communicate with your instance. 

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I use the Wizard VPC and more.

A graphical view (a visual diagram) that shows all the resources created or associated with your VPC, automatically organized by AWS.

It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because VPCs are isolated from each other. They act as separate networks, so overlapping CIDR blocks are allowed unless you try to connect the VPCs together.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

I can create up to 2.

NAT gateways allow my Private ressources to have internet connexion.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-ec2_8ee57662)

---

---
