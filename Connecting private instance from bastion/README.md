# Connect to a Private EC2 Instance Using a Bastion Host #

Steps :

### 1. Create a VPC
  `CIDR block: 10.0.0.0/16`
  
  ![Screenshot 2025-05-25 234719](https://github.com/user-attachments/assets/a70f0809-f695-4788-88d0-5592faf163a5)
  

### 2. Create Two Subnets: 

  `Public Subnet: 10.0.1.0/24`

  `Private Subnet: 10.0.2.0/24`

  ![Screenshot 2025-05-25 234936](https://github.com/user-attachments/assets/3ea83189-cdde-47bd-a8b7-f14814d2b799)


### 3. Set Up Internet Access

a. Create an Internet Gateway and attach it to your VPC

![Screenshot 2025-05-25 235041](https://github.com/user-attachments/assets/9f466bfc-4520-4839-9090-ffc138efcf60)


b. Update the route table for the public subnet:

Add route 0.0.0.0/0 → target the Internet Gateway

![Screenshot 2025-05-25 235528](https://github.com/user-attachments/assets/befd8a5e-e028-4a27-9594-d652ebee31de)


### 4. Launch EC2 Instances

One in the public subnet = Bastion host

One in the private subnet = Private instance

Use different key pairs for both:

Bastion EC2 → bastion.pem

Private EC2 → pvt-key.pem


### 5. SSH into the Bastion Host
From your local system, run:

  `ssh -i "path/to/bastion-key.pem" ubuntu@<public-ip-of-bastion>`
Send the Private Key to Bastion Host

![Screenshot 2025-05-26 004114](https://github.com/user-attachments/assets/37433f54-6fd1-4e43-8208-a75174d9d6d9)


Still from your local machine, send the private EC2 key:

  `scp -i "path/to/bastion-key.pem" path/to/private-key.pem ubuntu@<public-ip-of-bastion>:~`
SSH into Bastion Again & Set Permissions

chmod 400 private-key.pem
Now SSH into the Private EC2 from Bastion Host

  `ssh -i private-key.pem ubuntu@<private-ip-of-private-ec2>`

![Screenshot 2025-05-26 005641](https://github.com/user-attachments/assets/4fcefc77-9316-4f4b-8c8b-a7e16f5698f8)
