<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Peering

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-peering)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

## VPC Peering

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_88727bef)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC (Virtual Private Cloud) is a logically isolated section of the AWS cloud where you can launch AWS resources—like EC2 instances, databases, and load balancers—inside your own virtual network that you control.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create staff related in this project like, IG, NACL, SG etc.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was error.

### This project took me...

This project took me 1h.

---

## In the first part of my project...

### Step 1 - Set up my VPC

In this step, I will Create two VPCs from scratch! and Use the visual VPC resource map to create your VPCs supa fast

### Step 2 - Create a Peering Connection

In this step, I will Set up a connection link between your VPCs because I will further test the connectivity.

### Step 3 - Update Route Tables

In this step, I will Set up a way for traffic coming from VPC 1 to get to VPC 2 and Set up a way for traffic coming from VPC 2 to get to VPC 1.

### Step 4 - Launch EC2 Instances

In this step, I will Launch an EC2 instance in each VPC, so we can use them to test your VPC peering connection later.

---

## Multi-VPC Architecture

I started my project by launching 1.

The CIDR blocks for VPCs 1 and 2 are... They have to be unique because I evoid overlapsing.

### I also launched 2 EC2 instances

I didn't set up key pairs for these EC2 instances as I will not need to SSH it.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_11111111)

---

## VPC Peering

A VPC peering connection is a direct connection between two VPCs.

A peering connection lets VPCs and their resources route traffic between them using their private IP addresses. This means data can now be transferred between VPCs without going through the public internet.

Without a peering connection, data transfers between VPCs would use resources' public address - meaning VPCs have to communicate over the public internet. 

In VPC peering, the Accepter is the VPC that receives a peering connection request! The Accepter can either accept or decline the invitation. And requester is the one who initiate the connection.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_1cbb1b88)

---

## Updating route tables

After accepting a peering connection, my VPCs' route tables need to be updated because Allow connectivity between VPCs.


My VPCs' new routes have a destination of 10.1.0.0/16, 10.2.0.0/16 The routes' target was 10.1.0.0/16, 10.2.0.0/16.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_4a9e8014)

---

## In the second part of my project...

### Step 5 - Use EC2 Instance Connect

In this step, I will Use EC2 Instance Connect to connect to your first EC2 instance and Fix a connection error!

### Step 6 - Connect to EC2 Instance 1

In this step, I will Use EC2 Instance Connect to connect to Instance 1 (one more time) and Fix (another) error.

### Step 7 - Test VPC Peering

In this step, I will Get Instance 1 to send test messages to Instance 2 and Solve connection errors until Instance 2 is able to send messages back.

---

## Troubleshooting Instance Connect

Next, I used EC2 Instance Connect to my EC2 instances.

I was stopped from using EC2 Instance Connect as my EC2 instance didn't have the public IP.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_7685490c)

---

## Elastic IP addresses

To resolve this error, I set up Elastic IP addresses. Elastic IP addresses ar static public IP.

Associating an Elastic IP address resolved the error because I allocate IP to my instances.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_45663498)

---

## Troubleshooting ping issues

To test VPC peering, I ran the command ping.

A successful ping test would validate my VPC peering connection because the other side reply positivily by sendi packet.

I had to update my second EC2 instance's security group because I need to allow connectivity I added a new rule that allow all ICMP4 all.

![Image](https://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-peering_7a29d352?v=1)

---

---
