# Nexus Management System - Privacy Policy

**Effective Date:** Jun 6, 2026  
**Version:** 1.0 (Production Release)

### 1. Identity and Scope
This Privacy Policy governs the data processing practices of the Nexus Management System ("the Software"), an enterprise management platform. This policy is specifically intended for the administrative organization ("the Client") utilizing the Software to manage their daily operations and personnel. 

Currently, the Software is owned, operated, and maintained by an independent developer ("the Developer"). This policy outlines the strict technical safeguards, data routing architectures, and API protocols implemented by the Developer to ensure the Client's data integrity, sovereignty, and privacy.

### 2. Google API Disclosure (Limited Use)
Nexus utilizes Google OAuth 2.0 to provide core organizational functionality. Our use and transfer of information received from Google APIs to any other app will strictly adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

The Software requests the following scopes to facilitate specific automated workflows:

* **Google Drive (`drive`):** Utilized to programmatically create the "Nexus System" folder structure and securely store related operational files. The Software only accesses and manages files it generates; it does not read, modify, or delete unrelated private files within the Client's Google Drive.
* **Google Calendar (`calendar`):** Utilized to synchronize the Client's workspace by updating the calendar name to match the organization, scheduling internal events, and automatically dispatching event invitations to newly registered members.
* **Google Forms (`forms.body`):** Utilized to dynamically create, update, and manage member registration forms, and to securely read submitted form data back into Nexus' Pending Registrations section.
* **Gmail (`gmail.send`):** Utilized exclusively for outbound automated communications. This includes dispatching welcome messages to newly approved organizational members, as well as allowing system administrators to send automated diagnostic reports to the Developer for support purposes. It does not read, monitor, or modify the Client's inbox.

### 3. Architecture, Hosting Modalities, and Data Residency
To maximize data sovereignty and accommodate varying security requirements, the Software operates under two distinct hosting modalities. The handling of personally identifiable information (PII) depends entirely on the modality selected by the Client:

* **Modality A: Nexus-Hosted (Cloud Infrastructure)**
  If the Client opts for cloud hosting, their relational and document data is stored on secure, industry-standard cloud infrastructure managed by the Developer. To ensure data integrity, the Developer employs strict logical isolation; each Client is provisioned with dedicated, tenant-specific databases. The Developer enforces strict internal access controls and expressly does not monitor, mine, sell, or interact with the Client's operational data.
* **Modality B: Self-Hosted (On-Premise)**
  If the Client opts to self-host, all transactional data and PII inputted into the Software is routed directly to the Client's privately owned servers. In this modality, the Developer operates under a strict "Zero-Access" framework, retaining no physical, remote, or administrative access to the Client's databases. 
* **Google Data Routing (Both Modalities):**
  Regardless of the database hosting modality chosen, all data interacting with Google APIs (such as Drive files, Forms, and Calendar events) flows directly between the Client's local Software installation and their secure Google Workspace. This data bypasses the Developer's database infrastructure entirely.

### 4. Privacy by Design & POPIA Compliance
In accordance with the Protection of Personal Information Act (POPIA) of South Africa, the Software is engineered around the principles of privacy by design. Legal responsibilities are strictly delineated based on the Client’s chosen hosting modality:

* **The Client (Responsible Party):** Regardless of the hosting modality, the Client retains full legal authority, ownership, and responsibility for the personal information of their organizational members. The Client is solely responsible for obtaining lawful consent to process this data and for responding to any Data Subject requests (e.g., requests to access, modify, or delete personal records). 
* **The Developer (Operator):** In the **Nexus-Hosted** modality, the Developer acts as the Operator, providing the infrastructure to process data strictly within the automated parameters of the Software. The Developer will only process data as directed by the Client's use of the Software. In the **Self-Hosted** modality, the Developer does not act as an Operator, as no personal data is transmitted to or processed by the Developer's infrastructure.
* **Decentralized Configuration:** To further minimize centralized risk, critical system pathing and Google resource identifiers are never uploaded to the cloud. They are stored strictly within a local `settings.json` manifest on the Client's authorized hardware.
* **Data Subject Rights:** The Software provides the necessary administrative tools (CRUD operations) for the Client to seamlessly execute any member requests for data modification or deletion, ensuring the Client can fulfill their statutory POPIA obligations.

### 5. Security and Data Safeguards
To protect the Client’s data against unauthorized access, alteration, or destruction, the Developer implements the following technical safeguards:

* **Encryption in Transit:** All network communication—whether interacting with Google Cloud APIs or synchronizing with the Developer’s cloud infrastructure (in the Nexus-Hosted modality)—is strictly encrypted in transit utilizing industry-standard cryptographic protocols (SSL/TLS).
* **Secure Authentication (OAuth 2.0):** Integration with Google Workspace is authenticated exclusively via secure OAuth 2.0 token exchanges. The Software never asks for, processes, or stores the actual Google account passwords of the Client or its administrators.
* **Infrastructure Security:** In the Nexus-Hosted modality, cloud database instances are fortified using authenticated connection strings, strict user-role access controls, and network-level firewalls to prevent unauthorized external intrusion.
* **Local Credential Masking & Storage:** Sensitive connection URIs, database passwords, and system architecture keys stored in the Client's local `settings.json` file are visually masked within the user interface to prevent "shoulder-surfing" and unauthorized physical exposure.

### 6. Data Retention, Termination, and Deletion
Upon termination of the service agreement or uninstallation of the Software, data retention and retrieval responsibilities are determined by the Client's selected hosting modality:

* **Self-Hosted Modality:** The Client retains continuous, uninterrupted access to their privately hosted databases and Google Workspace. The Developer possesses no access to this data and plays no role in its retention or deletion.
* **Nexus-Hosted Modality:** The Client is strictly responsible for exporting their operational data prior to account termination. To comply with POPIA data minimization principles, the Developer will securely and permanently delete the Client’s tenant-specific databases within 30 days following the termination of the service agreement.
* **Google API Revocation:** Upon uninstallation or termination, the Software's automated connection to the Client's Google API services will be severed. All files, forms, and reports generated by the Software within the Client's Google Drive remain safely under the Client's ownership and control.
* **No Migration Liability:** Under no circumstances is the Developer responsible for data retrieval, formatting, or migration to third-party platforms once the service agreement has ended.

### 7. Policy Updates and Contact Information
As the Nexus Management System continues to evolve, this Privacy Policy may be updated to reflect architectural enhancements, changes in South African regulatory requirements, or the formal incorporation of the Developer into a registered corporate entity (e.g., a Pty Ltd). 

When significant modifications to data processing protocols occur, the Developer will provide reasonable notice to the Client's administrators via the Software's internal notification system or the administrative email address on file. 

For technical inquiries, bug reporting, POPIA compliance questions, or concerns regarding data processing, please contact the Developer directly at: **skandiworker@gmail.com**
