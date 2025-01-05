# Serverless-Framework-and-Terraform-as-tools-for-IaC

## Make a comparison between Serverless Framework and Terraform as tools for IaC. Answer the following:
### What type of infrastructure and application deployments are each tool best suited for?
* **Serverless Framework:** Tailored specifically for deploying serverless applications, it abstracts much of the underlying infrastructure, allowing developers to focus on writing and deploying functions and event-driven services. Ideal for projects primarily utilizing serverless services, where rapid development and deployment of functions are paramount. It excels in managing application-specific infrastructure components.
* **Terraform:** A general-purpose IaC tool capable of managing a broad spectrum of infrastructure resources and is best suited for managing comprehensive infrastructure environments, including both serverless and traditional resources. It's particularly effective for organizations requiring consistent infrastructure management across multiple services and providers.
### How do their primary objectives differ?
* **Serverless Framework:** Designed specifically for developing, deploying, and managing serverless applications. Allows developers to quickly build and deploy applications without having to worry about the unerlying infrasturcture.
* **Terraform:** General-purpose IaC tool for defining, deploying, and managing all types of infrastructure resources. Allows operations teams to manage and deploy comprehensive infrastructure environments consistently and at scale.
### How do they differ in terms of learning curve and ease of use for developers or DevOps teams?
* **Serverless Framework:**
  * Tailored for application developers working on serverless architectures.
  * Abstracts infrastructure complexities, focusing on deploying and managing serverless functions.
  * Configuration by intuitive YAML file.
  * Templates and plugins for common serverless scenarios available.
  * Limited need for understanding underlying infrastructure.
  * Low learning curvefor developers familiar with serverless applications.
* **Terraform:** 
  * Aimed at DevOps engineers and teams responsible for provisioning and managing infrastructure across providers.
  * Requires understanding of cloud resources, networking, and configuration dependencies.
  * Based on the HashiCorp Configuration Language designed for infrastructure automation which is a declarative IaC language but requires understanding dependencies and resource lifecycles.
  * Steeper for those new to Infrastructure as Code or cloud architecture.
  * Requires knowledge of cloud provider services, networking, permission policies and state management.
### What are the differences in how each tool handles state tracking and deployment changes?
* **Serverless Framework:**
  * Relies on cloud provider for state tracking (SSM and S3 for AWS).
  * State tracking for application-level deployments.
* **Terraform:**
  * Maintains an explicit state file (```terraform.tfstate```).
  * Infrastructure wide state management.
  * Team collaboration supported through shared remote state file.
### In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?
* **Serverless Framework:**
  * For rapid development and deployment of event driven (e.g. HTTP triggers, database updates, scheduled jobs) serverless applications.
  * When developers want to focus on application logic and not on managing infrastructure. A key feature of the Serverless Framework is the abstraction of underlying infrastruture.
* **Terraform:**
  * When there is a need for complex infrastructure beyond just managed severless services.
  * Where stateful infrastructure and dependency tracking is needed.
  * Where team collaboration is required due to the scale of deployment and is fascilitated by common explicit state file.
### Are there scenarios where using both together might be beneficial?
Yes, there are scenarios where using both might be beneficial. For example, when an application requires both serverless functions and traditional infrastructure components. In this scenario, Serverless Framework could be used to deploy AWS Lambda functions and manage API Gateway configurations while Terraform could be use to deploy the supporting infrastructure such as VPCs, databases and S3 buckets. This way, we get the benefits of both Severless Framework in deploying serverless applications and Terraform in provisioning the infrastructure dependencies.

Sources: 
* [The Advantages of Using Serverless Framework Over Terraform](https://dorian599.medium.com/the-advantages-of-using-serverless-framework-over-terraform-136f358454bf)
* [The definitive guide to using Terraform with the Serverless Framework](https://www.serverless.com/blog/definitive-guide-terraform-serverless)
* [Marrying Terraform and Serverless Framework by Using the Parameter Store](https://blog.awsfundamentals.com/marrying-terraform-and-serverless-framework)
* [Terraform vs Serverless Framework](https://blog.glen-thomas.com/aws/platform-engineering/terraform/serverless/iac/2022/08/18/terraform-vs-serverless.html)
* [Serverless Framework State](https://www.serverless.com/framework/docs/guides/state)
* [Making Terraform and Serverless framework work together](https://medium.com/dazn-tech/making-terraform-and-serverless-framework-work-together-3fd3d173f33f)
* [Combining Terraform and the Serverless Framework Gracefully](https://medium.com/@tminussi/combining-terraform-and-the-serverless-framework-gracefully-5aeb4fbde370)
