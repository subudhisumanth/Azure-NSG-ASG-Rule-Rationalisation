# Task 2 — NSG Rule Analysis

## Objective

To analyse the existing Network Security Group rules and identify the opportunity to use Application Security Groups (ASGs) for better organisation and rule management.

## Existing Configuration

The baseline NSG `web-vm-nsg` contains a custom SSH inbound rule:

| Priority | Name | Port | Protocol | Source | Destination | Action |
|---:|---|---:|---|---|---|---|
| 300 | SSH | 22 | TCP | Any | Any | Allow |

Azure default inbound rules are also present:

| Priority | Rule | Action |
|---:|---|---|
| 65000 | AllowVnetInBound | Allow |
| 65001 | AllowAzureLoadBalancerInBound | Allow |
| 65500 | DenyAllInBound | Deny |

## Analysis

The initial configuration uses a custom rule with broad source and destination values.

Application Security Groups provide a logical way to identify application workloads through their network interfaces instead of relying on individual IP addresses.

The project therefore introduces `ASG-Web-2` and associates the network interface `web-vm603` with the ASG.

## Rationalisation Approach

1. Identify the existing custom access rules.
2. Create an Application Security Group.
3. Associate the required network interface with the ASG.
4. Configure an NSG rule using the ASG.
5. Consolidate the required SSH and HTTP access into an ASG-based rule.
6. Verify the final NSG configuration.

## Result

The existing NSG configuration was analysed and an ASG-based approach was selected for rule rationalisation.
