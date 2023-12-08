# Installing Apache Spark on macOS using Homebrew

## Install Homebrew

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
