[Back to Syllabus](/README.md#course-syllabus)

## Learning Objectives

- Location of IBM Cloud Datacenters
- Account Type and Support Plans
- Billing and Usage
- The Cost Estimator
- Identity and Access Management
- IBM Cloud Console
- IBM Cloud CLI
- IBM Cloud Shell
<br>

## High Level Overview
- IBM Cloud has:
  - Over 200 services
  - 60 data centers worldwide
  - 47 of 50 Fortune companies

- Inside the IBM Cloud platform there is some layer that connect to each other
- Two main parts:
  - Console, identity and access management and catalog of products
  - Search and tagging resources, provisioning layer that allocate the resources and billing for unified account management and usage reports
- The IBM Cloud console is a dashboard for managing all the resources in your account
- The IBM Cloud CLI is a CLI supported by Mac, Linux and Windows, is extendable with plug-ins
- There is also the IBM Cloud Shell inside the dashboard
- To interact with services of IBM Cloud services there are API and SDK
- IBM Cloud have the best-in-industry security standard
<br>

## Locations and Regions
- IBM Cloud can deploy workloads in over:
  - 6 regions
  - 18 availability zones
  - 60 data centers

- The six IBM Cloud regions are:
  - Dallas
  - Washington DC
  - London
  - Frankfurt
  - Tokyo
  - Sydney

![image](https://user-images.githubusercontent.com/29455975/185744863-2a002c02-7910-4e4d-a366-1af7e40ef09f.png)

- In a single zone cluster your resources remain in the zone in which the cluster is deployed
- In IBM cloud, there is also the concept of a multi-zone region, a multi-zone region has three or more data centers within 6 miles of each other
- These data centers are located in close proximity to ensure high availability and resiliency
- So, essentially with a multi zone you have multiple places where you're deploying these servers and you're going to have more availability
<br>

## Account Types and Support Plans
- IBM Cloud has three main types of accounts:
  - Lite: free of charge
  - Pay-as-You-Go: access all IBM Cloud services
  - Subscription: enterprise customers

![image](https://user-images.githubusercontent.com/29455975/185744916-fa78df42-684c-4960-92d3-197fc58f68a2.png)

- Benefits
  - Lite: access to over 40 services like cloud object storage and cloud databases
  - Pay-as-You-Go: account are access to all services in the catalog, access to
    basic support, and it is fit for production use cases
  - Subscription: offers discounted pricing for services and support

- IBM Cloud support levels come in three forms:
  - Basic, which has access to create cases or tickets and can talk with support via phone or chat
  - Advanced, which guarantees a response time of 1 to 8 hours based on the severity of your ticket  
  - Premium, which guarantees a response time of 15 minutes to two hours and a
    technical account manager is assigned to your account for quarterly reviews
    
- Next, we'll take a deeper look into support and we'll show you how to create a ticket
  - In the account settings tab is where you can see your account type and then your ID
  - Click on support from the upper tab
  - In the support center, you can see your support plan
<br>

## Billing and Usage
- Billing and usage enables you to view detailed information about your IBM Cloud spending
- You can view billing by getting a monthly overview or you can view it by specific service, and you can also export your usage as a CSV file
- Next, we will take an in-depth look at billing and usage through a demo with the IBM Cloud Console
- So firstly, let's go into billing
  - So, we can click on this manage tab at the top and we can click on billing and usage
  - This will take us to the billing landing page and where we can quickly change our payments or uses and then see more things, such as order subscriptions and quotes
- So, let's click on usage
- Next, we can quickly add a promotion or a promo code
  - if we click on the promotions tab in the left-hand side
  - You can click apply here to add promo code
- If we want to click and create a spending notification, we’ll just go on spending notifications in the left-hand side and we can click on enable here and then add in your email address and then click a threshold

![image](https://user-images.githubusercontent.com/29455975/185744962-29cdd24d-cc6f-4196-9e2c-7a91bf6f16c9.png)
<br>

## Cost Estimator
- The cost estimator tool does exactly what its name suggests, it estimates the cost of an IBM Cloud service before you create the service
- The tool is supported by all IBM Cloud services ranging from AI Services to infrastructure, services and Kubernetes clusters

![image](https://user-images.githubusercontent.com/29455975/185744995-4860d283-8f2d-457e-ac8d-5af0aabb5b35.png)

- You can download your estimate as a PDF and you can calculate your estimate in over 15 currencies
<br>

## Hands-on Lab: Use the Cost Estimator Tool

- Navigate to [link](https://cloud.ibm.com/catalog) to launch the IBM Cloud Catalog
    - Add a quote
    - Review estimate
    - Download the PDF
![image](https://user-images.githubusercontent.com/29455975/185594127-ba741651-c8c6-4d39-9c51-57d88bc325d3.png)
<br>

## IAM

![image](https://user-images.githubusercontent.com/29455975/185745025-e46c08d8-7264-427f-a63a-1d600da3b3fe.png)

- In IBM Cloud, IAM is comprised of four concepts:
  - Users: these are the people that log in and use the account
  - Access groups: this is a way of grouping users together
  - Resources: a provision service offering selected from the catalog
  - Resource groups: a way of grouping resources together
- At the very highest level of IAM in IBM Cloud, we have an account
  - An account is comprised of many users
  - Each user has an email address that they use to log into IBM Cloud with
  - In each account there is an account owner
- In practice, for most enterprises this is usually a shared enterprise email that multiple
people can access should someone leave their job
- Difference between a service and a resource
  - A service is an entry from the IBM Cloud catalog, like a virtual machine or object storage or
one of the many other offerings
  - A resource is an instance of a service
- For example, in the IBM Cloud catalog, there's a database service called Cloudant
  - We can provision two instances of this service and called them DB-Dev and DV-prod
  - These would be our resources
- A user represents an IBM ID enabled account
  - Users are invited to join accounts which can be done through the console, IBM Cloud CLI or API
  - Users can create API keys to use with the CLI as an alternative to passwords for authentication
  - Users are given a role for the platform when invited, and these roles range from read-only viewer role to the administrator role, which can invite other users and view billing information
- Access groups are a collection of users
  - For instance, you may decide to group your users into access groups such as admins, billing, and basic users
  - Access groups help enable a cleaner separation of control, and it's worth noting that users can be part of multiple access groups at the same time
  - Resources have an automatically generated service ID, and they can be deployed to specific regions
- Resources have roles that can limit user access for that resource
  - For example, with cloud object storage, a user with the reader role could list and download objects in buckets
  - A user with a writer role could create and destroy buckets and a user with a manager role could control all aspects of data storage, like adding a retention policy and bucket firewall
- Resource groups are a collection of IBM Cloud resources
  - By grouping resources together, you can more easily provide access to multiple resources at once
  - Resource groups are specified at service creation time
  - A resource’s resource group cannot be changed
  - Resource groups have no geographical restrictions: this means you can put resources from Dallas and resources from Sydney in the same group,bringing it all together is the concept of an access policy
  - An access policy is the combination of a subject, which is a user or an access group, their role and a target, a resource or resource group
- So, let's talk a little bit about assigning users
  - Depending on your level of access, you can assign that same level of access or less to a new user
  - So, let's go ahead and click on the classic infrastructure and go to the devices
  - So, this is where you can see all the different specifications and permissions and actions for a specific device
  -With the Super user, of course, you could upgrade the server and view the software passwords, etc
- Now let's go ahead and talk about the IAM services
  - We can click all IAM services or we can go ahead and click on a specific service
  - So, we have cloud object storage, and we'll go cloudant in our account and we can give them access to only one region again so we can do Dallas or Frankfurt
  - We can click on Dallas and then all we do is we actually specify the service instance here and then we can give them editor access and then writer access 
  - So, and then let's do a test at Gmail and then all you do is add this and then you can see for this Cloud IAM services we've given them editor and writer access

- So, that's a little bit about IAM and that's how you would assign users additional access
<br>

## Hands-on Lab: Using the Catalog and Cloud Shell
- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database
    - Launch the IBM Cloud Shell
    - Use the IBM Cloud CLI

![image](https://user-images.githubusercontent.com/29455975/185613164-57e09cfb-340a-44e5-8c3b-85497d9c89ed.png)
<br>

## Module Summary
- IBM Cloud has a catalog of over 200 products and services covering IaaS, PaaS, containers, data and AI, blockchain and more; more than 60 data centers globally; is built on best-in-industry security standards, including GDPR, HIPAA, ISO 9001, PCI, and SOC2
- In terms of locations and regions, IBM Cloud has data centers in 19 countries and is divided into 6 regions; there is support for both single and multi-zone regions for better resiliency; there are federal regions for government workloads.
There are three account types on IBM Cloud: Lite, Pay-as-you-go, and Subscription; and there are three support levels on IBM Cloud: Basic, Advanced, and Premium
- IBM Cloud provides a month-to-month overview of billing and usage; usage and billing can be broken down by service; billing and usage reports can be exported as CSV files
- IBM Cloud’s Cost Estimator Tool is supported by all IBM Cloud services; is able to convert to multiple currencies, and is able to generate reports as PDF documents
- An IBM Cloud account can have many users and access groups, which are a collection of users; resources are instances of services from the catalog; roles are assigned on a user or access group and a resource or resource group, coming together to become an access policy
<br>

[Go to Next Module](./2_Infrastructure.md)
