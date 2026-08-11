# VirtualWes Foundation Inventory

**Last Updated**: 2026-08-10  
**Region**: Central US (`cus`)  
**Subscription**: VirtualWes (`ad5c68b6-779c-4514-a4bf-f134fbcf1e0e`)

## Resource Groups
- `vw-rg-shared-prod-cus`
- `vw-rg-monitoring-prod-cus`

## Core Resources
| Resource Type              | Name                        | Resource Group                  | Notes |
|---------------------------|-----------------------------|----------------------------------|-------|
| Log Analytics Workspace   | `vw-law-shared-prod-cus`    | `vw-rg-monitoring-prod-cus`     | Workspace ID: `ec2bd4d0-5306-4bfc-a2bb-4774b455ff97` |
| Key Vault                 | `vw-kv-shared-prod-cus`     | `vw-rg-shared-prod-cus`         | URI: `https://vw-kv-shared-prod-cus.vault.azure.net/` |
| Virtual Network           | `vw-vnet-hub-prod-cus`      | `vw-rg-shared-prod-cus`         | `10.10.0.0/16` |

## Subnets
| Name         | Address Range   | Purpose              |
|--------------|-----------------|----------------------|
| snet-shared  | 10.10.1.0/24    | Shared services      |
| snet-web     | 10.10.2.0/24    | Web / App Service    |
| snet-avd     | 10.10.3.0/24    | Azure Virtual Desktop|
| snet-mgmt    | 10.10.4.0/24    | Management / jumpbox |

## Other
- Cost Budget: `vw-budget-monthly-prod`
- Policy: Require tag `Environment`
- Diagnostic Settings: Enabled on Key Vault, VNet, and Subscription Activity Log → Log Analytics workspace

## Tags Applied (standard)
- Environment: prod
- Owner: wes
- Project: VirtualWes
- CostCenter: learning
- Workload: shared / monitoring (as appropriate)
