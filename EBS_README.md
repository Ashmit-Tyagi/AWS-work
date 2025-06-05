# EC2 Snapshot, AMI Creation, and Data Consistency – AWS Workflow

## 1. Launch Initial EC2 Instance

![image](https://github.com/user-attachments/assets/a036cedc-106f-4fc2-b941-5ec73c36f2a1)


## 2. Add Files to EBS Root Volume


## 3. Create Snapshot of the Root Volume

![image](https://github.com/user-attachments/assets/659af207-384f-4ffb-9544-b6deb29253ca)


## 4. Create EBS Volume from Snapshot


![image](https://github.com/user-attachments/assets/61d864e7-7733-4ea5-ae92-1df5f0395180)


## 5. Create AMI from Snapshot

![image](https://github.com/user-attachments/assets/aa302f97-e635-4a6e-aed0-6336044a26de)


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
