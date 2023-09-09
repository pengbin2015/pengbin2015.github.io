---
title: Infrastructure as Code Tools
description: >-
  If you’re involved in DevOps, you should be acquainted with Infrastructure as
  Code (IaC). IaC allows you to write code to define, deploy…
date: '2023-08-21T03:47:03.099Z'
categories: []
keywords: []
slug: /@pengbintech/infrastructure-as-code-tools-726fc4a38237
---

If you’re involved in DevOps, you should be acquainted with Infrastructure as Code (IaC). IaC allows you to write code to define, deploy, update, and dismantle IT infrastructure, rather than manually performing these tasks.

There are numerous tools designed to aid in IaC. These can be grouped into five categories:

*   Ad hoc scripts
*   Configuration management tools
*   Server templating tools
*   Orchestration tools
*   Provisioning tools

#### Ad hoc scripts

Ad hoc scripts are a straightforward method for automating tasks or configuring tools. These can be written in any scripting language (e.g., Bash, Perl, Python, Ruby).

For instance, the following Bash script creates and configures a web server:

#!/bin/bash  
yum update -y  
yum install -y httpd php  
systemctl start httpd  
systemctl enable httpd  
usermod -a -G apache ec2-user  
chown -R ec2-user:apache /var/www  
chmod 2775 /var/www  
find /var/www -type d -exec chmod 2775 {} \\;  
find /var/www -type f -exec chmod 0664 {} \\;  
echo "<?php phpinfo(); ?>" > /var/www/html/phpinfo.php

While ad hoc scripts are useful for small, one-off tasks, they can become. unwieldy when maintaining a large repository of scripts to manage your entire infrastructure.

#### Configuration Management Tools

Configuration management tools are purposely created to install and manage software on existing servers. Common configuration management tools include Chef, Puppet, Ansible, and SaltStack.

Compared to ad hoc scripts, configuration management tools offer advantages like:

*   Consistent coding conventions for readability.
*   Idempotent code that works correctly regardless of how many times it’s run.
*   Ability to manage large numbers of remote servers seamlessly.

For example, here is an Ansible YAML file that configures a web server:

\- name: Update the packages  
  apt:  
     update\_cache: yes  
  
\- name: install PHP  
  apt:  
     name: php  
  
\- name: install web server  
  apt:  
     name: apache2  
  
\- name: start web server  
  service: name=apache2 state=started enabled=yes

#### Server Templating Tools

Though configuration management tools provide advantages, they can cause configuration drift issues. Server templating tools, like Docker, Packer, and Vagrant, address these problems by adopting an immutable infrastructure approach. This means that once a server is deployed, no changes are made to it. Any required changes lead to the creation and deployment of a new image on a new server.

For instance, here is a Packer template for an Amazon Machine Image (AMI):

{  
  "builders": \[{  
    "ami\_name": "packer-image",  
    "instance\_type": "t2-micro",  
    "region": "us-east-2",  
    "type": "amazon-ebs",  
    "source\_ami": "ami-55c324223gf0",  
    "ssh\_username": "ubuntu"  
  }\],  
  "provisioners": \[{  
    "type": "shell",  
    "inline": \[  
      "sudo apt-get update",  
      "sudo apt-get install -y php apache2",  
    \],  
    "environment\_vars": \[  
      "DEBIAN\_FRONTEND=noninteractive"  
    \]  
  }\]  
}

#### Orchestration Tools

While server templating tools are excellent for creating VM and container images, they lack mechanisms to manage them. For example, how to deploy VMs and containers on a large number of servers, how to monitor the health of the VMS and containers and automatically replace unhealthy ones, and so on.

Therefore, orchestration tools like Kubernetes, Marathon/Mesos, Docker Swarm, Nomad, and Amazon ECS are designed to handle these tasks. The popular orchestration tools include Kubernetes, Marathon/Mesos, Docker Swarm, Nomad, and Amazon ECS. Most major cloud providers have native support for deploying managed Kubernetes clusters, such as Amazon EKS, Google GKE, and Azure AKS.

#### Provisioning Tools

Provisioning tools go beyond defining code and configuration that runs on each server; they are responsible for creating the actual servers and other aspects of infrastructure in the cloud. Examples include Terraform, CloudFormation, and OpenStack Heat.

Here’s an example code to deploy a web server using Terraform:

resource "aws\_instance" "webserver" {  
  instance\_type = "t2.micro"  
  availability\_zone = "us-east-2a"  
  ami = "ami-0c55b159cbfafeif0"  
    
  user-data = <<-EOF  
              #!/bin/bash  
              sudo service apache2 start  
              EOF  
}

With these IaC tools, organizations can significantly enhance the software delivery process and manage infrastructure with a smaller team of engineers.