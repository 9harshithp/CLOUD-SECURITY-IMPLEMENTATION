# CLOUD-SECURITY-IMPLEMENTATION

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: HARSHITH P

**INTERN ID**:CT08IJR

**DOMAIN**: Cloud Computing

**BATCH DURATION**: January 30th, 2025 to March 1st, 2025

**MENTOR NAME**: NEELA SANTHOSH

**ENTER DESCRIPTON OF TASK PERFORMED NOT LESS THAN 500 WORDS**:
Securing cloud-based resources is critical to protecting sensitive data and ensuring compliance with industry best practices. As part of this task, I implemented cloud security measures for an Amazon S3 bucket, focusing on identity and access management (IAM) policies, encryption for data security, and monitoring mechanisms. Below is a comprehensive description of the task performed, broken down into key steps with a humanized narrative of the experience.

The first step was to validate and configure access to the S3 bucket. I started by creating a bucket named my-secure-bucket914 and ensuring it followed the naming conventions. After the bucket was created, the focus shifted to securing access through a well-defined bucket policy. Crafting this policy involved specifying the Principal field to restrict access to a single IAM user, ensuring that only authorized individuals could interact with the bucket. I used the AWS Console’s Permissions tab to enter the policy, referencing the correct resource ARN and IAM user ARN. Initially, I encountered an error—“Invalid principal in policy”—which turned out to be due to an incorrect IAM user ARN. This required cross-verifying the user ARN in the IAM Dashboard and replacing it with the correct format. Once corrected, the policy worked as expected, granting s3:GetObject permissions to the intended user while denying all other actions.

To enhance data security, I enabled encryption on the bucket. Encryption is vital for ensuring that even if data is intercepted, it remains unreadable. Using the AWS S3 Console, I navigated to the bucket’s Properties tab and enabled server-side encryption. I opted for SSE-KMS (Server-Side Encryption with AWS Key Management Service), as it provides a higher level of control over encryption keys. During the process, I selected an AWS-managed KMS key for simplicity. Additionally, I enabled the Bucket Key option, which optimizes performance and reduces the cost of encryption operations. This step added an essential layer of protection to data stored in the bucket.

To ensure accountability and traceability, I implemented logging and monitoring mechanisms. I started by enabling S3 Server Access Logging, which records all access requests made to the bucket. This involved creating a separate bucket for logs and configuring the original bucket to send logs to this target bucket. Additionally, I integrated AWS CloudTrail to monitor S3 data events such as GetObject and PutObject. CloudTrail ensures that every action on the bucket is recorded and can be reviewed for suspicious activity. This setup provided a robust way to track usage and identify potential security breaches.

After configuring the bucket, I conducted thorough testing to validate the policy and security setup. Using the AWS CLI and the S3 Console, I tested the permissions granted to the IAM user. The results confirmed that the user could only perform the allowed actions (s3:GetObject) and was blocked from performing unauthorized actions such as s3:DeleteObject. This demonstrated that the bucket policy was correctly applied. Testing encryption was straightforward, as uploading and downloading objects showed the use of encryption keys.

Finally, I documented the entire process in a structured report. This included the bucket policy JSON, details of the encryption setup, and a summary of the testing results. The report also highlighted monitoring mechanisms in place and provided recommendations for future reviews.

This task emphasized the importance of detailed configurations and iterative testing to secure cloud resources. By implementing IAM policies, encryption, and monitoring, I ensured that the S3 bucket was not only secure but also auditable, providing a strong foundation for protecting sensitive data.

**output of the task**:
<img width="937" alt="Image" src="https://github.com/user-attachments/assets/08b50f50-8b8f-4286-b67b-51841cc7bbcc" />

<img width="958" alt="Image" src="https://github.com/user-attachments/assets/aa1dfbf9-ab77-4faf-a7b1-01c21076d75d" />

<img width="955" alt="Image" src="https://github.com/user-attachments/assets/9d74dfa8-796f-4013-b3c7-5b01b79f65bd" />
