# Project Abstract

## Azure Network Security Group and ASG Rule Rationalisation

Network Security Groups (NSGs) are used in Microsoft Azure to control inbound and outbound network traffic to Azure resources. As applications grow, maintaining multiple IP-based security rules can make network security configurations difficult to manage and maintain.

This project focuses on rationalising Azure Network Security Group rules by using Application Security Groups (ASGs). The objective is to replace individually defined network access rules with a structured ASG-based approach and reduce unnecessary custom security rules.

In this project, an Azure virtual machine named `web-vm` was configured with the Network Security Group `web-vm-nsg`. An Application Security Group named `ASG-Web-2` was created and the network interface `web-vm603` of the virtual machine was associated with it.

An ASG-based HTTP security rule was then configured. After analysing the custom inbound rules, SSH and HTTP access were consolidated into a single TCP rule using the Application Security Group. The original two custom inbound rules were reduced to one consolidated rule.

The final configuration demonstrates a 50% reduction in custom inbound NSG rules while maintaining the required SSH and HTTP access. This approach provides a more organised and scalable method for managing network security in Azure environments.
