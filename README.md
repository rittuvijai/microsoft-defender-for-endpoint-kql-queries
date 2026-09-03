# Microsoft Defender for Endpoint KQL Queries (Advanced Hunting)

A curated, categorized collection of **Microsoft Defender for Endpoint (MDE) Advanced Hunting KQL queries** for antivirus compliance, sensor health, security configuration assessment, vulnerability management, onboarding coverage, browser extension risk, and device inventory reporting on **Windows Servers**.

Every query in this repository is real, production-tested Kusto Query Language (KQL) written against the **Defender for Endpoint Advanced Hunting schema** (`DeviceInfo`, `DeviceTvmSecureConfigurationAssessment`, `DeviceTvmSoftwareVulnerabilities`, `DeviceEvents`, `DeviceNetworkInfo`, `DeviceTvmBrowserExtensions`) inside **Microsoft 365 Defender / Microsoft Defender XDR**.

> **Keywords:** Microsoft Defender for Endpoint, MDE Advanced Hunting, KQL queries, Defender XDR, Microsoft 365 Defender, threat hunting, SOC queries, antivirus compliance, sensor health, Kusto Query Language, DeviceTvmSecureConfigurationAssessment, security configuration assessment, vulnerability management, onboarding status, Windows Server security.

## Table of Contents

- [Why this repo exists](#why-this-repo-exists)
- [Antivirus Compliance](advanced-hunting/antivirus-compliance/) — signature age, AV mode, real-time protection, scan recency
- [Sensor Health](advanced-hunting/sensor-health/) — sensor status, impaired communications, data collection
- [Security Configuration Assessment](advanced-hunting/security-configuration/) — TVM secure configuration findings
- [Vulnerability Management](advanced-hunting/vulnerability-management/) — high-severity CVE analysis
- [Browser Extension Risk](advanced-hunting/browser-extensions/) — risky Chrome/Firefox/Edge extensions
- [Onboarding & Device Inventory](advanced-hunting/onboarding-and-inventory/) — onboarding coverage gaps
- [Device Inventory by OS](advanced-hunting/device-inventory/) — Windows, macOS, Linux, Android
- [Other EDR Platform Investigations](other-edr-platform-investigations/) — non-KQL reference queries
- [How to run these queries](#how-to-run-these-queries)
- [Contributing](#contributing)
- [License](#license)

## Why this repo exists

Security teams running **Microsoft Defender for Endpoint** need repeatable Advanced Hunting queries to answer the same operational questions every week: *Is antivirus actually enabled and up to date on every server? Which servers still aren't onboarded? Which sensors have gone quiet?* This repository packages those queries into ready-to-run `.kql` files, organized by use case, so SOC analysts, MDE administrators, and cloud security engineers don't have to rebuild them from scratch.

## Query Categories

### 🛡️ Antivirus Compliance
Queries covering AV enablement, real-time protection, signature freshness, scan recency, and AV compliance rate reporting for Windows Servers. See [`advanced-hunting/antivirus-compliance/`](advanced-hunting/antivirus-compliance/).

### 📡 Sensor Health
Queries that surface unhealthy MDE sensors, impaired communications, and data collection failures, with remediation priority scoring. See [`advanced-hunting/sensor-health/`](advanced-hunting/sensor-health/).

### 🔒 Security Configuration Assessment
Full Threat & Vulnerability Management (TVM) secure configuration findings for Windows Servers, mapped to benchmarks and remediation steps. See [`advanced-hunting/security-configuration/`](advanced-hunting/security-configuration/).

### 🐛 Vulnerability Management
High-severity CVE analysis across Windows Server software inventory, bucketed by CVE age. See [`advanced-hunting/vulnerability-management/`](advanced-hunting/vulnerability-management/).

### 🧩 Browser Extension Risk
Detection of medium/high-risk Chrome, Firefox, and Edge extensions installed on servers. See [`advanced-hunting/browser-extensions/`](advanced-hunting/browser-extensions/).

### ✅ Onboarding & Device Inventory
Finds onboarding coverage gaps, including internet-facing servers not yet onboarded. See [`advanced-hunting/onboarding-and-inventory/`](advanced-hunting/onboarding-and-inventory/).

### 💻 Device Inventory by OS
Cross-platform 90-day device inventory queries for Windows, macOS, Linux, and Android. See [`advanced-hunting/device-inventory/`](advanced-hunting/device-inventory/).

### 🔍 Other EDR Platform Investigations
Four reference investigation queries (Defender-disabled devices, non-onboarded devices, npcap detection, SCCM client detection) written in a different query dialect (`devices` / `execution.events`), kept for reference. See [`other-edr-platform-investigations/`](other-edr-platform-investigations/) for details.

## How to run these queries

1. Sign in to the **Microsoft Defender XDR portal** at [security.microsoft.com](https://security.microsoft.com).
2. Go to **Hunting → Advanced hunting**.
3. Copy the contents of any `.kql` file from this repo into the query editor.
4. Adjust the OS platform filters, thresholds (e.g., `ago(7d)`, `ago(90d)`), or `ConfigurationId` values if your environment differs.
5. Run the query, then optionally save it, pin it to a dashboard, or turn it into a **custom detection rule**.

Each query file starts with a header comment block describing its title, category, description, tables used, and required data connector — so you can identify the right query without opening the Defender portal.

## Contributing

Contributions are welcome. If you have a Defender for Endpoint Advanced Hunting query that fills a gap in this repo (identity, cloud apps, email, or additional server hardening checks), open a pull request. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Released under the [MIT License](LICENSE).

---

**Related terms:** Defender for Endpoint hunting queries, MDE KQL, Microsoft 365 Defender hunting, Advanced Hunting query library, Windows Server security queries, KQL cheat sheet, threat hunting queries GitHub.

## Author
**Rittu Vijai** — Senior Cloud Operations Engineer & SRE (Dallas-Fort Worth Metroplex)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rittuvijai)
