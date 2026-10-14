# Effort defaults

The calculator uses this file for every task, the default days a year, the scaling rule, the tooltip, and the source.

Task days are an estimate. Edit them on the page to match your team. They are not a BMC figure and not a customer result.

## Rules

- You keep service governance, operational reporting, and application administration either way. Those rows have no days.
- Shared platform days are counted once, for the solutions you tick.
- Each extra solution adds 10% more shared-platform days, because the same stack is run harder. Solution tasks are not scaled. They are added in full.
- With no solution ticked, shared days are not counted.
- SaaS residual is 10% of the on-prem days, rounded to the nearest day. Your team still spends those days. Days returned = on-prem days minus residual.
- People = days returned ÷ 230 working days. The 230 is an estimate.
- Cost per engineer day defaults to AED 1,950 (about US$530).
- Server running cost is AED 30,000 per server per year. It is used only if you type a server count. It is power, space, support, and software licences. It excludes the hardware purchase.

## Check totals

Service management only: shared 120 + solution 66 = 186 on-prem days. Residual 19. Days returned 167.

All four solutions: shared × 1.3 = 156, plus solutions 293 = 449 on-prem days. Residual 45. Days returned 404.

## You keep this either way

No days. Green on both the on-prem side and the SaaS side.

- Service governance & performance management
- Operational reporting & analytics
- Application administration, workflows & integrations

## Shared platform

Tooltip for every row: "Estimate, edit to match your team. Not a vendor figure."

### Application operations

| Task | Days/year |
| --- | ---: |
| Upgrades & release testing | 12 |
| Patching & hotfixes | 8 |
| Env refreshes (dev/QA/prod) | 8 |

### Software stack

| Task | Days/year |
| --- | ---: |
| Kubernetes / OpenShift | 10 |
| Databases, search, messaging | 8 |
| Adaptors & connectors runtime | 6 |

### Infrastructure operations

| Task | Days/year |
| --- | ---: |
| HA design & DR failover tests | 8 |
| Backups & restore drills | 6 |
| Monitoring the platform itself | 8 |

### Security & compliance

| Task | Days/year |
| --- | ---: |
| CVE tracking & hardening | 8 |
| Penetration testing | 4 |
| Audit evidence & certifications | 6 |

### Hardware infrastructure

| Task | Days/year |
| --- | ---: |
| Compute, storage, network | 10 |
| Capacity planning & scaling | 6 |
| Data centre & availability zones | 12 |

## Solution tasks

Counted only when that solution is ticked. Five tasks each. Same tooltip: "Estimate, edit to match your team. Not a vendor figure."

### Service management

ITSM, DWP, Business Workflows. Default: ticked.

| Task | Days/year |
| --- | ---: |
| Platform & app upgrades | 18 |
| Mid-tier & plugin servers | 12 |
| SSO, email & notification engines | 12 |
| Custom integration maintenance | 14 |
| Regression testing per release | 10 |

### Observability & AIOps

| Task | Days/year |
| --- | ---: |
| Event pipelines & connectors | 16 |
| Metric & log store sizing | 14 |
| ML and analytics services | 16 |
| Retention & index management | 16 |
| Agent rollout across the fleet | 14 |

### Discovery & CMDB

| Task | Days/year |
| --- | ---: |
| Appliance patching & TKU updates | 18 |
| Scanner & credential upkeep | 16 |
| Reconciliation jobs & tuning | 15 |
| Sync infrastructure | 14 |
| Data-model change control | 12 |

### HelixGPT & agentic AI

| Task | Days/year |
| --- | ---: |
| LLM hosting & GPU sizing | 20 |
| Model and agent service updates | 16 |
| Vector store & indexing ops | 14 |
| AI scaling under load | 14 |
| Guardrail & policy plumbing | 12 |

## Sources

- Engineer day rate. Cooper Fitch, UAE Salary Guide 2025. Cloud Engineer about AED 24,000–30,000 a month, DevOps Engineer about AED 23,000–30,000 a month, before bonus. We use AED 28,000 × 12 × 1.25 loading = AED 420,000 a year. The 1.25 is ours. AED 420,000 ÷ 215 working days, rounded, is AED 1,950 a day (about US$530). The 215 is an estimate. https://cooperfitch.ae/wp-content/uploads/2024/12/Salary-Guide-UAE-2025-Cooper-Fitch.pdf
- Availability. Helix subscription services, 99.9% in a month. Planned maintenance is excluded. https://www.helixops.ai/content/dam/bmc/corporate/service-level-agreement.pdf
- Recovery. A 15-minute recovery point, and a 4-hour recovery time, unless the contract says otherwise. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Operations/Data-centers-and-architecture/Business-continuity-and-disaster-recovery/
- Certifications. ISO 27001, and a yearly SOC 2 Type II examination. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Security/Compliance/
- Data location. For a UAE cloud subscription, backups are stored in Abu Dhabi (UAE Central). Data stays in the country you select. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Operations/Data-centers-and-architecture/Service-locations/
- Task days, the 10% extra per solution, the 10% residual, 230 working days, 215 days inside the day rate, and AED 30,000 per server: estimate, edit to match your team.
