# Setup of EMR on AWS

### 1. Go to EC2 > Create Cluster

### 2. Give cluster name

### 3. Select Amazon EMR release -> emr-6.15.0

### 4 Click Cluster Configuration -> Add a instance group to add one more instance to create a 4 cluster group
![Image Launch Instance](https://github.com/dm0927/Cloud-Assignment-2/blob/main/images/Screenshot%202023-12-08%20at%201.16.04%E2%80%AFAM.png)

### 5. Security configuration and EC2 key pair -> Add Amazon EC2 key pair for SSH to the cluster

### 6. Select Role
        --> Amazon EMR service role
        --> EMR_DefaultRole

        --> EC2 instance profile for Amazon EMR
        --> EMR_DefaultRole


### 7. Create Cluster

Once cluster is created you have to go to security of ec2 isntances and open a port 22 and custom IP Address.

