<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-private)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

## Creating a Private Subnet

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is my own private network inside AWS. It is useful because it allows me to create and control my own isolated subnets, define routing, and secure my resources.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create subnet, route table, NACL etc.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is that It is a simple one.

### This project took me...

This project took me 1h

---

## Private vs Public Subnets

The difference between public and private subnets is that private subnet is reachable in the world of internet whereas private subnet is not.

Having private subnets are useful because it will allow us to keep some ressources in private. 

My private and public subnets cannot have the same CIDR.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with 10.0.1.0/24

I had to set up a new route table because I need to keep this subnet private.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows all traffic.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with the defaut one created by AWS which allo all traffic inbound and outbound.

I set up a dedicated network ACL for my private subnet because I dont need to expose my private subnet.

My new network ACL has two simple rules inbound is deny and outbound is deny.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-private_1ed2cb07)

---

---
