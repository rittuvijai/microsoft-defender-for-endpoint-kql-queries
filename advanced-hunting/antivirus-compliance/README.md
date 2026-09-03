# Antivirus Compliance — Microsoft Defender for Endpoint KQL Queries

KQL queries for auditing **Microsoft Defender Antivirus compliance** on Windows Servers via Defender for Endpoint Advanced Hunting: AV enablement, real-time protection, signature age/freshness, AV mode (Active/Passive/EDR Blocked), and scan recency.

| Query | What it answers |
|---|---|
| [`av-compliance-status-on-servers.kql`](av-compliance-status-on-servers.kql) | What % of servers are compliant for AV enabled / signatures / real-time protection? |
| [`av-signature-age-distribution.kql`](av-signature-age-distribution.kql) | How stale are AV signatures across the fleet? |
| [`non-compliant-servers-detailed-report.kql`](non-compliant-servers-detailed-report.kql) | Which specific servers are non-compliant, and why? |
| [`antivirus-health-risk-assessment.kql`](antivirus-health-risk-assessment.kql) | Which servers are High/Medium/Low AV risk overall? |
| [`antivirus-scan-recency-daily-report.kql`](antivirus-scan-recency-daily-report.kql) | Which servers haven't had a recent completed AV scan? |
| [`av-compliance-and-signature-update-analysis.kql`](av-compliance-and-signature-update-analysis.kql) | Criticality-tiered breakdown of signature age and AV mode issues, with remediation steps |

⬅ [Back to main README](../../README.md)
