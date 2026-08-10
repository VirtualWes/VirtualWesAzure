# ADR 001: Governance and Identity First

## Status
Accepted

## Context
VirtualWes is a new Azure environment intended for learning AZ-305 design skills and building resume-relevant experience. There is a temptation to jump straight to workloads (App Service, AVD, containers).

## Decision
We will complete identity, governance, cost management, monitoring, and a minimal shared landing zone **before** deploying any workload resources.

## Consequences
- Slightly slower start
- Much cleaner, more professional, and more defendable architecture
- Directly practices the design skills tested in AZ-305
- Prevents costly and messy technical debt later