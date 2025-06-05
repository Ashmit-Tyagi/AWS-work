# AWS S3 Bucket: Create, Upload, and Browse Using AWS CLI

# Prerequisites

	•	AWS CLI installed (aws --version)
	•	AWS CLI configured (aws configure) with valid Access Key and Secret Key
	•	An IAM user with necessary S3 permissions
	•	A text file (e.g., sample.txt) ready for upload

## 1. Create an S3 Bucket

![image](https://github.com/user-attachments/assets/16629ae7-bda8-4d2b-8580-fdb56eac831b)

![image](https://github.com/user-attachments/assets/c6370c00-3a64-4a76-b12f-9346d0e197a4)


## 2. Upload a File to the Bucket

![image](https://github.com/user-attachments/assets/865e8d09-6a37-4131-8089-3aa241af744a)


## 3. Make the File Publicly Accessible

![image](https://github.com/user-attachments/assets/64a449d3-d00f-4448-969e-54a35898555d)


## 4. Access the File via Browser

![image](https://github.com/user-attachments/assets/296d5904-0fd9-44e1-91a8-b59499e88aff)


## Summary

This task demonstrates how to create an Amazon S3 bucket using AWS CLI, upload a sample text file, and make it publicly accessible over the internet. Using commands like aws s3api create-bucket and aws s3 cp, you can manage file storage efficiently. By setting the object’s ACL to public-read or applying a bucket policy, the file becomes accessible via a public S3 URL, enabling easy sharing and static file hosting.






