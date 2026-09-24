# Azure Network Security Group and ASG Rule Rationalisation

## Project Code

24CC3046-P028

## Project Overview

This project focuses on rationalising Azure Network Security Group (NSG) rules by replacing IP-based or individually defined access rules with Application Security Groups (ASGs).

The main objective is to simplify network security management, improve rule organisation, and reduce the number of custom NSG rules while maintaining the required network access.

## Objectives

- Configure an Azure Network Security Group.
- Analyse existing inbound NSG rules.
- Create and configure an Application Security Group.
- Associate the virtual machine network interface with the ASG.
- Configure NSG rules using the ASG.
- Consolidate multiple custom rules into a single rule.
- Reduce the number of custom NSG rules by 50%.
- Verify the final NSG configuration.

## Azure Environment

| Component | Configuration |
|---|---|
| Subscription | Azure for Students |
| Resource Group | RG-AzureNetworking-Lab |
| Region | Central India |
| Virtual Machine | web-vm |
| Operating System | Ubuntu Server 24.04 LTS |
| Network Interface | web-vm603 |
| Private IP | 10.0.0.4 |
| Network Security Group | web-vm-nsg |
| Application Security Group | ASG-Web-2 |

## Project Tasks

### Task 1 — Baseline NSG Configuration

Document the initial NSG configuration and existing inbound security rules.

### Task 2 — NSG Rule Analysis

Analyse the existing custom rules and identify opportunities for consolidation and rationalisation.

### Task 3 — Application Security Group

Create the Application Security Group `ASG-Web-2` and associate the `web-vm603` network interface with it.

### Task 4 — ASG-Based NSG Rule

Configure an NSG rule using the Application Security Group for HTTP traffic.

### Task 5 — Rule Rationalisation

Create a consolidated ASG-based rule for SSH and HTTP traffic and remove the redundant custom rules.

## Final Result

Before rationalisation:

- Custom inbound rules: 2

After rationalisation:

- Custom inbound rules: 1

Rule reduction:

**50%**

The final configuration uses the Application Security Group `ASG-Web-2` with a consolidated TCP rule covering ports 22 and 80.

## Technologies and Services

- Microsoft Azure
- Azure Virtual Machines
- Azure Virtual Network
- Network Security Groups
- Application Security Groups
- Network Interfaces
- Ubuntu Server
- TCP/IP
- SSH
- HTTP
- GitHub

## Project Documentation

- [Project Abstract](01-Project-Abstract/Project-Abstract.md)
- [Services and Technologies](03-Technologies/Services-and-Technologies.md)
- [Task Documentation](04-Tasks/)
- [Final Results](Results/Final-Results.md)
