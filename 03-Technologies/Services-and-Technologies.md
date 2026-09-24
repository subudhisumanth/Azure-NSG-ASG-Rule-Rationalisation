# Services and Technologies Required

## Cloud Platform

### Microsoft Azure
Microsoft Azure is used as the cloud platform for deploying and configuring the networking resources required for the project.

## Azure Services

| Service | Purpose |
|---|---|
| Azure Virtual Machine | Hosts the web server workload |
| Azure Virtual Network | Provides the private network environment |
| Network Security Group (NSG) | Controls inbound and outbound network traffic |
| Application Security Group (ASG) | Groups network interfaces logically for security rules |
| Network Interface (NIC) | Provides network connectivity to the virtual machine |
| Public IP Address | Provides external connectivity to the virtual machine |
| Resource Group | Organises and manages the Azure resources |

## Operating System

**Ubuntu Server 24.04 LTS**

The virtual machine uses Ubuntu Server 24.04 LTS as its operating system.

## Networking Technologies

- TCP/IP
- SSH — TCP port 22
- HTTP — TCP port 80
- Virtual Network
- Subnet
- Network Security Groups
- Application Security Groups

## Development and Documentation Tools

- Microsoft Azure Portal
- GitHub
- Git
- Web Browser
- SSH Client

## Azure Resources Used in the Project

| Resource | Name |
|---|---|
| Resource Group | `RG-AzureNetworking-Lab` |
| Virtual Machine | `web-vm` |
| Network Security Group | `web-vm-nsg` |
| Application Security Group | `ASG-Web-2` |
| Network Interface | `web-vm603` |
| Private IP | `10.0.0.4` |
| Region | Central India |
| Subscription | Azure for Students |

## Security Configuration

The final NSG configuration uses an ASG-based consolidated rule:

```text
Priority: 305
Name: Allow-SSH-HTTP-ASG
Protocol: TCP
Destination: ASG-Web-2
Destination Ports: 22,80
Action: Allow
