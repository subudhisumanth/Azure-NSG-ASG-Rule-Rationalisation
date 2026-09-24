# Task 5 — Final NSG Rule Rationalisation

## Objective

To consolidate the required SSH and HTTP access into a single ASG-based Network Security Group rule and verify the final configuration.

## Before Rationalisation

The custom inbound configuration contained two rules:

| Priority | Rule | Port | Action |
|---:|---|---|---|
| 300 | SSH | 22 | Allow |
| 310 | Allow-HTTP-ASG | 80 | Allow |

Total custom inbound rules: **2**

## Rationalisation Procedure

1. Created a consolidated rule named `Allow-SSH-HTTP-ASG`.
2. Selected TCP as the protocol.
3. Configured destination ports `22,80`.
4. Selected `ASG-Web-2` as the destination Application Security Group.
5. Set the rule action to Allow.
6. Assigned priority `305`.
7. Verified that the consolidated rule was working.
8. Removed the previous separate SSH rule.
9. Removed the previous separate HTTP rule.
10. Verified the final inbound NSG configuration.

## Final Configuration

| Priority | Rule | Protocol | Ports | Destination | Action |
|---:|---|---|---|---|---|
| 305 | Allow-SSH-HTTP-ASG | TCP | 22,80 | ASG-Web-2 | Allow |

The Azure default NSG rules remain unchanged.

## Rule Reduction

Before rationalisation:

**2 custom inbound rules**

After rationalisation:

**1 custom inbound rule**

Reduction:

**50%**

### Calculation

```text
Reduction = (2 - 1) / 2 × 100
          = 50%
