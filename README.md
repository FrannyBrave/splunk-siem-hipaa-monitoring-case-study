# Splunk SIEM & HIPAA Security Monitoring Case Study

## Project Overview

This repository contains an independent cybersecurity implementation case study demonstrating the design, deployment, and validation of a Splunk Enterprise SIEM environment for a healthcare technology organization.

The project focuses on centralized log monitoring, automated threat detection, HIPAA audit reporting, executive security dashboards, role-based access control, and alerting workflows.

> This is an independent portfolio case study. Client name, infrastructure details, accounts, and screenshots have been anonymized for public presentation.

## Business Problem

The simulated healthcare technology environment lacked centralized security visibility. Logs were generated across Active Directory, file servers, and workstations without unified monitoring, automated alerting, or efficient compliance reporting.

Key challenges included:

- No centralized log visibility
- No automated alerting
- Manual incident investigation
- Manual HIPAA audit reporting
- Delayed detection of suspicious activity
- Limited executive visibility into security events

## Project Scope

The implementation focused on a pilot SIEM deployment covering:

- Active Directory Domain Controller
- Primary file server
- Developer workstation
- Splunk Enterprise 9.1.2
- Ubuntu 22.04 LTS
- VMware vSphere infrastructure
- Windows Security Event Logs
- HIPAA Audit Controls reporting
- Custom SPL detection rules
- Executive dashboards

## Methodology

The project followed the ADDIE framework:

1. Analysis
2. Design
3. Development
4. Implementation
5. Evaluation

## Deliverables

| Deliverable | Description |
|---|---|
| [SIEM Client Project Report](./reports/SIEM_Client_Project.pdf) | Portfolio-ready report covering the SIEM implementation, dashboard, detection rule, HIPAA audit sample, and testing outcomes |
| [Project Background Document](./reports/Splunk_SIEM_Implementation_Project_Background.docx) | Original academic project background and implementation documentation |
| [Executive Security Dashboard](./screenshots/executive-security-dashboard.png) | Anonymized Splunk-style dashboard showing security metrics, alerts, failed logins, and user activity |
| [Splunk Alert Configuration](./screenshots/splunk-alert-configuration.png) | Alert configuration screen for the brute-force authentication detection rule |
| [CR-AUTH-001 Detection Rule](./detection-rules/CR-AUTH-001-brute-force-detection.spl) | SPL query for detecting brute-force authentication behavior |

## Key Technical Components

- Splunk Enterprise SIEM deployment
- Splunk Universal Forwarder configuration
- Secure log ingestion using TLS
- Windows Security Event Log monitoring
- Role-Based Access Control
- MFA for privileged SIEM roles
- SPL correlation rule development
- Email alerting configuration
- HIPAA file access audit reporting
- Executive security dashboard development

## Detection Rule Highlight

### CR-AUTH-001: Brute Force Authentication Detection

This rule detects possible brute-force attacks by identifying patterns of multiple failed authentication attempts followed by a successful login within a short time window.

Detection logic includes:

- Windows Event ID 4625: Failed Logon
- Windows Event ID 4624: Successful Logon
- Failure threshold greater than 10 attempts
- 5-minute correlation window
- High-priority alert classification
- Email alert notification workflow

## Testing and Results

The SIEM environment was tested using simulated attack scenarios and compliance reporting workflows.

Documented outcomes included:

- Brute-force authentication simulation detected in 8 minutes
- Simulated ransomware activity detected in 12 minutes
- Lateral movement attempt detected in 9 minutes
- HIPAA audit report generated in 47 minutes
- 10 custom SPL detection rules developed
- Executive and compliance dashboards created
- RBAC and MFA implemented for SIEM access

## Skills Demonstrated

- SIEM implementation
- Splunk Enterprise
- SPL query development
- Security monitoring
- Log management
- Threat detection
- HIPAA audit reporting
- Windows event log analysis
- Role-based access control
- Security dashboard development
- Incident detection and alerting
- Technical documentation

## Disclaimer

This repository is for cybersecurity portfolio and educational purposes. The environment, client name, screenshots, accounts, and infrastructure details have been anonymized or simulated. No real patient data, production client data, or protected health information is included.
