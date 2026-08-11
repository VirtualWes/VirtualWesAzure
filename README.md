# VirtualWes Azure

Cloud architecture and Infrastructure as Code for **VirtualWes** — a greenfield Azure environment designed for secure web hosting, Azure Virtual Desktop (AVD), and future expansion into containers and CI/CD.

**Architect**: Wes Mac  
**Purpose**: Practical application of Azure Solutions Architect (AZ-305) design principles while building a production-grade foundational environment.

## Current Status
- **Phase**: Foundation complete (manual portal deployment)
- **Primary Region**: Central US (`cus`)
- **Subscription**: VirtualWes
- **IaC**: Bicep (next step — converting the foundation)
- **Planned Workloads**: Web hosting → AVD → Containers / CI/CD

## Design Principles
- Governance, identity, and cost control before any workloads
- Infrastructure as Code from day one (Bicep)
- Least-privilege access and defense-in-depth
- Full observability with Azure Monitor + Log Analytics
- Explicit documentation of design decisions via Architecture Decision Records (ADRs)

## What Has Been Built (Foundation)

| Component                    | Name                          | Notes                                      |
|-----------------------------|-------------------------------|--------------------------------------------|
| Shared Resource Group       | `vw-rg-shared-prod-cus`       | Main shared services                       |
| Monitoring Resource Group   | `vw-rg-monitoring-prod-cus`   | Log Analytics and monitoring               |
| Log Analytics Workspace     | `vw-law-shared-prod-cus`      | Central logging                            |
| Key Vault                   | `vw-kv-shared-prod-cus`       | Secrets management                         |
| Virtual Network             | `vw-vnet-hub-prod-cus`        | Address space `10.10.0.0/16`               |
| Subnets                     | `snet-shared` (`10.10.1.0/24`)<br>`snet-web` (`10.10.2.0/24`)<br>`snet-avd` (`10.10.3.0/24`)<br>`snet-mgmt` (`10.10.4.0/24`) | |
| Cost Management Budget      | `vw-budget-monthly-prod`      | Monthly budget with alerts                 |
| Azure Policy                | Require tag `Environment`     | Additional tag policies optional           |
| Diagnostic Settings         | Key Vault, VNet, Activity Log | Sending logs to Log Analytics              |

## Repository Structure
- `/docs` — Naming conventions, tagging standards, ADRs, inventory, runbooks
- `/infra/bicep` — Bicep modules and environment deployments (coming next)
- `/diagrams` — Architecture diagrams
- `/.github` — Workflows and issue templates (coming later)

## Architecture Decision Records
- [001 - Governance First](docs/adrs/001-governance-first.md)

## Next Steps
1. Convert the current foundation into Bicep
2. Add Network Security Groups
3. Deploy first workload (Web or AVD)
4. Expand monitoring and governance
