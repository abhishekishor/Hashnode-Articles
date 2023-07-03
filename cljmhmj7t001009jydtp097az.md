---
title: "Terraform Introduction: Workflow"
seoTitle: "Mastering Terraform: Streamlined Workflow"
seoDescription: "Discover the best practices and step-by-step guide to optimize your Terraform workflow. Streamline infrastructure provisioning and management effortlessly."
datePublished: Mon Jul 03 2023 06:36:11 GMT+0000 (Coordinated Universal Time)
cuid: cljmhmj7t001009jydtp097az
slug: terraform-introduction-workflow
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1688365926973/0cf7210a-c663-490f-937f-4ffd7cecc387.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1688365977752/5e2bc0eb-b626-498a-a7fd-69906c0adafb.jpeg
tags: devops, infrastructure, terraform, infrastructure-as-code, devops-articles

---

# **Introduction**

To provision any infrastructure using Terraform on any of the cloud providers or on-premise infrastructures, whatever Terraform supports we need to follow the five core commands known as **Terraform Workflow**.

The five commands used in Terraform Workflow are:

1. Terraform Init
    
2. Terraform Validate
    
3. Terraform Plan
    
4. Terraform Apply
    
5. Terraform Destroy
    

# ⚙️ Terraform Init

`terraform init` is the first command we need to use whenever we create the Terraform configuration files. It initializes a new or existing Terraform configuration. It sets up the environment, and downloads necessary provider plugins which are configured in the respective configuration files. And it prepares the working directory for Terraform operations.

We need to do Initialization in the working folder where configuration files are present.

**Directory Initialization**: In the working directory, where the Terraform configuration files are located, run the command "terraform init" in the terminal or command prompt.

**Provider Plugin Download**: Terraform will automatically download the necessary provider plugins specified in the configuration files. Providers are responsible for interacting with specific cloud platforms, such as AWS, Azure, or Google Cloud Platform. The providers are typically defined in the "provider" block in the configuration files.

**Module Installation (Optional)**: If the configuration uses external Terraform modules, then "`terraform init`" will download and install those modules. Modules are reusable components that encapsulate a set of resources and configurations. They can be used to share infrastructure code and simplify complex deployments.

**Initialization Complete**: Once the initialization process is complete, it’ll report the successful completion of the initialization process and then Terraform is ready to perform other operations like "terraform plan" or "terraform apply" on our infrastructure code.

It's an essential first step in the Terraform workflow to establish the necessary dependencies and prepare for subsequent operations.

**Note:** During subsequent Terraform runs, you won't need to repeat the "`terraform init`" step unless there are changes to providers or modules. Instead, you can directly use other Terraform commands like "terraform plan" or "terraform apply" to manage your infrastructure.

# ⚙️ Terraform Validate

**terraform validate** is the command used in the Terraform Workflow to validate the **Terraform configuration** files present in the respective directory to ensure they're syntactically valid and internally consistent.

It checks for any errors or issues in the code without actually making any changes to the infrastructure.

So once, whatever the configuration files we’ll write, we can set **terraform validate** to validate that.

## *🏷️ Terraform Validate Workflow*

1. **Directory Preparation**: Make sure, we are in the directory where your Terraform configuration files are located.
    
2. Run "`terraform validate`" in the terminal or command prompt.
    
3. **Syntax and Configuration Validation**: Terraform will analyze the configuration files and validate the syntax and structure against the Terraform language and provider requirements. It checks for proper syntax, resource and variable references, and valid provider configurations.
    
4. **Error Reporting**: If there are any syntax errors or configuration issues in the code, Terraform will report them in the terminal, providing details about the problem and the affected file and line number.
    
    Based on this error message, we can identify the syntax issue and fix it in the affected file.
    
    This step helps us to prevent potential issues and ensures a smoother execution of subsequent Terraform commands like "`terraform plan`" or "`terraform apply`".
    

# ⚙️ Terraform Plan

After validating the Syntax, we can generate an execution plan.

Terraform Plan is the Terraform workflow that allows users to preview the changes that Terraform will make to their infrastructure. It analyzes the configuration files, compares the desired state with the current state, and provides a detailed execution plan without actually making any changes.

## *🏷️ Terraform Plan Workflow*

1. **Directory Preparation**: Make sure we are inside the directory where the Terraform configuration files are located.
    
2. Run "`terraform plan`" in the terminal or command prompt.
    
3. **Configuration Analysis**: Terraform will read the configuration files and analyze them to determine the current state of the infrastructure.
    
4. **Dependency Graph Construction**: Terraform will construct a dependency graph based on the resource relationships defined in the configuration. This graph helps Terraform understand the order in which resources need to be created, updated, or destroyed.
    
5. **Desired State Comparison**: Terraform will compare the current state of your infrastructure (obtained from the Terraform state file) with the desired state defined in the configuration files. It identifies any differences or changes required to align the current state with the desired state.
    
6. **Execution Plan Generation**: Terraform generates a detailed execution plan that outlines the actions it will take to reach the desired state. The plan includes information about resource creation, modification, or destruction. It also provides insights into any potential risks or side effects.
    
7. **Plan Output**: The "`terraform plan`" command displays the execution plan in the terminal, listing the resources to be added, modified, or destroyed. It also shows any changes in attributes or configuration for existing resources.
    

Ex:

**COPY**

**COPY**

```json
Plan: 1 to add, 0 to change, 0 to destroy.


Changes to be performed:
  # aws_s3_bucket.example will be created
  + resource "aws_s3_bucket" "example" {
      + acl                      = "private"
      + arn                      = (known after apply)
      + bucket                   = "my-example-bucket"
      + force_destroy            = false
      + id                       = (known after apply)
      + region                   = "us-west-2"
      + request_payer            = (known after apply)
      + tags                     = (known after apply)
      + website_domain           = (known after apply)
      + website_endpoint         = (known after apply)
    }
```

It highlights the attributes that will be set and provides information about any unknown values that will be determined after applying the changes.

This step provides an additional layer of safety and allows us to make informed decisions about the modifications to be made.

# ⚙️ Terraform Apply

`terraform apply` command applies the changes defined in the Terraform configuration to the infrastructure. It creates, modifies, or destroys resources based on the execution plan generated by "`terraform plan`".

## *🏷️ Terraform Apply Workflow*

1. **Directory Preparation**: Make sure we are in the directory where the Terraform configuration files are located.
    
2. Run "terraform apply" in the terminal or command prompt.
    
3. **Configuration Loading**: Terraform loads the configuration files and initializes the necessary providers and modules.
    
4. **Execution Plan Review**: Terraform displays the execution plan, listing the changes it will make to the infrastructure. Review the plan carefully to ensure it aligns with the intentions. If we haven't run "`terraform plan`" yet, Terraform will generate a new plan for us before applying changes.
    
5. **Confirmation Prompt**: Terraform will prompt us to confirm whether we want to proceed with the planned changes. Enter "yes" to continue or "no" to cancel the operation.
    
6. **Resource Provisioning**: If we confirm the changes, Terraform begins provisioning resources according to the execution plan. It creates new resources, modifies existing resources, or destroys resources as needed.
    
7. **Status Updates**: Terraform provides real-time updates on the progress of resource provisioning. It shows the status of each resource being created, modified, or destroyed.
    
8. **Output Values**: After successfully applying the changes, Terraform may display any output values defined in your configuration. These values can be useful for obtaining information about the provisioned resources, such as IP addresses or DNS names.
    

This workflow empowers us to manage and evolve our infrastructure in a controlled and repeatable manner.

# ⚙️ Terraform Destroy

The `terraform destroy` command allows to gracefully tear down and remove all resources created by Terraform configuration. It reverses the changes made to the infrastructure and cleans up the provisioned resources.

## *🏷️ Terraform Destroy Workflow*

1. **Directory Preparation**: Make sure we are in the directory where our Terraform configuration files are located.
    
2. Run "`terraform destroy`" in the terminal or command prompt.
    
3. **Configuration Loading**: Terraform loads the configuration files and initializes the necessary providers.
    
4. **Execution Plan Generation**: Terraform generates a destruction plan that outlines all the resources to be destroyed.
    
5. **Confirmation Prompt**: Terraform will prompt us to confirm whether we want to proceed with the destruction of resources. Enter "yes" to continue or "no" to cancel the operation.
    
6. **Resource Destruction**: If we confirm the destruction, Terraform begins tearing down the resources specified in the destruction plan. It destroys the resources in the reverse order of their dependency graph.
    
7. **Status Updates**: Terraform provides real-time updates on the progress of resource destruction. It shows the status of each resource being destroyed.
    
8. **Cleanup Complete**: Once the destruction process is complete, Terraform will display a summary of the resources destroyed and any associated cleanup actions performed.
    

This workflow provides us control over the lifecycle of our infrastructure and ensures that we can easily clean up resources when they are no longer needed, avoiding unnecessary costs and clutter in your cloud environment.