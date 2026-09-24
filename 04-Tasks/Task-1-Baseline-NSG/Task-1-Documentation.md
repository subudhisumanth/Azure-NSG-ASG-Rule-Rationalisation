# Task 1 — Baseline NSG Configuration

## Objective

To inspect and document the initial Network Security Group (NSG) configuration before applying Application Security Group (ASG)-based rule rationalisation.

## Azure Resource

- Resource Group: `RG-AzureNetworking-Lab`
- Network Security Group: `web-vm-nsg`
- Region: Central India
- Associated Network Interface: `web-vm603`

## Initial Inbound Rules

The initial custom inbound rule was:

| Priority | Rule | Port | Protocol | Source | Destination | Action |
|---:|---|---:|---|---|---|---|
| 300 | SSH | 22 | TCP | Any | Any | Allow |

Azure also provided the following default inbound rules:

| Priority | Rule | Action |
|---:|---|---|
| 65000 | AllowVnetInBound | Allow |
| 65001 | AllowAzureLoadBalancerInBound | Allow |
| 65500 | DenyAllInBound | Deny |

## Initial Outbound Rules

The default outbound rules were also present:

- AllowVnetOutBound
- AllowInternetOutBound
- DenyAllOutBound

## Procedure

1. Opened the Microsoft Azure Portal.
2. Navigated to **Network Security Groups**.
3. Opened `web-vm-nsg`.
4. Selected **Inbound security rules**.
5. Inspected the existing custom and default security rules.
6. Recorded the baseline configuration before applying ASG-based rationalisation.

## Result

The baseline NSG configuration was successfully documented. The initial custom inbound SSH rule was identified for subsequent analysis and rationalisation.

## Evidence

Screenshot:

`Task-1-Baseline-NSG-Rules.png`
