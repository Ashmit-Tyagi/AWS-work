# Auto Scaling EC2 Instances Using Launch Templates and AMI 


## Step-by-Step Setup

### 1. Create a EC2 Instance

- Choose a base AMI (Amazon Linux 2 or Ubuntu)
- Launch the instance

  ![Screenshot 2025-05-26 013424](https://github.com/user-attachments/assets/bb847db0-a12d-4c39-8f17-d9b03c61b30d)


### 2. Create an AMI (Amazon Machine Image)

- Once the EC2 is configured:
  - Go to Actions → Image → Create Image
  - Name it (e.g., `MyWebServerAMI`)

![Screenshot 2025-05-26 013515](https://github.com/user-attachments/assets/d0f7d12f-8d74-4608-9d54-f26160df46f8)


### 3. Create a Launch Template

  - Name: `WebServerTemplate`
  - AMI: Use the AMI created above
  - Instance Type: e.g., `t2.micro`
  - Security Group : Allow HTTP (port 80) and SSH (port 22)  
  - Launch Template

![Screenshot 2025-05-26 013819](https://github.com/user-attachments/assets/3af1dcff-ef4e-40bf-ac00-7143f23bd919)


### 4. Create Auto Scaling Group (ASG)

- Name your ASG (e.g., `WebServerASG`)
- Choose Launch Template you created
- Select VPC and Subnets
- Set Desired, Min, and Max capacity:
  - Desired: `1`, Min: `1`, Max: `3`

![Screenshot 2025-05-26 014442](https://github.com/user-attachments/assets/69844dab-c7d7-47ca-b7e1-74dd9c1519e1)

- Click Create Auto Scaling Group

![Screenshot 2025-05-26 014537](https://github.com/user-attachments/assets/f74417dd-042a-484c-a76b-45ae079ae301)


# Testing Auto Scaling

1. EC2 → Instances
![Screenshot 2025-05-26 014753](https://github.com/user-attachments/assets/2dd72bbc-d8cb-43ee-9ca4-3e1433a3009a)
  
2. Terminate one instance launched by ASG
   
3. ASG will automatically launch a new instance to maintain capacity

![Screenshot 2025-05-26 015119](https://github.com/user-attachments/assets/06c8a530-6785-48e8-91ff-0c54c42d0f53)

