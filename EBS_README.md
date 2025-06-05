# EC2 Snapshot, AMI Creation, and Data Consistency – AWS Workflow

## 1. Launch Initial EC2 Instance


## 2. Add Files to EBS Root Volume


## 3. Create Snapshot of the Root Volume


## 4. Create EBS Volume from Snapshot



## 5. Create AMI from Snapshot


## 6. Launch EC2 from New AMI


## 7. Launch EC2 and Attach EBS Volume

- SSH into the EC2 and mount the volume
- You should see the files and directories from the original instance here as well.

## Summary

By using both EBS Snapshots and custom AMIs, we demonstrated how to:

	•	Back up and clone EC2 env
 
	•	Recover data
 
	•	Ensure system consistency
 
	•	Support scaling and DR strategies in AWS
