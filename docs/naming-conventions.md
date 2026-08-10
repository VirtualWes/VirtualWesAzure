# Naming Conventions – VirtualWes

## Pattern
`vw-<resource-type>-<workload>-<environment>-<region>`

### Examples
| Resource              | Name                          |
|-----------------------|-------------------------------|
| Resource Group        | `vw-rg-shared-prod-eus`       |
| Resource Group        | `vw-rg-avd-prod-eus`          |
| Log Analytics         | `vw-law-shared-prod-eus`      |
| Key Vault             | `vw-kv-shared-prod-eus`       |
| Virtual Network       | `vw-vnet-hub-prod-eus`        |
| App Service           | `vw-app-web-prod-eus`         |
| Storage Account       | `vwstsharedprodeus`           |

## Environment Codes
- `prod`
- `nonprod` / `dev` / `test`

## Region Codes
- `eus` = East US
- `wus` = West US

## Rules
- All lowercase
- Hyphens as separators (except Storage Accounts)
- Keep names under the length limits for each resource type