# Sensor Health — Microsoft Defender for Endpoint KQL Queries

KQL queries for diagnosing **MDE sensor health** on Windows Servers: sensor enabled status, impaired communications, data collection issues, and a full cross-platform (Windows/macOS/Linux) endpoint agent health matrix.

| Query | What it answers |
|---|---|
| [`mde-server-health-diagnostic-and-remediation.kql`](mde-server-health-diagnostic-and-remediation.kql) | Which servers have unhealthy sensors, prioritized 1–5 for remediation? |
| [`mde-server-sensor-health-analysis-report.kql`](mde-server-sensor-health-analysis-report.kql) | Readable report of unhealthy sensor checks with risk description and fix |
| [`endpoint-agent-health-status-report.kql`](endpoint-agent-health-status-report.kql) | Full GOOD/BAD/N/A matrix across sensor, AV, tamper protection, cloud protection, and more |

⬅ [Back to main README](../../README.md)
