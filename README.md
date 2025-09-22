Deploying Secure EC2 Instances with a Shared RDS Database

In this project, we navigate the process of deploying secure EC2 instances connected to a shared database on AWS using Terraform. We covered the setup of a Virtual Private Cloud (VPC), Elastic Compute Cloud (EC2) instances and a Relational Database Service (RDS) instance. Our focus is always be on adhering to best practices for security, scalability, and maintainability.

Building the Infrastructure

Our web application will need a VPC, EC2 instances, and an RDS instance. We need to define each of these components in respective terraform configuration file.

Virtual Private Cloud (VPC)

A VPC is a virtual network dedicated to your AWS account. It is isolated from other virtual networks in the AWS cloud.

Subnets

Within the VPC, we create subnets. Each subnet resides in a different availability zone for high availability.

Security Groups

Security groups act as a virtual firewall for our instances to control inbound and outbound traffic.

Elastic Compute Cloud (EC2)

EC2 instances will host our web application. We will create an instance within our VPC and associate it with the security group we defined.

Relational Database Service (RDS)

For data persistence, we will set up an RDS instance. It's managed by AWS, which simplifies database administration tasks such as backups and patching.

Deploying AWS Infrastructure

With all components defined, we can now deploy our infrastructure using simple terraform workflow

1. terraform init initializes the Terraform configuration, preparing our working directory for other commands.
2. terraform plan creates an execution plan, allowing us to review the changes Terraform will make to our infrastructure.
3. terraform apply applies the changes to create the defined resources.
