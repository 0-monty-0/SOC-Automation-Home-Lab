# SOC-Automation-Home-Lab

This project demonstrates a fully automated Security Operations Center (SOC) workflow that detects, enriches, and responds to security incidents. The lab integrates Wazuh for threat detection, Shuffle for automation, and TheHive for case management.

The environment simulates real-world security operations by generating malicious activity and automating incident response.

## Version
02/18/2025

## Authors
Authored by [Sheila Montecino](https://github.com/0-monty-0), [Steven Mah](https://www.mydfir.com/)

## Architecture
The following diagram shows the workflow of the SOC automation pipeline:

![SOC Architecture](SOC-Automation-Project-Diagram.png)

The Windows endpoint sends logs to the Wazuh manager, which triggers alerts. Alerts are forwarded to Shuffle, where automated enrichment and response workflows occur. Enriched alerts are then sent to TheHive for incident tracking and investigation.

## Objectives
- Simulate real-world SOC workflows
- Detect credential dumping attacks
- Automate incident enrichment and response
- Reduce manual alert triage
- Gain hands-on experience with SIEM and SOAR tools
  
### Tools & Technologies 
- Oracle VirtualBox with Windows 11 pro (endpoint simulation)
- Vultr (Virtualization and cloud infastructure)
- Wazuh (SIEM and endpoint detection)
- Apache Cassandra (backend database)
- Elasticsearch (log storage and search) 
- TheHive (incident response and case management)
- Shuffle (SOAR and automation)
- VirusTotal (threat intelligence enrichment)

## Lab Setup

The lab environment was built using virtual machines and cloud infrastructure.

### Steps:
1. Deployed Windows 11 endpoint and installed Wazuh agent.
2. Configured Wazuh manager for centralized log monitoring.
3. Installed and configured Elasticsearch.
4. Set up TheHive and connected Cassandra.
5. Created Shuffle workflows for automation.
6. Integrated VirusTotal API for threat intelligence.

## Attack Simulation

Credential dumping was simulated using Mimikatz to generate malicious activity.

The attack triggered:
- Endpoint alert in Wazuh
- Automated workflow in Shuffle
- Hash enrichment via VirusTotal
- Case creation in TheHive
- Email alert notification

## Automation Workflow

Shuffle was configured to:

- Receive alerts from Wazuh via webhook
- Extract malicious hash values
- Perform threat intelligence enrichment
- Send automated email alerts
- Create incident cases in TheHive

## Screenshots

### Wazuh Alert
![Alert](./images/wazuh-alert.png)

### Shuffle Workflow
![Workflow](./images/shuffle.png)

### TheHive Case
![TheHive](./images/thehive.png)

## Challenges & Troubleshooting

- Resolved Elasticsearch connectivity issues.
- Troubleshot service failures during TheHive setup.
- Debugged webhook communication between Wazuh and Shuffle.
- Fixed network configuration and firewall rules.

## Future Improvements

- Add brute-force and lateral movement attack simulations
- Integrate additional threat intelligence sources
- Implement automated endpoint isolation
- Deploy the lab fully in the cloud
- Add Slack or SIEM dashboards

## Lessons Learned

This project strengthened my understanding of:

- SOC workflows and incident lifecycle
- Threat detection and automation
- SIEM and SOAR integration
- Real-world troubleshooting and system configuration

