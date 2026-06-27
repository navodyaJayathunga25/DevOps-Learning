# 📘 EC2 Provisioning Methods

> Learn the different ways to create and manage Amazon EC2 instances.

---

# Why Automation?

Imagine a company needs to create **100 EC2 instances**.

### Manual Approach

Using the AWS Console:

- Open AWS Console
- Launch EC2
- Configure settings
- Click Launch

Doing this **100 times** is:

- Time-consuming
- Error-prone
- Not scalable

This is why automation is important.

---

# Multiple Ways to Create an EC2 Instance

```text
AWS Console
      │
      ▼
AWS CLI
      │
      ▼
Python (Boto3)
      │
      ▼
CloudFormation
      │
      ▼
Terraform
      │
      ▼
AWS CDK
```

All of these methods eventually communicate with the **AWS API**.

---

# 1. AWS Console

The AWS Console is the web-based graphical interface provided by AWS.

### Best For

- Beginners
- Learning AWS services
- Manual resource creation

### Advantages

- Easy to use
- No coding required

### Disadvantages

- Manual process
- Difficult to repeat many times

---

# 2. AWS API

AWS provides APIs for every AWS service.

Examples:

- EC2 API
- S3 API
- IAM API
- EBS API

The API receives requests and performs actions such as:

- Create EC2
- Delete EC2
- Create S3 Bucket
- Stop Instances

Think of the AWS API as the communication layer between your tools and AWS.

---

# 3. AWS CLI

AWS CLI allows you to communicate with AWS using terminal commands.

Example:

```bash
aws ec2 run-instances \
    --image-id ami-xxxxxxxx \
    --instance-type t2.micro
```

Instead of clicking buttons, you execute commands.

---

# 4. Python (Boto3)

Boto3 is the official AWS SDK for Python.

Instead of typing CLI commands, you write Python code.

Example:

```python
import boto3

ec2 = boto3.client("ec2")

ec2.run_instances(
    ImageId="ami-xxxxxxxx",
    InstanceType="t2.micro",
    MinCount=1,
    MaxCount=1
)
```

### How it works

```text
Python
   │
   ▼
Boto3
   │
   ▼
AWS API
   │
   ▼
EC2 Instance
```

---

# 5. AWS CloudFormation

CloudFormation is AWS's Infrastructure as Code (IaC) service.

Infrastructure is defined in:

- YAML
- JSON

Example:

```yaml
Resources:
  MyEC2:
    Type: AWS::EC2::Instance
```

CloudFormation creates AWS resources automatically from the template.

---

# 6. Terraform

Terraform is an open-source Infrastructure as Code tool developed by HashiCorp.

It uses:

- HCL (HashiCorp Configuration Language)

Example:

```terraform
resource "aws_instance" "web" {
  ami           = "ami-xxxxxxxx"
  instance_type = "t2.micro"
}
```

Unlike CloudFormation, Terraform works with:

- AWS
- Azure
- Google Cloud
- Kubernetes
- GitHub
- Many other providers

---

# 7. AWS CDK

AWS Cloud Development Kit (CDK) allows you to define infrastructure using programming languages.

Supported languages:

- TypeScript
- Python
- Java
- C#
- Go

Example:

```python
ec2.Instance(
    self,
    "MyInstance",
    instance_type=ec2.InstanceType("t2.micro")
)
```

The CDK automatically generates CloudFormation templates and deploys them.

```text
Your Code
      │
      ▼
AWS CDK
      │
      ▼
CloudFormation
      │
      ▼
AWS API
      │
      ▼
EC2 Instance
```

---

# Comparison

| Method | Coding Required | Automation | Best For |
|---------|----------------|------------|----------|
| AWS Console | ❌ | ❌ | Beginners |
| AWS CLI | Basic Commands | ✅ | Quick automation |
| Python (Boto3) | Python | ✅ | Application development |
| CloudFormation | YAML/JSON | ✅ | AWS Infrastructure as Code |
| Terraform | HCL | ✅ | Multi-cloud Infrastructure |
| AWS CDK | Programming Language | ✅ | Developers |

---

# Key Takeaways

- AWS Console is used for manual resource creation.
- AWS API is the backend interface used by all AWS tools.
- AWS CLI automates AWS using terminal commands.
- Boto3 allows Python applications to communicate with AWS.
- CloudFormation defines AWS infrastructure using YAML or JSON.
- Terraform is a multi-cloud Infrastructure as Code tool.
- AWS CDK allows infrastructure to be created using programming languages.

---

# Interview Questions

### What is the AWS API?

The AWS API is the backend interface that receives requests from tools like the AWS Console, CLI, Boto3, Terraform, CloudFormation, and CDK to manage AWS resources.

---

### What is Boto3?

Boto3 is the official AWS SDK for Python that allows Python applications to interact with AWS services through the AWS API.

---

### What is the difference between CloudFormation and Terraform?

CloudFormation is AWS-native and uses YAML/JSON templates, while Terraform is cloud-independent and uses HCL to provision infrastructure across multiple cloud providers.

---

### What is the AWS CDK?

AWS CDK is an Infrastructure as Code framework that allows developers to define cloud infrastructure using programming languages like Python and TypeScript. It generates CloudFormation templates automatically.
