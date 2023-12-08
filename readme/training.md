# Setup of EMR on AWS

### 1. Go to EC2 -> Create Cluster

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

# Connect to EMR Instance

### 1. Connect to SSH Server

```bash
ssh -i "CS643-Cloud.pem" hadoop@ec2-3-92-224-244.compute-1.amazonaws.com
```

### 2. Copy the file from local to EMR Instance
You need to exit from EMR instance and then use the below command

```bash
scp -i CS643-Cloud.pem ~/Desktop/ProgrammingAssignment2-main/training.py ubuntu@ec2-34-207-132-95.compute-1.amazonaws.com:~/trainingModel
```

Once done reconnect to server using ssh command

### 3. Create a `Virtual Environment`

Navigate to your project folder and create a virtual environment (replace "venv" with your preferred name):

```bash
python -m venv venv
```

### 4. Activate the `Virtual Environment`

```bash
source venv/bin/activate
```

### 5. Install Project Dependencies

```bash
pip install -r requirements.txt
```

### 6. Execute the command

```bash
python training.py```