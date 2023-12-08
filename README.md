# Installing Apache Spark on macOS using Homebrew

## Install Homebrew - This was the setup used to run the predection and training on local pc

If you don't have Homebrew installed, you can install it by running the following command in your terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

# Install Apache Spark
## Once Homebrew is installed, you can use it to install Apache Spark. Run the following commands:

```bash
brew install apache-spark
```

# Install Apache Hadoop

Spark depends on Hadoop, so you also need to install Hadoop using Homebrew:

```bash
brew install hadoop
```

# Set Environment Variables

Set the environment variables SPARK_HOME and HADOOP_HOME in your shell configuration file (e.g., .bash_profile, `.zshrc, etc.). Open the file in a text editor and add the following lines:

```bash
export SPARK_HOME=/usr/local/opt/apache-spark/libexec
export HADOOP_HOME=/usr/local/opt/hadoop
```

Save the file and either restart your terminal or run source ~/.bash_profile (or the corresponding command for your shell) to apply the changes.

# Verify Installation

To verify the installation, you can run Spark's built-in example:

```bash
spark-shell
```

If everything is set up correctly, you should see the Spark shell prompt.


# Installing AWS-CLI on Mac

## If you have sudo permissions, you can install the AWS CLI for all users on the computer. We provide the steps in one easy to copy and paste group. See the descriptions of each line in the following steps.

```bash
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg AWSCLIV2.pkg -target /
```

Download the file using the curl command. The -o option specifies the file name that the downloaded package is written to. In this example, the file is written to AWSCLIV2.pkg in the current folder.

```bash
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
```

Run the standard macOS installer program, specifying the downloaded .pkg file as the source. Use the -pkg parameter to specify the name of the package to install, and the -target / parameter for which drive to install the package to. The files are installed to /usr/local/aws-cli, and a symlink is automatically created in /usr/local/bin. You must include sudo on the command to grant write permissions to those folders.

```bash
sudo installer -pkg ./AWSCLIV2.pkg -target /
```
After installation is complete, debug logs are written to /var/log/install.log.

To verify that the shell can find and run the aws command in your $PATH, use the following commands.

```bash
which aws
/usr/local/bin/aws 
$ aws --version
aws-cli/2.10.0 Python/3.11.2 Darwin/18.7.0 botocore/2.4.5
```

# Setup of Cluster on AWS

How to setup cluster on AWS [Click Here](https://github.com/dm0927/Cloud-Assignment-2/blob/main/readme/training.md)

# Setup of Predection on EC2 Instance

How to setup predection on ec2 instance [Click Here](https://github.com/dm0927/Cloud-Assignment-2/blob/main/readme/prediction.md)