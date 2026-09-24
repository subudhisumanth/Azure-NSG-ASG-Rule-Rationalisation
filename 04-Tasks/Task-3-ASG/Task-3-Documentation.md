# Task 3 — Application Security Group

## Objective

To create an Application Security Group (ASG) and associate the web virtual machine network interface with it.

## ASG Configuration

| Property | Value |
|---|---|
| Application Security Group | `ASG-Web-2` |
| Resource Group | `RG-AzureNetworking-Lab` |
| Region | Central India |
| Network Interface | `web-vm603` |
| Private IP | `10.0.0.4` |
| Virtual Machine | `web-vm` |

## Procedure

1. Opened Microsoft Azure Portal.
2. Navigated to **Application Security Groups**.
3. Created the Application Security Group `ASG-Web-2`.
4. Selected the Central India region.
5. Opened the ASG after successful deployment.
6. Added the network interface `web-vm603`.
7. Verified that the NIC belonging to `web-vm` was associated with the ASG.

## Result

The Application Security Group `ASG-Web-2` was successfully created and the network interface `web-vm603` was associated with it.

The ASG can now be used as a logical destination in NSG security rules.
