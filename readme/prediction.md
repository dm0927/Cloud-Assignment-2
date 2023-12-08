# Setup of EC2 Instance on AWS

### 1. Go to EC2

### 2. Click on Launch Instance

### 3. Use the step which are there below the image
![Image Launch Instance](https://github.com/dm0927/Cloud-Assignment-2/blob/main/images/Screenshot%202023-12-08%20at%2012.44.25%E2%80%AFAM.png)

## Once done you can now connect with ssh command
```bash
ssh command
```

Install Java
Both Apache Spark and Apache Hadoop require Java. You can install OpenJDK using the following commands:


```bash
sudo apt update
sudo apt install openjdk-8-jdk
```

Add the following lines at the end of the file:

```bash
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64   # Replace this path with the correct path to your Java installation
export PATH=$PATH:$JAVA_HOME/bin
```

# Install AWS-CLI

Using Package Manager (e.g., apt on Ubuntu):
```bash
sudo apt update
sudo apt install awscli
```

## Configure AWS CLI:
After installing the AWS CLI, you need to configure it with your AWS credentials. Open a terminal and run:

```bash
aws configure
```

# Install Hadoop

### Step 1: Download and Extract Hadoop
```bash
wget https://downloads.apache.org/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz
tar -xzvf hadoop-3.3.6.tar.gz
sudo mv hadoop-3.3.6 /opt/hadoop
```

### Step 2: Configure Hadoop
Edit ~/.bashrc or ~/.bash_profile and add the following lines:

```bash
export HADOOP_HOME=/opt/hadoop
export PATH=$PATH:$HADOOP_HOME/bin
```

Then, refresh your shell:

```bash
source ~/.bashrc   # or source ~/.bash_profile
```

### Step 3: Test Hadoop Installation

```bash
hadoop version
```

# Install Spark

### Step 1: Download and Extract Spark

```bash
wget https://downloads.apache.org/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz
tar -xzvf spark-3.5.0-bin-hadoop3.tgz
sudo mv spark-3.5.0-bin-hadoop3 /opt/spark
```

### Step 2: Configure Spark

Edit ~/.bashrc or ~/.bash_profile and add the following lines:

```bash
export SPARK_HOME=/opt/spark
export PATH=$PATH:$SPARK_HOME/bin
export HADOOP_HOME=/opt/hadoop
export PATH=$PATH:$HADOOP_HOME/bin
```

Then, refresh your shell:

```bash
source ~/.bashrc   # or source ~/.bash_profile
```

Step 3: Test Spark Installation
```bash
spark-shell
```

This should start the Spark shell, indicating a successful installation.