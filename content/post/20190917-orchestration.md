+++
showonlyimage = true
draft = false
image = "img/orchestration-arch-design.png"
date = "2019-09-17T10:30:00+05:30"
title = "OpenSDS Orchestration - Simplifying Complex Data Management Tasks"
description = "To reduce manual intervention and provide ease of use, orchestration helps to streamline and optimize frequent, repeatable processes to ensure accurate and faster execution of services."
writer = "Himanshu, Ashit"
categories = [ "Blog", "Features", "Orchestration"]
tags = ["orchestration"]
# weight = 1
+++
To reduce manual intervention and provide ease of use, Orchestration helps to streamline and optimize frequent, repeatable processes to ensure accurate and faster execution of services.
<!--more-->
## Why Orchestrate?
> In a real distributed environment, most business processes consist of several interconnected steps that need to be performed in a specific order. Sometimes these business processes need to interact with other systems. If these complex business processes are interfered with users, they are error prone. To reduce manual intervention and provide ease of use, Orchestration helps to streamline and optimize frequent, repeatable processes to ensure accurate and faster execution of services.  

## Use Cases:
Automating tasks and Orchestrating interrelated tasks find multiple use cases:  

- **Autoscaling**: Auto scaling is always used in the cloud native scenario. Users will define some scaling policies that increases or decreases proportionally to the number of compute instances or storage capacity according to a utilization metric.
- **Data Migration**: Data migration is the process of moving data from one location to another or moving from one application to another. Data migration processes include many steps, such as selecting a data source, loading data, transforming the data and moving the data to a new location, checking the environment, and so on. Some of them are long-running steps that may cause data migration to fail if there is no automation
- **Big Data Analysis**: Data has been a driving factor in many industries and organizations, especially in financial companies. They store financial data on private data center for the purpose of security. They typically replicate data to the cloud and use big data analytics to capture financial data for new insights and an understanding of business, market, performance and growth.

## Background : What is OpenSDS?
> An open source community working under The Linux Foundation to address storage integration challenges in scale-out cloud native environments. Its vision is to connect siloed data solutions to build a self governed and intelligent data platform. On a high level, it connects any northbound platform to any southbound storage backend supporting various data management services (like Provisioning, Data Migration, Replication etc.)  

Read more about OpenSDS :  

[Website](https://www.opensds.io/) & [GitHub](https://github.com/opensds)

## OpenSDS Orchestration  

OpenSDS Orchestration provides seamless and simple ways to automate complex data management tasks. It can be used to optimize the repeatable process involved in the services in order to streamline complex flows. Therefore, Automation for OpenSDS which can be built into a series of processes and workflows, can be orchestrated to run automatically, to provide a more consistent and reliable standardized process.  

![OpenSDS Orchestration Manager Architecture diagram](/img/orchestration-arch-design.png)

## OpenSDS Orchestration Manager 

OpenSDS Orchestration Manager comprises of the following components:  

- **Service Catalog Manager**: It will provide a convenient way to manage service catalog which represents a variety of classic business process that will enable organizations to improve user experience, accelerate service delivery and reduce operational costs. User can register service catalog based on their business requirements. A service catalog instance will be generated when user executes service catalog with specific input. In addition, the history of execution can be queried when the service catalog is being executed or has been completed. User can write a YAML or JSON template to register a service catalog which represents a specific user’s business process. Service, Workflow and Task can be defined inside it. A Service contains workflows, each workflow consists of multiple tasks, and every task can have one or more than one action.
- **Connection Manager**: Connection Manager manages the connection between the OpenSDS Service Manager and the workflow manager. There can be different adapters which acts as workflow connector for OpenSDS workflow orchestration. Connector acts as an OpenSDS orchestration adapter for inbound and outbound integration with the Workflow Manager. In the current implementation, OpenSDS uses Stackstorm as the Workflow Manager and connector connects StackStorm to handle the interaction between service catalog manager and StackStorm.
- **Workflow Manager (i.e. Stackstorm)**: It’s an IFTTT framework which offers advanced automation, letting users create complex workflows to automate your tasks. Stackstorm breaks automation down into discrete actions and ties these actions together into workflows that can perform complex operations. StackStorm also provides a sophisticated event bus that can be used to implement event-based automation. Stackstorm enables OpenSDS Orchestration and Automation for the generic workflow actions based on OpenSDS projects such as hotpot, gelato and so forth.  

_**Note**: OpenSDS Orchestration Manager can support different “Workflow Managers”. As of now it is qualified to work with **Stackstorm**._  

- **Service**: It represents user defined business process. User can write a YAML or JSON template to register a service which on validation registers a workflow. Also, it can be canned workflows shipped with the solution.
- **Instance**: It is a consumable service. Once the registration is done, user can consume the service.
- **Execution**: A service instance can be executed immediately or scheduled later. It helps in tracking execution progress, result of service instance.
- **Connector**: It is the OpenSDS orchestration adapter for inbound and outbound integration with the Workflow Manager.
- **Workflow**: It stitches actions together, define the order, transition conditions, and passing the data.
- **Actions**: Actions are pieces of code that can perform arbitrary automation tasks.  

## Key Benefits  

As we discussed above, automating complex data management tasks and orchestrating reduces the manual maintenance of big storage clusters, effort and cost. It can also enable the user to build any custom workflows and get it automated. This helps to the solution provider to enhance the service catalog with more and more data management services.  

## Summary and Future  

Automation is not new, however automating and orchestrating complex data management workflows with different storage platforms is really a value. OpenSDS Orchestration can help to build custom workflows for heterogeneous platforms and storage systems. Going forward, it can build intelligence into these automations to handle reliability, disaster recovery etc.  

## Want to try OpenSDS Orchestration?  

[Click here for the OpenSDS Orchestration Manager Installation:](https://github.com/opensds/orchestration/blob/master/docs/INSTALL.md)

For information on how to write your own custom workflow and Orchestrate in OpenSDS  

[Click here for Developer Guides](https://github.com/opensds/documentation/tree/master/readthedocs/starterguides/developerguides)  

[Click here for User Guides](https://github.com/opensds/documentation/blob/master/readthedocs/starterguides/userguides/Orchestration_UserGuide.md)