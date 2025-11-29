<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Encrypt Data with AWS KMS

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-kms)

**Author:** Joel Mfunga  
**Email:** joelmfunga6@gmail.com

---

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-kms_w0x1y2z3)

---

## Introducing Today's Project!

In this project, I will demonstrate using KMS to secure data The goal is to create encryption keys in AWS.

### Tools and concepts

Services I used include DynamoDB Key concepts I learnt include encryption with KMS.

### Project reflection

This project took me approximately 1h 

I chose to do this project today because It has helped me to understand better the KMS.

---

## Encryption and KMS

is a process that uses algorithms to convert data into a secure format called ciphertext. Only authorised users can decrypt and restore the data to its original, readable state.

AWS Key Management Service (KMS) is a secure vault for your encryption keys. You use KMS to create, manage, and use encryption keys that protect the data in your AWS resources.

Symmetric encryption use a single encryption key to both lock (encrypt) and unlock (decrypt) your data. They are generally faster and more efficient for encrypting large amounts of data, which is why we're using one for our DynamoDB table. 

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-kms_a2b3c4d5)

---

## Encrypting Data

DynamoDB is one of AWS's database services. DynamoDB stands out as a fast and flexible way to store your data, which makes it a great choice for applications that need quick access to large volumes of data e.g. games.

Owned by Amazon DynamoDB: Amazon DynamoDB fully manages the key, so you have no access or visibility to the key. Great for basic encryption where you don't need any control.



AWS managed key: AWS Key Management Service (KMS) manages the key, so it's not a customer managed key like what we created! You can see the key and its usage, but management is done by AWS.



Stored in your account, and owned and managed by you: aka a customer managed key (CMK). You create and manage the key in KMS, giving you full control. T

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-kms_q8r9s0t1)

---

## Data Visibility

Rather than controlling who has access to the key directly, AWS KMS manages user permissions by automatically enforcing IAM policies and key policies.

Even though the data is encrypted, you as a user have permissions to use the encryption key in KMS.

DynamoDB is designed to decrypt the data on your behalf. When data is requested by an authorized user (like you) or an authorized application, DynamoDB retrieves the encrypted data, decrypts it with the key, then shows you the decrypted format so you can use it instantly. This security feature is called transparent data encryption.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-kms_c0d1e2f3)

---

## Denying Access

I configured a new IAM user to teste The permission policies I granted this user are.

ou don't have permission to kms:Decrypt means your user isn’t allowed to decrypt the data. This highlights how KMS works - a KMS key can be accessible to many users, but only those with the right permissions can use it to do specific actions like encryption or decryption.

![Image](http://learn.nextwork.org/nostalgic_indigo_jolly_prickly_pear/uploads/aws-security-kms_w0x1y2z3)

---

## EXTRA: Granting Access

---

---
