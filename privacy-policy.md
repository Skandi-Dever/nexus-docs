# Nexus Management System - Privacy Policy

**Effective Date:** Jun 24, 2026  
**Version:** 1.0 (Production Release)  
**Producer:** Kernel 7 Group (Pty) Ltd

### 1. Identity and Scope
This Privacy Policy governs the data processing practices of the Nexus Management System ("the Software"), an enterprise management platform designed to replace spreadsheet-based record keeping for organizations of all sizes, from startups to large enterprises. This policy is specifically intended for the administrative organization ("the Client") utilizing the Software to manage their daily operations and personnel. 

The Software is owned, operated, and engineered by **Kernel 7 Group (Pty) Ltd** ("Kernel 7 Group"). This policy outlines the strict technical safeguards, data routing architectures, and API protocols implemented by Kernel 7 Group to ensure the Client's data integrity, sovereignty, and privacy.

### 2. Google API Data Usage, Sharing, and Disclosure
Nexus respects your privacy and is committed to protecting your organizational data. All data accessed via your Google account is used strictly to provide the application's core organizational functionality. **We do not share, transfer, sell, or disclose your personal information or Google user data to any third-party companies, advertisers, brokers, or external entities.** 

To facilitate synchronization, cloud backups, and multi-user collaboration, certain operational data (such as internal event records, organization data, and necessary Google object identifiers like eventIDs, fileIDs, or formIDs) are securely transmitted to and stored on our protected virtual private servers. This data remains strictly within the secure Nexus ecosystem, is accessible only to authorized administrators within your organization, and is never sold, traded, or monetized. 

Our use and transfer of information received from Google APIs to any other app will strictly adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

The Software requests the following scopes to facilitate specific automated workflows:
* **Google Drive (`drive.file`):** Utilized to programmatically create the "Nexus System" folder structure and securely store related operational files. The Software only accesses and manages files it generates; it does not read, modify, or delete unrelated private files within the Client's Google Drive.
* **Google Calendar (`calendar`):** Utilized to synchronize the Client's workspace by updating the calendar name to match the organization, scheduling internal events, and automatically dispatching event invitations to newly registered members.
* **Google Forms (`forms.body`):** Utilized to dynamically create, update, and manage member registration forms, and to securely read submitted form data back into Nexus' Pending Registrations section.
* **Gmail (`gmail.send`):** Utilized exclusively for outbound automated communications, such as dispatching welcome messages to newly approved members or routing user-initiated Bug Reports to the Kernel 7 Group engineering team. It does not read, monitor, or modify the Client's inbox.

### 3. Architecture, Hosting Modalities, and Data Residency
To maximize data sovereignty and accommodate varying security requirements, the Software operates under two distinct hosting modalities:

* **Modality A: Nexus-Hosted (Cloud Infrastructure)**
  If the Client opts for cloud hosting, their relational and document data is stored on secure, industry-standard cloud infrastructure managed by Kernel 7 Group. To ensure data integrity, Kernel 7 Group employs strict logical isolation; each Client is provisioned with dedicated, tenant-specific databases. Kernel 7 Group enforces strict internal access controls and expressly does not monitor, mine, sell, or interact with the Client's operational data.
* **Modality B: Self-Hosted (On-Premise)**
  If the Client opts to self-host, all transactional data and PII inputted into the Software is routed directly to the Client's privately owned servers. In this modality, Kernel 7 Group operates under a strict "Zero-Access" framework, retaining no physical, remote, or administrative access to the Client's databases. 
* **Google Data Routing (Both Modalities):**
  Regardless of the hosting modality chosen, the actual content of your Google Workspace flows directly between the Client's local Software installation and Google's servers. Minimal relational metadata is synchronized with your chosen database modality to link local records to Google objects.
* **Cross-Border Data Transfers:**
  In the Nexus-Hosted modality, the Client's tenant databases are currently hosted on secure infrastructure provided by DigitalOcean, physically located in London, United Kingdom. By selecting this modality, the Client acknowledges that operational data will be transferred across South African borders. Kernel 7 Group ensures that our infrastructure partners operate in jurisdictions governed by stringent data protection laws (such as the UK GDPR) that provide an adequate, equivalent level of protection to South African privacy standards.

### 4. Privacy by Design & POPIA Compliance
In accordance with the Protection of Personal Information Act (POPIA) of South Africa, the Software is engineered around the principles of privacy by design:

* **The Client (Responsible Party):** The Client retains full legal authority, ownership, and responsibility for the personal information of their organizational members. The Client is solely responsible for obtaining lawful consent to process this data and for responding to any Data Subject requests.
* **Processing of Minor Data:** The Software may process records that include the personal information of minors. The Client retains sole legal responsibility for obtaining verifiable, explicit consent from a competent person (parent or guardian) prior to inputting such data into the Software. Kernel 7 Group accepts no liability for data processed by the Client without lawful authorization.
* **The Operator (Kernel 7 Group):** In the Nexus-Hosted modality, Kernel 7 Group acts as the Operator, providing the infrastructure to process data strictly within the automated parameters of the Software. In the Self-Hosted modality, Kernel 7 Group does not act as an Operator, as no personal data is transmitted to our infrastructure.
* **Zero-Knowledge Architecture:** Critical architectural data—such as highly sensitive Google OAuth access tokens and root database connection URIs—are secured locally on the Client's hardware within a `settings.json` manifest. When synced to the cloud, this configuration undergoes strict Application-Level Encryption. Kernel 7 Group stores only mathematically scrambled ciphertext, ensuring we possess zero ability to read or decrypt your core infrastructure secrets.

### 5. Security and Incident Response
To protect the Client’s data against unauthorized access, alteration, or destruction, Kernel 7 Group implements the following technical safeguards:

* **Application-Level Data-at-Rest Encryption:** Sensitive local files and cloud-synced configuration payloads are secured using the Advanced Encryption Standard (AES). 
* **Encryption in Transit:** All network communication is strictly encrypted in transit utilizing industry-standard cryptographic protocols (SSL/TLS).
* **Secure Authentication (OAuth 2.0):** Integration with Google Workspace is authenticated exclusively via secure OAuth 2.0 token exchanges. 
* **Infrastructure Security:** Cloud database instances are fortified using authenticated connection strings, strict user-role access controls, and network-level firewalls.
* **Breach Notification Protocol:** In the event of a confirmed security breach compromising the Client's tenant database within the Nexus-Hosted infrastructure, Kernel 7 Group will notify the Client's administrators without undue delay, providing the necessary details for the Client to fulfill their statutory reporting obligations to the Information Regulator.

### 6. Telemetry and Diagnostic Data
Kernel 7 Group prioritizes a non-intrusive operational footprint:
* **Zero Background Tracking:** The Software operates silently. It does not collect, transmit, or monitor background usage telemetry, keystrokes, or anonymous analytics.
* **User-Initiated Bug Reports:** The only diagnostic data transmitted to Kernel 7 Group occurs when a user explicitly initiates a "Bug Report" from within the Software. These email-based reports transmit minimal system metadata (including the operating system version, Java runtime version, and organization name) alongside the user's message to assist in rapid technical troubleshooting.

### 7. Data Retention, Termination, and Deletion
* **Self-Hosted Modality:** The Client retains continuous access to their privately hosted databases and Google Workspace. Kernel 7 Group possesses no access to this data and plays no role in its retention or deletion.
* **Nexus-Hosted Modality:** The Client is strictly responsible for exporting their operational data prior to account termination. To comply with POPIA data minimization principles, Kernel 7 Group will securely and permanently delete the Client’s tenant-specific databases within 30 days following the termination of the service agreement.
* **Google API Revocation:** Upon uninstallation or termination, the Software's automated connection to the Client's Google API services will be severed. All files generated within the Client's Google Drive remain safely under the Client's control.
* **No Migration Liability:** Kernel 7 Group is not responsible for data retrieval, formatting, or migration to third-party platforms once the service agreement has ended.

### 8. Policy Updates and Contact Information
As the Nexus Management System continues to evolve, this Privacy Policy may be updated to reflect architectural enhancements or changes in regulatory requirements. When significant modifications occur, Kernel 7 Group will provide reasonable notice via the Software's internal notification system or the administrative email address on file. 

For technical inquiries, bug reporting, POPIA compliance questions, or concerns regarding data processing, please contact the Kernel 7 Group engineering team directly at: **skandiworker@gmail.com**

---

&copy; 2026 Kernel 7 Group (Pty) Ltd. All rights reserved.
