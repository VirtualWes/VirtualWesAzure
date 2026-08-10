# VirtualWes Azure

Cloud architecture and Infrastructure as Code for **VirtualWes** — a greenfield Azure environment designed for secure web hosting, Azure Virtual Desktop (AVD), and future expansion into containers and CI/CD.

**Architect**: Wes Mac  
**Purpose**: Practical application of Azure Solutions Architect (AZ-305) design principles while building a production-grade foundational environment.

## Current Status
- **Phase**: Foundation (Identity, Governance, Monitoring, Cost Control)
- **IaC**: Bicep
- **Planned Workloads**: Web hosting → AVD → Containers / CI/CD

## Design Principles
- Governance, identity, and cost control before any workloads
- Infrastructure as Code from day one
- Least-privilege access and defense-in-depth
- Full observability with Azure Monitor + Log Analytics
- Explicit documentation of design decisions via Architecture Decision Records (ADRs)

## Repository Structure
- `/docs` — Naming conventions, tagging standards, ADRs, runbooks
- `/infra/bicep` — Bicep modules and environment deployments
- `/diagrams` — Architecture diagrams
- `/.github` — Workflows and issue templates (coming later)

## Architecture Decision Records
- [001 - Governance First](docs/adrs/001-governance-first.md)

## Getting Started
See the Issues and Project board for the current foundation tasks.
