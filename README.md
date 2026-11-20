# Cybersecurity Coursework Portfolio

Selected work from my B.S. in Cybersecurity at ECPI University, chosen for Security Operations Center (SOC) analyst roles. Each folder holds one project or lab report, converted from my original submission.

**How this repository is put together**

- Assignment prompts are summarized in my own words; course materials are not reproduced.
- Grades and instructor feedback are not included.
- Classmates’ and instructors’ names are removed, and screenshots are redacted.
- Team projects are labeled as team work.

## Incident response and detection

Investigating suspicious activity, analyzing malware behavior and turning findings into reports and lessons learned. My Splunk SOC home lab is the hands-on SIEM companion to this section.

- **[AI-Assisted Incident Investigation and Live Response Report](01-incident-response-and-detection/ai-assisted-incident-investigation/)** (CST440): Suspicious activity across simulated lab systems was investigated over four weeks with network discovery, packet capture, live response and malware analysis; the final report validates the manual findings with an Isolation Forest anomaly-detection model.
- **[Malware Analysis and Threat Intelligence: Static and Dynamic Analysis](01-incident-response-and-detection/malware-analysis-and-threat-intelligence/)** (CST440): Suspicious traffic in a containerized Ubuntu environment was examined with static analysis (file inspection, strings, hashing) and dynamic analysis (strace, lsof, tcpdump, process monitoring) to identify anomalous communications and indicators.
- **[Breach Lessons Learned: Governance, Mitigation and Accountability (team project)](01-incident-response-and-detection/breach-lessons-learned-team/)** (CYB250, team): A four-person team analyzed a real third-party cloud data breach and presented governance gaps (NIST SP 800-63-3 authentication assurance), mitigations and team responsibilities.

## Threat analysis and vulnerability assessment

Reconnaissance, vulnerability validation and attack techniques, each mapped to defenses. Understanding how attacks work is what lets a SOC analyst recognize them in logs and alerts.

- **[Penetration Test Final Report: Simulated Web, Windows Domain and Linux Tiers](02-threat-analysis-and-vulnerability-assessment/penetration-test-final-report/)** (CYB410L): An authorized penetration test of an isolated lab that simulates a company's web, Windows domain and Linux service tiers, written up as a client report with an executive summary, attack path and prioritized remediation plan.
- **[Ethical Hacking Workflow: From Attack Surface to Evidence-Based Defense](02-threat-analysis-and-vulnerability-assessment/ethical-hacking-workflow-presentation/)** (CYB400L): A final presentation that ties five weeks of CEH labs into one workflow: reconnaissance, vulnerability validation, controlled exploitation, persistence and the defenses that break each stage.
- **[Reconnaissance Vulnerability Assessment Mapped to MITRE ATT&CK](02-threat-analysis-and-vulnerability-assessment/reconnaissance-assessment-mitre-attack/)** (CYB400L): A black-box footprinting assessment of a practice target using search engines, DNS and Whois, traceroute, email headers, recon-ng and AI-assisted recon, with findings mapped to MITRE ATT&CK and mitigations.
- **[System Hacking and Malware Threats Lab Report](02-threat-analysis-and-vulnerability-assessment/system-hacking-and-malware-threats/)** (CYB400L): A lab report on how attackers gain and keep access (Meterpreter sessions, privilege escalation, credential theft, persistence and covering tracks) and how defenders detect and prevent each step.
- **[Denial-of-Service Attacks and Layered Defenses Lab Report](02-threat-analysis-and-vulnerability-assessment/denial-of-service-attacks-and-defenses/)** (CYB400L): Transport-layer, volumetric and application-layer DoS techniques from the lab, linked to a state-sponsored campaign against the U.S. financial sector and CVE-2023-44487 (HTTP/2 Rapid Reset), with layered defense recommendations.
- **[Session Hijacking and Firewall/IDS Evasion Lab](02-threat-analysis-and-vulnerability-assessment/session-hijacking-and-ids-evasion-lab/)** (CYB410): Hands-on lab work hijacking sessions and testing firewall and IDS evasion techniques, documented with screenshots and a summary of detection takeaways.

## Windows, Active Directory and network defense

Hardening hosts, writing Group Policy baselines, building firewall rules and designing segmented networks.

- **[Security Audit Remediation Plan: Auditing and Patch Management](03-windows-ad-and-network-defense/audit-remediation-auditing-and-updates/)** (CYB300): A remediation project for audit findings on Windows and Linux hosts (no security auditing, automatic updates not configured), with requirements, validation steps, risk assessment and a back-out plan.
- **[Security Audit Remediation: Host Firewalls, DEP and pfSense Rules](03-windows-ad-and-network-defense/audit-remediation-firewalls-and-dep/)** (CYB300): Enabling Windows Firewall and Data Execution Prevention through GPO, configuring ufw on Linux, forwarding pfSense logs to syslog and building pfSense rules for Active Directory traffic, each with testing procedures.
- **[Group Policy Security Baseline Design for an Active Directory Domain](03-windows-ad-and-network-defense/group-policy-security-baseline/)** (CIS256L): A layered Group Policy plan for a fictional company domain: domain-wide password and account lockout policy, then OU-level settings to standardize and secure users and computers.
- **[Windows Accounts, Shared Folders and Security Monitoring Plan](03-windows-ad-and-network-defense/windows-accounts-shares-and-monitoring/)** (CYB240L): A four-phase Windows client and server project covering user and group design, shared-folder permissions, remote management and security monitoring and maintenance.
- **[Enterprise Network Build: Routing, Switching and Firewall Design (team project)](03-windows-ad-and-network-defense/enterprise-network-build-team/)** (CYB330L, team): A two-person project that designed and built a multi-site enterprise network in Packet Tracer, configuring routers, switches and firewalls and documenting the build in weekly journals.

## Cloud security

Security assessment for a workload moving to AWS.

- **[AWS Migration Security Assessment and Threat Mitigation](04-cloud-security/aws-migration-security-assessment/)** (CYB350): A security assessment for moving a Java web application to AWS (EC2, RDS, CodePipeline, IAM): threats such as stolen credentials, mitigations and how they support the availability and recovery targets.

## Related projects

- [Splunk SOC home lab](https://github.com/DrBarber13/soc-home-lab): containerized SOC lab with Splunk, SPL detections mapped to MITRE ATT&CK, a dashboard and an incident report.
- [Incident response case studies](https://github.com/DrBarber13/incident-response-case-studies)
- [Active Directory home lab](https://github.com/DrBarber13/active-directory-home-lab)
- [Microsoft 365 identity and security labs](https://github.com/DrBarber13/microsoft-365-identity-security-labs)
- [AWS security labs](https://github.com/DrBarber13/aws-security-labs)
- [PowerShell automation scripts](https://github.com/DrBarber13/powershell-automation-scripts)

