# Task 4 — ASG-Based NSG Rule

## Objective

To configure an NSG security rule using an Application Security Group (ASG) instead of an individual IP-based destination.

## Rule Configuration

| Property | Value |
|---|---|
| Priority | `305` |
| Rule Name | `Allow-SSH-HTTP-ASG` |
| Protocol | TCP |
| Source | Any |
| Source Port | * |
| Destination | `ASG-Web-2` |
| Destination Ports | `22,80` |
| Action | Allow |

## Procedure

1. Opened the `web-vm-nsg` Network Security Group.
2. Navigated to **Settings → Inbound security rules**.
3. Created an inbound security rule.
4. Selected TCP as the protocol.
5. Configured ports 22 and 80 for SSH and HTTP access.
6. Selected `ASG-Web-2` as the destination.
7. Set the action to **Allow**.
8. Assigned priority `305`.
9. Created the rule as `Allow-SSH-HTTP-ASG`.
10. Verified the rule in the inbound security rules list.

## Result

The ASG-based NSG rule was successfully created. The rule uses `ASG-Web-2` as the destination and consolidates SSH and HTTP access into one custom rule.

## Evidence

Screenshot:

`Task-4-ASG-NSG-Rule.png`
