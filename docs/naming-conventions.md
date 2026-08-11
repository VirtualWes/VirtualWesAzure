# Naming Conventions – VirtualWes

## Pattern
`vw-<resource-type>-<workload>-<environment>-<region>`

### Examples
| Resource              | Name                            |
|-----------------------|---------------------------------|
| Resource Group        | `vw-rg-shared-prod-cus`         |
| Resource Group        | `vw-rg-monitoring-prod-cus`     |
| Resource Group        | `vw-rg-avd-prod-cus`            |
| Log Analytics         | `vw-law-shared-prod-cus`        |
| Key Vault             | `vw-kv-shared-prod-cus`         |
| Virtual Network       | `vw-vnet-hub-prod-cus`          |
| App Service           | `vw-app-web-prod-cus`           |
| Storage Account       | `vwstsharedprodcus`             |

## Environment Codes
- `prod`
- `nonprod` / `dev` / `test`

## Region Codes
- `cus` = Central US (primary)
- `eus` = East US
- `eus2` = East US 2
- `wus` = West US
- `wus2` = West US 2

## Rules
- All lowercase
- Hyphens as separators (except Storage Accounts — no hyphens, shorter names)
- Keep names under the length limits for each resource type
- Primary region for VirtualWes is **Central US** (`cus`)
