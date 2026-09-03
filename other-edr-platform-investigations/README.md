# Other EDR Platform Investigations (Reference Only)

⚠️ **Heads up:** the four queries in this folder are **not written in KQL / Defender for Endpoint Advanced Hunting syntax**. They use a `devices during past Nd` / `execution.events` query pattern that belongs to a different EDR/XDR query builder (commonly seen in platforms like Uptycs). They will **not run as-is** in the Microsoft Defender XDR Advanced Hunting editor.

They're kept here for reference and as a starting point if you want to **port the same detection logic to KQL** (e.g., using `DeviceProcessEvents` and `DeviceFileEvents` against the Defender for Endpoint schema instead of `execution.events`).

| File | Investigation intent |
|---|---|
| [`defender-disabled-devices.txt`](defender-disabled-devices.txt) | Windows devices with no Microsoft Defender process activity in 7 days |
| [`defender-not-onboarded-devices.txt`](defender-not-onboarded-devices.txt) | Windows devices with no firewall/Defender-related process activity in 30 days |
| [`npcap-installed-devices.txt`](npcap-installed-devices.txt) | Devices running the Npcap packet-capture driver |
| [`sccm-not-installed-devices.txt`](sccm-not-installed-devices.txt) | Windows devices with no SCCM client process activity in 30 days |

⬅ [Back to main README](../README.md)
