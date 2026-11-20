# Breach Lessons Learned: Governance, Mitigation and Accountability (team project)

**Course:** CYB250 Principles of Cybersecurity · ECPI University · Sep 2025  
**Work:** Team project (classmates’ names removed)

## Scenario

A four-person team analyzed a real third-party cloud data breach and presented governance gaps (NIST SP 800-63-3 authentication assurance), mitigations and team responsibilities.

## Skills and tools

- **Skills:** Post-incident review, Security governance, Identity assurance, Presentation
- **Tools and references:** NIST SP 800-63-3, MFA / AAL2-AAL3

## My work

*Converted from my original submission. The assignment prompt, grade and instructor feedback are not included.*

##### Slide 1

- 3.10 Lessons Learned from BreachCYB250 Principles of CybersecurityAugust 10, 2025
- [classmate]
- [classmate] &
- [classmate], Jr.

##### Slide 2

- Agenda
- Security Governance
- -
- Mitigation
- -
- Team Responsibility

##### Slide 3

- Governance
- NIST SP 800-63-3
- AAL2 and AAL3
- FICAM
- KMS

> Speaker notes: Governance during the breach viewed through the National Institute of Standards and Technology Special Publication 800-63-3, shows major gaps in leadership oversight that weakened cybersecurity defenses. Their third party vendor Snowflake’s posture did not meet Authentication Assurance Levels (AAL2 and AAL3), which require multi-factor authentication (MFA) and verifier impersonation resistance. This security feature protects users from authenticating to a malicious verifier, such as a fake login portal, and is critical for preventing phishing and adversary-in-the-middle attacks. To mitigate these types of attack, MFA should be enforced for all users , which is a requirement using AAL2, using two different authentication factors such as a password and biometric or token. For AAL3, phishing-resistant authenticators like hardware security keys or certificate-based authentication should be implemented along with identity proofing that meets NIST SP 800-63A standards, including biometric binding and reauthentication timeouts (NIST, U.S. Dept. of Commerce, 2020).  At AT&T, leadership failed to enforce credential management and federated identity governance - both core to NIST’s digital identity framework. Utilizing the Federal Identity, Credential, and Access Management (FICAM) Framework which offers standardized processes for issuing, validating, and revoking credentials. (Lam, 2020). Implementing Privileged Identity Management (PIM) for monitoring and rotating credentials, especially for high-risk roles.  Some the  key control failures include a lack of multi-factor authentication (MFA), no Annual Loss Expectancy calculations (ALE) , and weak vendor oversight. Applying FICAM principles to third-party access, monitoring login activity for anomalies, and allowing only trusted systems onto the network could have minimized the risk. Hardware Security Modules (HSM) and a centralized Key Management System (KMS) with controls for secure generation, rotation, and revocation of keys would have provided more robust protection. With guidance from the Open Worldwide Application Security Project (formerly the Open Web Application Security Project), a non-profit organization founded in 2001 with a mission to improve the security of software through open-source projects, community-led initiatives, and educational resources, such as the OWASP Key Management Cheat Sheet, would've provided the best practices for creating, storing, and rotating keys securely.  The breach illustrates how leadership’s failure to align with federal standards, enforce policy, and oversee identity and key management contributed to the breakdown of defenses. NIST SP 800-63-3 stresses that identity proofing, authenticators, authentication protocols, and federation must be consistently applied to maintain a strong security posture (NIST, U.S. Dept. of Commerce, 2020).   (INTRO. Marvin)  AAL2 and AAL3 - Authentication Assurance Levels  ALE - Application Layer Encryption ALE - Annual Loss Expectancy = a way to estimate how much money a company might lose each year due to a specific risk or threat:     ALE = SLE × ARO (Single Loss Expectancy) & (Annual Rate of Occurrence) FICAM - Federated Identity, Credential, and Access Management  HSM - Hardware Security Module KMS - Key Management Systems  MFA - Multi-Factor Authentication  NIST SP 800-63-3 - National Institute of Standards and Technology Special Publication  OWASP - Open Worldwide Application Security Project (formerly the Open Web Application Security Project), a non-profit organization founded in 2001 with a mission to improve the security of software through open-source projects, community-led initiatives, and educational resources PIM - Privileged Identity Management

##### Slide 4

- Mitigation

> Speaker notes: A comprehensive analysis of the AT&T data breach requires a clear distinction between reactive damage control and proactive security measures. Proactive controls are preventative and are implemented to stop a breach from occurring. However, once a breach is discovered, a new set of proactive measures can be initiated as part of the incident response process to anticipate an attackers next actions and prevent further harm.   After a massive dataset impacting 73 million current and former customers surfaced on the dark web, AT&T took one significant proactive containment step to mitigate the immediate threat posed by the leaked data.   AT&T didn’t wait for active account takeovers. Recognizing that the leaked dataset contained encrypted but 4-digit passcodes, the company reset the passcodes for all 8 million currently active accounts identified in the breach. (Whittaker, 2024). This measure was designed to neutralize the immediate threat of attackers using the credentials for account takeovers or credential stuffing attacks. This action aligns with the “Containment, Eradication, & Recovery” phase of the incident response lifecycle, prioritizing preventing additional damage (Cichonski et al., 2012).   Proactive security model like ZTA would have limited the breach's impact. Instead of trusting internal network traffic, ZTA operates on the principle of least privilege, on a need-to-know basis, and is continuously verified. If this was previously implemented, a single compromised credential or system would not have been the sweeping access required to exfiltrate a dataset of 73 million records. (Rose et al., 2020).

AT&T also provided free credit monitoring and identity theft protection services through Experian to al affected individuals. This was a measure to help customers mitigate the personal financial risk and harm from their personal data being exposed.   An organization should not wait for a breach to occur or be reported. It implements Information Security Continuous Monitoring (ISCM) to hunt for threats. This involves using advanced tools to analyze data access patterns, network traffic, and user behavior to detect anomalies. In this event, an unusual transfer of massive datasets occurred. This allows the incident response team to intervene and mitigate the breach as it happens, rather than learning about it months later. (Dempsey et al., 2011).

##### Slide 5

- Team Responsibility

> Speaker notes: [classmate]: (Security Governance Research Lead) -  Conducted a thorough research on security governance. Leverages his knowledge and experience to provide insights on governance models. He will be conducting another research on Applications defense next week.   Marvin: (Threat Mitigation Research Lead ) Investigates current threat mitigation strategies. Applies his own expertise to evaluate the effectiveness of various mitigation techniques. Contributed a detailed analysis on risk reduction and incident response planning. He will conduct another research on vulnerabilities next week.   [classmate]: (Team Coordination and Participation Facilitator) –  Oversees overall team collaboration and ensures active participation from all members. Documents team decisions and ensures alignment with project goals. She will be doing the same thing next week.   [classmate]: (Editing & Presentation Specialist) -Responsible for refining written content to ensure clarity , coherence and academic tone. Formats and designs presentation slides for visual impact and consistency. Integrates contributions from all members into a unified and professional final deliverable. He will conduct a research and do editing next week.

##### Slide 6

- References
- Cichonski, P., Millar, T., Grance, T., & Scarfone, K. (2012). Computer security incident handling guide. Computer Security Incident Handling Guide, 2(2). https://doi.org/10.6028/nist.sp.800-61r2
- Dempsey, K., Shah Chawla, N., & Johnson, A. (2011). Information Security Continuous Monitoring (ISCM) for Federal Information Systems and Organizations. Ploughshares, 37(4), 11–17. https://doi.org/10.1353/plo.2011.0093
- Lam, T. N. (2020, June n/a). DoD Enterprise Identity, Credential, and Access Mgmt. (ICAM) Refernce Design. DoD Enterprise Identity, Credential, and Access Mgmt. (ICAM) Refernce Design(1.0). US Department of Defense. Retrieved August 12, 2025, from chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://dodcio.defense.gov/Portals/0/Documents/Cyber/DoD_Enterprise_ICAM_Reference_Design.pdf
- NIST, US Dept. of Commerce. (2020, March 2). NIST Special Publication 800-63-3. Digital Identity Guidelines(Revision 3). Gaithersburg, MD, USA East: US Dept. of Commerce. Retrieved August 12, 2025, from https://pages.nist.gov/800-63-3/sp800-63-3.html#:~:text=These%20guidelines%20provide%20technical%20requirements,Publication%20800%2D63%2D2
- Rose, S., Borchert, O., Mitchell, S., & Connelly, S. (2020). Zero trust architecture. NIST Special Publication 800-207, 800-207. https://doi.org/10.6028/nist.sp.800-207
- Whittaker, Z. (2024, March 30). AT&T resets account passcodes after millions of customer records leak online. TechCrunch. https://techcrunch.com/2024/03/30/att-reset-account-passcodes-customer-data/
