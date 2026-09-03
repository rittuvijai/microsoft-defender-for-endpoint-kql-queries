# Onboarding & Device Inventory — Microsoft Defender for Endpoint KQL Queries

KQL queries for closing **Defender for Endpoint onboarding coverage gaps**: environment-wide onboarding status distribution, unassigned-group non-onboarded servers, and internet-facing servers eligible for onboarding (highest priority).

| Query | What it answers |
|---|---|
| [`onboarding-status-distribution.kql`](onboarding-status-distribution.kql) | What % of the environment is Onboarded / Can Be Onboarded / Unsupported? |
| [`non-onboarded-windows-server-devices.kql`](non-onboarded-windows-server-devices.kql) | Which non-onboarded servers are sitting in the unassigned machine group? |
| [`internet-facing-servers-eligible-for-onboarding.kql`](internet-facing-servers-eligible-for-onboarding.kql) | Which internet-facing servers still need to be onboarded first? |

## Author
**Rittu Vijai** — Senior Cloud Ops & Automation Engineer | Azure Observability | Defender Endpoint | KQL (Dallas-Fort Worth Metroplex)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rittuvijai)

⬅ [Back to main README](../../README.md)
