---
title: "Terraform Introduction"
seoTitle: "Terraform Introduction: Complete Guide"
seoDescription: "Get a comprehensive guide to Terraform with our introduction article. Learn about its history, architecture, and the drawbacks of traditional methods."
datePublished: Wed Jun 28 2023 07:49:05 GMT+0000 (Coordinated Universal Time)
cuid: cljff11i8000709ic0f2c8uhc
slug: terraform-introduction
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1687938385440/4a034fac-7b7b-42dd-94eb-9a110bf92407.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1687938501679/b9bac909-9fc2-4652-ae3e-315242b2fe4a.jpeg
tags: devops, terraform, infrastructure-as-code, devops-articles

---

# *⚙️ Introduction*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687851463214/e45748c1-82fc-4d67-87d2-fe7f863d4a52.jpeg align="center")

Terraform is an open-source **infrastructure as code (IaC)** tool developed by **HashiCorp** that helps you manage your infrastructure (servers, networks, databases, etc.) using code instead of manually setting them up. Think of it as using a programming language to define and control your infrastructure.

It allows you to define and manage your infrastructure using a declarative configuration language. This means, Terraform provides a language that allows us to describe the desired state of our infrastructure without worrying about the specific steps to achieve that state.

Instead of writing procedural code, we write declarations of what resources we want and how they should be configured.

Terraform is compatible with different cloud providers, meaning you can use it to create and manage resources in providers like Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), and others.

It provides a consistent way to work with multiple cloud platforms, making it easier to switch or use a combination of different providers.

# *⚙️ Traditional Methods To Manage Infrastructure Of Cloud*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687852879062/63fe287b-b528-4e61-8339-f594adf5532f.jpeg align="center")

Before the advent of tools like Terraform, managing cloud infrastructure was often done using traditional methods that involved manual provisioning and configuration.

1. **Manual Provisioning**: In this approach, each component of the infrastructure, such as virtual machines, storage, and networking, had to be manually provisioned through the cloud provider's management console or command-line interface.
    
    For example, if we wanted to create a virtual machine, we would log in to the cloud console, select the desired settings, and create the instance.
    
2. **Configuration Management Tools**: Traditional methods often relied on configuration management tools like **Chef**, **Puppet**, or **Ansible**. These tools helped in automating the installation, configuration, and management of software on cloud instances. With these tools, system administrators could define the desired state of their infrastructure and apply those configurations to multiple instances simultaneously.
    
    For example, Ansible playbooks could be used to install and configure web servers across multiple virtual machines.
    
3. **Scripts and Shell Commands**: Infrastructure management also involved writing scripts and executing shell commands to perform specific tasks.
    
    For example, Bash or PowerShell scripts could be used to automate the setup of networking rules, security groups, or load balancers.
    
4. **Custom Automation Scripts**: System administrators often wrote custom scripts using programming languages like Python or Ruby to manage cloud resources. These scripts interacted with the cloud provider's API to create, modify, or delete resources.
    
    For instance, a Python script could be written to automatically scale up or down the number of instances based on resource utilization metrics.
    
5. **Configuration Files**: Infrastructure configuration files, such as XML, YAML, or JSON, were commonly used to define the desired state of resources. These files contained detailed information about the infrastructure components, their dependencies, and configurations.
    
    Examples include creating a load balancer and defining its listeners, target groups, and routing rules.
    
6. **Manual Tracking and Documentation**: Keeping track of changes made to the infrastructure was crucial. System administrators often relied on spreadsheets, wikis, or other documentation methods to record and maintain an inventory of infrastructure resources and their configurations. This manual tracking was error-prone and challenging to maintain as the infrastructure scaled.
    

## 🏷️ Problems With Traditional Methods

While these traditional methods provided some level of automation, they lacked the declarative and infrastructure-as-code capabilities offered by tools like Terraform. With Terraform, we can define our infrastructure as code using a **domain-specific language (DSL)**, and the tool takes care of provisioning and managing the infrastructure in a consistent and reproducible manner.

Terraform simplifies the management of cloud infrastructure by providing a unified workflow for provisioning and updating resources across multiple cloud providers. It allows us to define your infrastructure in a declarative manner, enabling version control, collaboration, and automated deployments.

Using traditional methods to manage cloud infrastructure before the advent of tools like Terraform posed several challenges and limitations.

1. **Manual Provisioning Errors**: Manual provisioning of cloud resources often led to human errors. Mistakes in configuration settings, security rules, or dependencies could cause infrastructure instability, security vulnerabilities, or inconsistent environments.
    
    For example, misconfiguring a Security Group could result in unintended access to sensitive resources.
    
2. **Lack of Scalability**: Scaling infrastructure using traditional methods required repetitive manual effort. As the infrastructure grew or needed to be modified, administrators had to manually provision and configure each component individually. This process was time-consuming, error-prone, and limited the ability to quickly scale resources in response to changing demands.
    
3. **Configuration Drift**: With traditional methods, it was challenging to maintain consistent configurations across the infrastructure. As changes were made manually or through scripts, it was difficult to track and enforce the desired state of resources. Configuration drift occurred when resources deviated from their intended configurations over time, leading to inconsistencies and potential issues.
    
4. **Limited Collaboration and Version Control**: Traditional methods lacked proper collaboration and version control capabilities. Multiple administrators working on the same infrastructure could face difficulties in coordinating their changes. Additionally, tracking and managing changes over time, especially in large and complex environments, became a cumbersome task without proper version control mechanisms.
    
5. **Lack of Infrastructure as Code**: Traditional methods relied heavily on manual interventions, scripts, or configuration management tools. While these methods provided some level of automation, they did not offer a standardized and declarative approach to define and manage infrastructure as code. Infrastructure definitions were often fragmented, and spread across various scripts or configuration files, making it harder to maintain and reproduce environments consistently.
    
6. **Vendor Lock-in and Portability**: Each cloud provider had its own set of APIs, CLI commands, and management consoles, making it challenging to switch between providers or maintain multi-cloud environments. Traditional methods lacked the portability and flexibility needed to manage infrastructure across different cloud platforms seamlessly.
    

# *⚙️ History*

![Hemlington Hall Academy | history-clipart](https://www.hemlingtonhallacademy.co.uk/wp-content/uploads/2018/10/history-clipart.jpg align="center")

Before the advent of Terraform, managing infrastructure resources was typically a manual and time-consuming process.

In the early days of infrastructure management, system administrators and operations teams had to manually provision and configure resources. This involved tasks such as setting up servers, networking components, storage, and various software dependencies. These tasks were often performed through a combination of manual steps, scripts, and configuration files specific to each infrastructure provider.

As organizations started adopting cloud computing, the complexity of managing infrastructure increased significantly. Cloud platforms like AWS, Azure, and Google Cloud provided APIs and command-line interfaces (CLIs) for provisioning resources, but the process still required writing scripts and executing them to achieve the desired infrastructure state. This approach was error-prone, time-consuming, and lacked standardization.

In 2011 AWS introduced **Cloudformation** and the very next day he wrote a blog post and posted it on **Tumblr** (a Social Media platform to express yourself) of all things saying how impressed he was with that idea, but what he thought that people needed a tool that supported more than just aws resources i.e. a general infrastructure as code tool and the best way to do that was through the power of an **open source**

ecosystem. So in that blog post, he invited anyone to solve this problem and gave the idea for terraforming away.

A few years passed and that request he made in the blog post remained unanswered meanwhile the challenges that he posted in that blog post became very real for him personally and he needed a solution, so he and his team at Hashicorp decided to solve it themselves and in July 2014, they released **terraform 0.1**, an open source cloud-agnostic infrastructure's code solution, basically the same idea that he presented in that blog post back in 2011. Terraform 0.1 supported only **AWS** and **Digitalocean**. The idea was just to start here and just show how Terraform could support multiple providers and focus on expanding that in the future.

They designed a configuration language called **HashiCorp Configuration Language (HCL)**, which provided a human-readable and expressive syntax for defining infrastructure resources and their dependencies.

Over time, Terraform evolved to support more advanced features, including the ability to manage complex network topologies, load balancers, databases, and other infrastructure components. The tool became an essential part of the infrastructure management toolkit, allowing organizations to embrace the principles of infrastructure as code and reap the benefits of automation and scalability.

## 🏷️ Why The Word “Terraform”?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687809379700/f5931aed-8136-430a-a3dc-6ae68c81b7a9.png align="center")

The term "terraform" has its roots in science fiction and refers to the process of transforming or shaping a planet or environment to make it suitable for human habitation. In the context of the infrastructure as a code tool developed by HashiCorp, "Terraform" represents the idea of transforming and configuring your infrastructure resources using code.

In this context, Terraform allows us to define and manage infrastructure as code, providing a way to describe the desired infrastructure state in a configuration file. By leveraging Terraform's configuration language, we can specify the resources, their properties, and their relationships in a **human-readable format**.

# *⚙️ Why Terraform Is Better Than CloudFormation*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1687809556081/19b2573c-ede4-45ea-8e92-97deba143f02.png align="center")

Terraform and AWS CloudFormation are both infrastructure-as-code tools used for provisioning and managing cloud resources. While they serve similar purposes, Terraform offers several advantages over CloudFormation.

1. **Multi-Cloud Support**: Terraform supports provisioning and managing resources across multiple cloud providers, such as AWS, Azure, Google Cloud Platform, and more. This flexibility allows you to work with different cloud providers using a consistent workflow. In contrast, CloudFormation is specific to AWS and doesn't offer native support for other providers.
    
    Example: Let's say we start with provisioning resources on AWS using Terraform, but later you decide to incorporate Azure services into your infrastructure. With Terraform, we can easily extend our existing configuration to include Azure resources, leveraging the multi-cloud capabilities. This flexibility enables us to adopt a multi-cloud or hybrid cloud strategy as our needs evolve.
    
2. **Declarative Language**: Terraform uses a declarative language called HashiCorp Configuration Language (HCL) to define infrastructure. HCL provides a simple and readable syntax for expressing resources and their dependencies. In comparison, CloudFormation uses JSON or YAML, which can be more verbose and harder to read and understand, especially for beginners and it can be more lengthy and complex.
    
3. **Modular and Reusable Configurations**: Terraform encourages creating modular configurations using reusable modules. Modules encapsulate a set of resources and their configurations, making it easy to reuse them across different projects. This modularity reduces duplication, promotes code reusability, and simplifies the management of complex infrastructure.
    
    Example: Imagine we have a module that defines a load balancer configuration. We can reuse that module in multiple projects by simply referencing it in the respective Terraform code. This reusability saves time and effort, improves consistency, and simplifies updates across different environments. CloudFormation has a similar concept called "nested stacks," but managing dependencies and sharing modules is generally considered more straightforward in Terraform.
    
4. **State Management**: Terraform maintains the state of our infrastructure in a state file, which is used to understand the current state and manage changes. The state file provides essential features like tracking resource dependencies, detecting drifts and enabling collaborative work. It also offers state locking to prevent concurrent modifications and conflicts when working in a team.
    
    Example: Let's say we initially provision a set of resources using Terraform. Later, we modified our configuration to add more resources. Terraform compares the current state with the desired state and determines the necessary changes to achieve the desired configuration. This tracking and comparison are essential for maintaining consistency and managing infrastructure changes over time.
    
5. **Community and Ecosystem**: Terraform has a vibrant community and a vast ecosystem. It provides a wide range of community-maintained modules, plugins, and providers. The Terraform Registry serves as a central repository for sharing and discovering modules, which accelerates development and reduces the need to start from scratch. While CloudFormation also has its own set of resources and plugins, Terraform's ecosystem is known for its diversity and extensive support.
    
    Example: If anyone is looking to deploy a specific application stack, chances are there's already a Terraform module available in the registry. They can leverage these pre-built modules to save time and benefit from the expertise of the community. This ecosystem makes Terraform a powerful tool for infrastructure management, especially for beginners who can rely on community contributions.
    

# *⚙️ Terraform Architecture*

![](https://lh4.googleusercontent.com/5bv7d501LuzxXjXnbq-j2WhJFn81EaLVqtKTftxHtNeo8e3-5-dpu1o3yxDhQEwmvkkVwa3V1bNP6lXEsg31PjFYz3yjMLgKGWkNhpHyOCwHhbl_QXEsCZvJiMgAWdFtF_6nZ9XkUI_5xJJvdf-K8Mg align="left")

**Terraform** follows a **Client-Server** Architecture where multiple components interact to provision and manage infrastructure.

Terraform operates with a **distributed system design** where different components collaborate to facilitate infrastructure provisioning and management.

Terraform's architecture is composed of two main components: **Terraform Core** and **Providers**.

## 🏷️ Terraform Core

**Terraform Core** is the heart of Terraform. It is responsible for reading and parsing configuration files, building dependency graphs, and communicating with providers. Terraform Core is written in the Go programming language and is available as a binary for Linux, macOS, and Windows.

Core uses two input sources in order to do its job. It takes **terraform configuration** that we as a user write and where we define what needs to be created or provisioned. The second is **State** where Terraform keeps the up-to-date state of how the current set up of the infrastructure

looks like.

Then Core takes the input, and it figures out the **Plan** of what needs to be done; So it compares the **State** what is the current state, what is the configuration that you desire, the end result and compares that, and when it sees there is a difference i.e we want something else than what the current state is, it figures out what needs to be done to get to that desired state in the configuration file, i.e what needs to be created, what needs to be updated or deleted or in which order on that infrastructure setup.

## 🏷️ Providers

**Providers** are plugins that extend Terraform's capabilities to support different cloud providers and infrastructure services. Providers are written in the Go programming language and are available as open-source or commercial offerings.

Providers for specific technologies can be cloud providers like AWS, Azure, GCP or other infrastructure-as-a-service platforms for the

infrastructure-level tasks, but Terraform is also a provider for more high-level components like Kubernetes or other **platform-as-a-service tools**, even some software is a **self-service tool**. So it gives us the possibility to create stuff on different levels like creating a AWS infrastructure then deploying or creating Kubernetes on top of it and then creating services inside that or components inside that Kubernetes cluster.

Each provider then gives Terraform user access to its resources. Like, through an AWS provider, we can have access to hundreds of AWS resources like **EC2 instances**, **AWS users** etc. With Kubernetes provider, we can access commodities resources like **services**, **deployments** and **namespaces** etc

In addition to Terraform Core and Providers, Terraform also uses several other components, including:

## 🏷️ Terraform CLI

In the architecture, the client component refers to the **Terraform CLI** tool that users interact with. It acts as the front-end interface, allowing users to issue commands and define infrastructure configurations. For example, users can run commands like **terraform apply** or **terraform plan** to provision or preview changes to the infrastructure.

* The primary tool used to interact with Terraform.
    
* Allows users to write and execute Terraform commands to create, modify, and destroy infrastructure.
    
* Reads and interprets Terraform configuration files.
    

Example: Running the command **terraform init** initializes a new Terraform project by downloading provider plugins and setting up the backend.

On the server side, multiple components work together:

## 🏷️ Terraform Configuration

* Written in HashiCorp Configuration Language (HCL) or JSON.
    
* Describes the desired infrastructure state, resource dependencies, and configuration values.
    
* Defines providers, resources, variables, outputs, and modules.
    

Example:  A configuration file might specify the creation of an AWS EC2 instance with specific attributes like instance type, security groups, and tags.

## 🏷️ Terraform State

* Stores the current state of deployed infrastructure.
    
* Records the mapping between resources defined in the configuration and their real-world counterparts.
    
* Helps Terraform track changes and manage updates incrementally.
    
* Can be stored locally or in a remote backend for collaboration and state consistency.
    

Example:

After applying a Terraform configuration, the state file records the created resources and their attributes, such as the resource IDs and the last-known state.

## 🏷️ Terraform Providers

* Interfaces with various infrastructure platforms (e.g., AWS, Azure, GCP) or services (e.g., Docker, Kubernetes).
    
* Each provider communicates with the respective platform's API to create, modify, and destroy resources.
    
* Manages authentication and resource lifecycle.
    

Example: The AWS provider communicates with the AWS API to create and manage AWS resources, such as EC2 instances, S3 buckets, or VPCs.

## 🏷️ Terraform Modules

* Encapsulates reusable infrastructure components.
    
* Comprises one or more resources, variables, and outputs.
    
* Supports composition and abstraction to promote code reuse and maintainability.
    
* Can be shared internally or publicly through module registries.
    

Example: A module can define a standardized AWS VPC configuration that can be reused across different projects.

## 🏷️ Terraform Backend

* Determines how Terraform state is stored and accessed.
    
* Supports local file storage, as well as remote backends like Amazon S3, HashiCorp Consul, or Terraform Cloud.
    
* Enables collaboration, version control, and sharing of state between team members.
    

## 🏷️ Remote Execution

Terraform supports remote execution modes using remote backends or Terraform Cloud.

Example: Leveraging a remote backend, multiple team members can collaborate on a shared infrastructure project, executing Terraform commands from their local environments.

# *⚙️ How Terraform Works*

When we run Terraform, it will read the configuration file and create an execution plan. The plan will show what resources Terraform will create or modify to match the desired state. If we decide to proceed, Terraform will make the necessary API calls to AWS to provision the EC2 instance.

This way, we can use Terraform to manage our infrastructure across different cloud providers by defining the desired state in code and letting Terraform handle the provisioning and configuration for us.