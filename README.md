🛡️ Wazuh Queries
A curated collection of Wazuh detection queries built around real-world security scenarios. These queries are designed to help SOC analysts and security engineers detect suspicious activity, monitor critical events, and respond to threats faster across cloud and endpoint environments.

📋 Overview
This repository contains custom Wazuh queries focused on:

Microsoft 365 / Office 365 security events
Identity and access anomalies
Email and phishing threats
File and data activity monitoring
Account modification tracking

Each query is organized by scenario and can be adapted to your own Wazuh / OpenSearch / Kibana environment.

📂 Available Queries
QueryDescriptionAdmin RoleDetects admin role assignments and privilege changes in Office 365File Accessed ExternalMonitors external file access events for potential data exposureFileMalwareDetectedAlerts when malware is detected in uploaded or shared filesMass File DownloadedIdentifies bulk file download activity (possible exfiltration)Phishing Urgent Action RequiresDetects phishing emails using urgency-based social engineeringSuspicious Inbox Rule CreationFlags unusual mailbox rules often used to hide attacker activityTravellersDetects logins from unusual or impossible geographic locationsUPDATE USER (MFA-LastDirSyncTime-StsRefresh...)Tracks changes to user account attributes (MFA, sync, tokens)User Login FailedAlerts on failed login attempts and brute-force patterns

🚀 Getting Started
Prerequisites

A running Wazuh deployment (manager + agents)
Access to the Wazuh Dashboard or OpenSearch / Kibana
Proper log sources configured (e.g., Office 365 module, Sysmon, audit logs)

How to Use

Clone the repository

bash   git clone https://github.com/x1y0x0y1/Wazuh.git
   cd Wazuh

Open the query file for the scenario you need.
Copy the query into your Wazuh Dashboard, OpenSearch Dashboards, or Kibana Discover view.
Adjust filters (timeframe, index pattern, organization-specific fields) to match your environment.
Save it as a search or build a dashboard / alert rule around it.


🧩 Query Structure
Each query is built to be:

✅ Readable — clear field names and logical structure
✅ Adaptable — easily tuned to your tenant or environment
✅ Scenario-driven — mapped to real attack techniques (MITRE ATT&CK where applicable)


🤝 Contributing
Contributions are very welcome! If you have a new scenario, a tuning improvement, or a false-positive reduction tip:

Fork this repository
Create a new branch (git checkout -b feature/new-query)
Add your query with a clear filename and description
Open a Pull Request

Please make sure any sample data is anonymized — no real IPs, usernames, or tenant IDs.

⚠️ Disclaimer
These queries are provided as-is for educational and defensive security purposes. Always test in a non-production environment before deploying. Tune thresholds and field mappings to fit your own infrastructure to avoid false positives.

📚 Useful Resources

Wazuh Documentation          >> https://documentation.wazuh.com/
Wazuh Office 365 Module      >> https://documentation.wazuh.com/current/user-manual/capabilities/office365/index.html
MITRE ATT&CK Framework       >> https://attack.mitre.org/
OpenSearch Query DSL         >> https://opensearch.org/docs/latest/query-dsl/


📬 Contact
Maintained by @x1y0x0y1
If you have questions, suggestions, or want to discuss detection engineering — feel free to open an issue.

⭐ If this repo helps your detection work, consider giving it a star!
