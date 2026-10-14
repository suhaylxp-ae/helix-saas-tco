# Effort defaults

The calculator uses this file for every task, the default days a year, the scaling rule, the tooltip, and the source.

Task days with no public source are an estimate. Edit them on the page to match your team. They are not a BMC figure and not a customer result.

## Rules

- You keep service governance, operational reporting, and application administration either way. Those rows have no days.
- The platform is counted once. It is 148 days: 108 scaling (S) and 40 fixed (F).
- Each extra solution adds 50% of the scaling total. Fixed tasks are not lifted. Solution tasks are not lifted. They are added in full.
- If you edit a scaling task, the extra is 50% of the edited scaling total, not of the original 108.
- With no solution ticked, the page says "Tick at least one solution" and does not show 0 days.
- A share link with no real solution, such as `#sol=xx`, falls back to Service management.
- On-prem days = 148 + 54 × (solutions − 1) + ticked solution days, when the scaling tasks are still at these defaults. 54 is half of 108.
- SaaS residual = 19 + 5 × (solutions − 1). Days returned = on-prem days − residual.
- People = days returned ÷ 230 working days.
- Cost per engineer day defaults to AED 1,950 (about US$530). That is AED 30,000 a month × 12 × 1.25 loading ÷ 230 days, rounded.
- Server running cost is AED 30,000 per server per year. It is used only if you type a server count. It is power, space, support, and software licences. It excludes the hardware purchase.
- On-prem licence and maintenance per year is blank by default. It is added to the on-prem side of the 5-year comparison only when a SaaS quote is entered.

## Check totals

Service management only: 148 + 38 = 186 on-prem days. Residual 19. Days returned 167.

Observability only: 148 + 32 = 180 on-prem days. Residual 19. Days returned 161.

HelixGPT only: 148 + 26 = 174 on-prem days. Residual 19. Days returned 155.

All four solutions: 148 + 54 × 3 + 128 = 438 on-prem days. Residual 34. Days returned 404.

## You keep this either way

No days. Green on both the on-prem side and the SaaS side.

- Service governance & performance management
- Operational reporting & analytics
- Application administration, workflows & integrations

## Shared platform

Total 148. Scaling 108. Fixed 40.

S = scales with extra solutions. F = fixed.

### Application operations

| Task | Days/year | Scales | Tooltip |
| --- | ---: | --- | --- |
| Upgrades & release testing | 30 | S | Plan, run and test each new version across dev, test and production. |
| Patching & hotfixes | 12 | S | Apply fixes BMC releases between upgrades. |
| Environment refreshes | 8 | S | Rebuild dev, test and production from a clean copy. |

### Software stack

| Task | Days/year | Scales | Tooltip |
| --- | ---: | --- | --- |
| Kubernetes/OpenShift | 20 | F | Keep the container platform under Helix patched and healthy. |
| Databases, search, messaging | 15 | S | Patch and look after the databases, search, and message queues. |
| Adaptors & connectors runtime | 5 | S | Keep the connectors that move data in and out running. |

### Infrastructure operations

| Task | Days/year | Scales | Tooltip |
| --- | ---: | --- | --- |
| HA design & DR failover tests | 8 | F | Test that the spare site takes over if the main one fails. |
| Backups & restore drills | 6 | S | Run backups and practise a restore. |
| Monitoring the platform itself | 8 | S | Watch the platform that Helix runs on, not the business services. |

### Security & compliance

| Task | Days/year | Scales | Tooltip |
| --- | ---: | --- | --- |
| CVE tracking & hardening | 12 | S | Track new vulnerabilities and apply the hardening they need. |
| Penetration testing | 4 | F | Commission a yearly test that tries to break in. |
| Audit evidence & certifications | 5 | F | Collect the proof auditors ask for. |

### Hardware infrastructure

| Task | Days/year | Scales | Tooltip |
| --- | ---: | --- | --- |
| Compute, storage, network | 8 | S | Look after the servers, disks, and network Helix uses. |
| Capacity planning & scaling | 4 | S | Check you have enough room before you run out. |
| Data centre & availability zones | 3 | F | Deal with the data centre, power, and the extra site. |

## Solution tasks

Counted only when that solution is ticked. Five tasks each. Not scaled.

### Service management

ITSM, DWP, Business Workflows. Default: ticked. Sum 38.

| Task | Days/year | Tooltip |
| --- | ---: | --- |
| Platform & app upgrades | 10 | Upgrade the service-management apps and retest your setup. |
| Mid-tier & plugin servers | 4 | Patch and restart the extra servers those apps need. |
| SSO, email & notification engines | 4 | Keep sign-on, email, and alerts working. |
| Custom integration maintenance | 10 | Fix the links you built to other systems when they change. |
| Regression testing per release | 10 | Retest your own workflows after each release. |

### Observability & AIOps

Sum 32.

| Task | Days/year | Tooltip |
| --- | ---: | --- |
| Event pipelines & connectors | 8 | Keep the pipes that bring events in from your tools. |
| Metric & log store sizing | 5 | Make sure metric and log storage does not fill up. |
| ML & analytics services | 4 | Look after the services that group events and spot patterns. |
| Retention & index management | 5 | Decide how long data is kept and keep the indexes healthy. |
| Agent rollout across fleet | 10 | Install and update the agents on your servers. |

### Discovery & CMDB

Sum 32.

| Task | Days/year | Tooltip |
| --- | ---: | --- |
| Appliance patching & TKU updates | 10 | Apply BMC's monthly discovery content and appliance OS updates. |
| Scanner & credential upkeep | 6 | Keep scan accounts working and the scanners online. |
| Reconciliation jobs & tuning | 8 | Tune the jobs that match new data to the CMDB. |
| Sync infrastructure | 4 | Keep the copy of data between Discovery and the CMDB moving. |
| Data-model change control | 4 | Control changes to the types of items you store. |

### HelixGPT & agentic AI

Sum 26.

| Task | Days/year | Tooltip |
| --- | ---: | --- |
| LLM hosting & GPU sizing | 6 | Host the model and make sure it has enough GPU. |
| Model & agent service updates | 6 | Apply new model and agent versions and retest them. |
| Vector store & indexing ops | 5 | Keep the search index the assistant uses up to date. |
| AI scaling under load | 4 | Add capacity when more people use the assistant. |
| Guardrail & policy plumbing | 5 | Keep the rules that limit what the assistant can do. |

Tasks with no source in the list below are marked on the page: "Estimate, edit to match your team."

## Sources

- Engineer day rate. Cooper Fitch, UAE Salary Guide 2025. We use AED 30,000 a month × 12 × 1.25 loading ÷ 230 days, rounded to AED 1,950 a day (about US$530). The 1.25 loading is ours. https://cooperfitch.ae/wp-content/uploads/2024/12/Salary-Guide-UAE-2025-Cooper-Fitch.pdf
- Upgrades. BMC Helix On-Prem Container Upgrade Service. Estimated duration 6 to 10 weeks for one environment. The 30 days is staff effort, not that calendar window. https://www.helixops.ai/it-services/success-catalog/bmc-helix-on-premise-container-upgrade-service.html
- Kubernetes release cycle. A new release about three times a year. https://kubernetes.io/releases/
- Spectro Cloud, State of Production Kubernetes 2025. The 20 days for Kubernetes/OpenShift is an estimate of the work to keep it healthy. https://www.spectrocloud.com/state-of-kubernetes-2025
- TKU. BMC publishes Technology Knowledge Updates on a monthly schedule. The 10 days is an estimate of the work to apply them. https://docs.helixops.ai/bin/IT-Operations-Management/Discovery/BMC-Discovery/Configipedia/Technology-Knowledge-Updates-TKU/Schedule-and-Roadmap/
- Penetration testing. PCI DSS expects a test at least once a year. The 4 days is an estimate of the time to manage that test. https://listings.pcisecuritystandards.org/documents/Penetration-Testing-Guidance-v1_1.pdf
- Availability. Helix subscription services, 99.9% in a month. Planned maintenance is excluded. https://www.helixops.ai/content/dam/bmc/corporate/service-level-agreement.pdf
- Recovery. A 15-minute recovery point, and a 4-hour recovery time, unless the contract says otherwise. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Operations/Data-centers-and-architecture/Business-continuity-and-disaster-recovery/
- Certifications. ISO 27001, and a yearly SOC 2 Type II examination. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Security/Compliance/
- Data location. For a UAE cloud subscription, backups are stored in Abu Dhabi (UAE Central). Data stays in the country you select. https://docs.helixops.ai/bin/Helix-Common-Services/Other/BMC-Helix-Subscriber-Information/helixsubscriber/Operations/Data-centers-and-architecture/Service-locations/
- Every other task day, the 50% scaling rule, the residual of 19 days plus 5 for each extra solution, 230 working days, and AED 30,000 per server: estimate, edit to match your team.
