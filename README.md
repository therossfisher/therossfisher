# Ross Fisher

**Network Engineer | Cloud Security**

20 years in telecommunications, the last four provisioning and troubleshooting enterprise Layer 2 and Layer 3 services on Nokia carrier-grade MPLS platforms across a four-state footprint. These days I spend my own time on the cloud side of the same problem: Terraform, containers, and CI/CD pipelines that refuse to merge until the security scan passes.

Most of what's here is infrastructure I built, broke, and rebuilt until I understood it.

## Certifications

| | | |
|---|---|---|
| **GCIH** | GIAC Certified Incident Handler | Active through Apr 2029 |
| **GSEC** | GIAC Security Essentials | Active through Dec 2028 |
| **GISF** | GIAC Information Security Fundamentals | Active through Sep 2028 |
| **GFACT** | GIAC Foundational Cybersecurity Technologies | Active through Mar 2028 |
| **Advisory Board** | GIAC Advisory Board Member | Active through Dec 2028 |
| **AWS SAA-C03** | Solutions Architect Associate | In progress, 2026 |

## Projects

### terrapot
A cloud-native honeypot and threat intelligence platform, provisioned entirely as code. 42 AWS resources in modular Terraform with S3 remote state, Docker Compose services, and a GitHub Actions pipeline that gates every merge on Checkov policy scanning, with each finding either remediated or accepted in writing.

Runs live Cowrie SSH and DShield web sensors on EC2, with threat intelligence enrichment through Lambda and AbuseIPDB, canary alerting built on CloudTrail and EventBridge, and log aggregation in Grafana, Loki, and Promtail.

The instance gets destroyed between working sessions, so nothing a rebuild would lose is allowed to live on the box. Every design decision in the repo follows from that one constraint.

[Repository](https://github.com/therossfisher/terrapot) · [Full writeup](https://www.therossfisher.xyz/terrapot/)

### DShield sensor for the SANS Internet Storm Center
A Raspberry Pi 4 running Cowrie SSH and Telnet honeypots alongside Suricata 7 with the Emerging Threats ruleset, reporting continuously to the SANS ISC. I use the live telemetry to document active attack campaigns, including Redtail cryptominer and Outlaw/mdrfckr IRC botnet activity.

[Live dashboard](https://dashboard.therossfisher.xyz)

## Stack

**Networking**  Nokia 7750 SR and IXR, Nokia NFMP, MPLS/VPLS, Metro-Ethernet, BGP, WAN circuit provisioning

**Cloud and IaC**  AWS (EC2, S3, Lambda, VPC, IAM, CloudTrail, EventBridge), Terraform, Docker, GitHub Actions, Checkov

**Security and observability**  Suricata, Cowrie, DShield, Wireshark, Grafana, Loki, Promtail, incident handling

## Elsewhere

[therossfisher.xyz](https://therossfisher.xyz) · [LinkedIn](https://linkedin.com/in/rossfish)
