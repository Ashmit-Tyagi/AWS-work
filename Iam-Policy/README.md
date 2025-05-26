# Creating a Custom IAM Policy

This IAM policy is designed to provide limited EC2 instance control with the following permissions and restrictions:

a. Start and Stop Instances (us-west-2 only):
The user is allowed to start and stop EC2 instances, but only within the us-west-2 (Oregon) region. This ensures control is limited to a specific AWS region.

b. View EC2 Instances Across All Regions:
The user has read-only access to describe and list EC2 instances (DescribeInstances) in any region, enabling visibility into existing infrastructure.

c. Deny Termination of Instances (All Regions):
The policy explicitly denies the ability to terminate EC2 instances (TerminateInstances), preventing accidental or unauthorized deletion of any instance.

![Screenshot 2025-05-26 170551](https://github.com/user-attachments/assets/f29418c1-bf16-486b-8ee3-eab6ef51a828)
