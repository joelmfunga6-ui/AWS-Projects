<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Monitoring with Flow Logs

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-monitoring)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

## VPC Monitoring with Flow Logs

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_3e1e79a1)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a virtual private network environment in AWS where you can launch and control your cloud resources. It is useful because I need to test features like VPC Flow Logs, security groups, NACLs, and network connectivity scenarios.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create VPC Flow logs etc.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was troubleshooting.

### This project took me...

This project took me 1h.


---

## In the first part of my project...

### Step 1 - Set up VPCs

In this step, I will Create two VPCs from scratch!

### Step 2 - Launch EC2 instances

In this step, I will Launch an EC2 instance in each VPC, so we can use them to test your VPC peering connection later.

### Step 3 - Set up Logs

Set up a way to track all inbound and outbound network traffic.
Set up a space that stores all of these records.

### Step 4 - Set IAM permissions for Logs

Give VPC Flow Logs the permission to write logs and send them to CloudWatch.
Finish setting up your subnet's flow log.

---

## Multi-VPC Architecture

I started my project by launching VPC-1 and 2. VPC-1 and I create 2 subnets.

The CIDR blocks for VPCs 1 and 2 are... They have to be unique because overlapsing.

### I also launched EC2 instances in each subnet

My EC2 instances' security groups allow All ICMP4 traffic.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_e7fa8775)

---

## Logs

Logs are like a diary for your computer systems. They record everything that happens, from users logging in to errors popping up. It's the go-to place to understand what's going on with your systems, troubleshoot problems, and keep an eye on who’s doing what.

Think of a log group as a big folder in AWS where you keep related logs together. Usually, logs from the same source or application will go into the same log group, BUT logs are also region-specific. This means log data gets created and saved in the region it was created, although you can use CloudWatch dashboards to bring together logs from different regions.

### I also set up a flow log for VPC 1

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_e8398869)

---

## IAM Policy and Roles

I created an IAM policy because to allow Cloudwatch.

I also created an IAM role because I need to allow VPC Flow Logs.

A custom trust policy is specific type of policy! They're different from IAM policies. While IAM policies help you define the actions a user/service can or cannot do, custom trust policies are used to very narrowly define who can use a role.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_4334d777)

---

## In the second part of my project...

### Step 5 - Ping testing and troubleshooting

In this step, I will Get Instance 1 to send test messages to Instance 2.

### Step 6 - Set up a peering connection

In this step, I will Set up a connection link between your VPCs.

### Step 7 - Analyze flow logs

In this step, I will Review the flow logs recorded aboout VPC 1's public subnet.
Analyse the flow logs to get some tasty insights 👀

---

## Connectivity troubleshooting

My first ping test between my EC2 instances had no replies, which means packet sent back the other side is not responding.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_99d4ba42)

I could receive ping replies if I ran the ping test using the other instance's public IP address, which means Receiving ping replies from the public IPv4 address means Instance 2 is correctly configured to respond to ping requests, and Instance 1 can actually communicate with Instance 2 if it traffic goes across the public internet!

---

## Connectivity troubleshooting

Looking at VPC 1's route table, I identified that the ping test with Instance 2's private address failed because the is no peering connection.

### To solve this, I set up a peering connection between my VPCs

I also updated both VPCs' route tables so that both EC2 can communicate.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_7316a13d)

---

## Connectivity troubleshooting

I received ping replies from Instance 2's private IP address! This means there is connectivity.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_4ec7821f)

---

## Analyzing flow logs

Flow logs tell us about the network traffic that is accepted or rejected within a VPC.

For example, the flow log I've captured tells us requested accepted succesfully.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_d116818e)

---

## Logs Insights

Logs Insights is a powerful query tool in CloudWatch that lets you search, analyze, and visualize log data in seconds.

I ran the query. This query analyzes the log data to identify patterns, errors, and traffic behavior based on specific fields and filters.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-networks-monitoring_3e1e79a1)

---

---
