# 🐍 Python for DevOps

Python is widely used in DevOps for **automation, scripting, cloud management, API interaction, monitoring, and deployment tasks**.

This section covers the Python concepts that are important for **Cloud & DevOps interviews and practical automation**.

---

## 📚 1. Python Fundamentals

* Variables
* Data Types
* Operators
* Input and Output
* Conditional Statements
* `if`, `elif`, `else`
* `for` loop
* `while` loop
* `break`, `continue`, `pass`

---

## 📦 2. Python Data Structures

### List

```python
servers = ["web01", "web02", "web03"]
print(servers)
```

### Tuple

```python
ports = (22, 80, 443)
print(ports)
```

### Set

```python
services = {"nginx", "docker", "jenkins"}
print(services)
```

### Dictionary

```python
server = {
    "name": "web01",
    "ip": "192.168.1.10",
    "status": "running"
}

print(server["name"])
```

---

## 🔧 3. Functions

Learn:

* Creating functions
* Parameters
* Arguments
* Return values
* Default arguments
* Lambda functions
* Modules

Example:

```python
def check_server(status):
    if status == "running":
        return "Server is running"
    return "Server is down"

print(check_server("running"))
```

---

## 📁 4. File Handling

File handling is important for working with:

* Configuration files
* Log files
* Reports
* CSV files
* JSON files

Example:

```python
with open("server.log", "r") as file:
    data = file.read()

print(data)
```

---

## ⚠️ 5. Exception Handling

Used to prevent automation scripts from crashing unexpectedly.

```python
try:
    number = int(input("Enter number: "))
    print(10 / number)

except ValueError:
    print("Invalid input")

except ZeroDivisionError:
    print("Cannot divide by zero")

finally:
    print("Program completed")
```

---

# 🚀 Python for DevOps

These are the most important Python topics for DevOps.

## 🖥️ 6. `os` Module

Used to interact with the operating system.

```python
import os

print(os.getcwd())
print(os.listdir())
```

Useful for:

* Working with directories
* Environment variables
* File paths
* Operating-system information

---

## ⚙️ 7. `subprocess` Module

Used to execute Linux/Unix commands from Python.

```python
import subprocess

result = subprocess.run(
    ["df", "-h"],
    capture_output=True,
    text=True
)

print(result.stdout)
```

### DevOps Uses

* Execute shell commands
* Run deployment commands
* Automate server tasks
* Execute scripts
* Collect command output

---

## 🌎 8. Environment Variables

Environment variables are commonly used for configuration and secrets.

```python
import os

username = os.getenv("USERNAME")

print(username)
```

Example:

```bash
export ENVIRONMENT=production
```

Python:

```python
import os

environment = os.getenv("ENVIRONMENT")

print(environment)
```

> Never hard-code passwords, API keys, AWS secret keys, or other credentials in GitHub repositories.

---

## 📄 9. JSON

JSON is heavily used in:

* REST APIs
* AWS
* Configuration files
* CI/CD tools
* Cloud automation

```python
import json

data = {
    "server": "web01",
    "status": "running"
}

with open("server.json", "w") as file:
    json.dump(data, file, indent=4)
```

---

## 🌐 10. API Automation

Learn how to communicate with REST APIs using Python.

Install:

```bash
pip install requests
```

Example:

```python
import requests

response = requests.get("https://api.github.com")

print(response.status_code)
print(response.json())
```

Important concepts:

* GET
* POST
* PUT
* DELETE
* HTTP status codes
* Headers
* JSON responses

---

# ☁️ AWS Automation with Python

## 11. Boto3

`Boto3` is the AWS SDK for Python.

Install:

```bash
pip install boto3
```

Example — list EC2 instances:

```python
import boto3

ec2 = boto3.client("ec2")

response = ec2.describe_instances()

for reservation in response["Reservations"]:
    for instance in reservation["Instances"]:
        print(instance["InstanceId"])
```

### Important AWS Services to Practice

* EC2
* S3
* IAM
* CloudWatch
* Lambda
* VPC

---

# 📝 Interview Programs

Practice these basic programs:

1. Reverse a string
2. Check palindrome
3. Find largest number
4. Find smallest number
5. Find duplicate elements
6. Remove duplicates
7. Count word frequency
8. Count vowels
9. Check prime number
10. Generate Fibonacci series
11. Find factorial
12. Find second-largest number
13. Sort a list
14. Merge two lists
15. Read and analyze a log file

---

# 🔥 DevOps Automation Programs

These are more important for a DevOps profile.

### Beginner

* Check whether a file exists
* Create a directory
* Delete a file
* Rename a file
* Read a log file
* Count lines in a file

### Intermediate

* Check disk usage
* Check running processes
* Execute Linux commands
* Monitor a service
* Search errors in log files
* Backup a directory
* Read environment variables
* Parse JSON configuration

### Advanced

* REST API automation
* AWS EC2 automation
* AWS S3 automation
* CloudWatch automation
* Automated log analysis
* Server monitoring script

---

# 🛠️ Mini Projects

## 1. Log Analyzer

Python script that:

* Reads a log file
* Searches for `ERROR`
* Counts errors
* Displays important log entries

## 2. System Monitoring Script

Monitor:

* CPU usage
* Memory usage
* Disk usage
* Running processes

## 3. Backup Script

Automate:

* Directory backup
* File compression
* Backup naming
* Backup storage

## 4. AWS Automation

Use Boto3 to:

* List EC2 instances
* Start/stop EC2 instances
* List S3 buckets
* Upload files to S3

---

# 🎯 Interview Focus

For Cloud & DevOps interviews, focus more on:

| Topic                 | Priority |
| --------------------- | -------- |
| Lists & Dictionaries  | ⭐⭐⭐⭐⭐    |
| Functions             | ⭐⭐⭐⭐⭐    |
| File Handling         | ⭐⭐⭐⭐⭐    |
| Exception Handling    | ⭐⭐⭐⭐⭐    |
| `os`                  | ⭐⭐⭐⭐⭐    |
| `subprocess`          | ⭐⭐⭐⭐⭐    |
| JSON                  | ⭐⭐⭐⭐⭐    |
| Environment Variables | ⭐⭐⭐⭐⭐    |
| APIs                  | ⭐⭐⭐⭐⭐    |
| Boto3                 | ⭐⭐⭐⭐⭐    |
| OOP                   | ⭐⭐⭐      |
| Advanced DSA          | ⭐        |

---

# 📌 Learning Path

```text
Python Basics
      ↓
Data Structures
      ↓
Functions
      ↓
File Handling
      ↓
Exception Handling
      ↓
OS & System Modules
      ↓
Shell Command Automation
      ↓
JSON
      ↓
REST APIs
      ↓
Boto3
      ↓
AWS Automation
      ↓
DevOps Automation Projects
```

## 🎯 Goal

By completing this section, I should be able to use Python to:

* Automate repetitive tasks
* Execute system commands
* Work with files and logs
* Interact with APIs
* Work with JSON
* Manage environment variables
* Automate AWS resources
* Build basic DevOps automation scripts
