# AWS Migration Security Assessment and Threat Mitigation

**Course:** CYB350 Introduction to DevOps and Project Management · ECPI University · Jul 2026  
**Work:** Individual

## Scenario

A security assessment for moving a Java web application to AWS (EC2, RDS, CodePipeline, IAM): threats such as stolen credentials, mitigations and how they support the availability and recovery targets.

## Skills and tools

- **Skills:** Cloud security, Threat modeling, IAM
- **Tools and references:** AWS EC2, AWS RDS, AWS CodePipeline, AWS IAM

## My work

*Converted from my original submission. The assignment prompt, grade and instructor feedback are not included.*

**5.4 Project: Security Assessment**

**5.4 Project: Security Assessment**

ACME Cloud Corp is moving a Java web application from an on-premises system to Amazon Web Services. The goal is to make releases faster, more consistent, and easier to recover when something goes wrong. Amazon EC2 will run the application, Amazon RDS will store the data, AWS CodePipeline will handle builds and deployments, and AWS Identity and Access Management will control access. The project expects about four releases each month, 99.9 percent availability, a four-hour recovery time, and no more than one hour of lost data. The yearly AWS cost should stay under $25,000.

The first threat is stolen login information. An attacker could trick an employee with a phishing email, steal a password or access key, or find a secret in source code or a build log. The attacker could then enter AWS, view data, or change the system. ACME should require multifactor authentication, use separate named accounts, give each person and service only the access it needs, and avoid long-term access keys (Amazon Web Services, 2025). Passwords and application secrets should be stored in AWS Secrets Manager and changed regularly. The team should also watch for unusual sign-ins, new accounts, and unexpected permission changes.

The second threat is a compromised development pipeline. An attacker could add harmful code through a stolen developer account, a bad third-party library, or a changed pipeline file. To lower this risk, ACME should protect the main branch, require another developer to review changes, and block direct changes to production. The pipeline should scan the code for known security problems, exposed secrets, and unsafe dependencies (OWASP, 2025). Only the same tested build should move into production, and the person who wrote a change should not be the only person approving it.

The third threat is a cloud setup mistake. A security group could be opened to everyone, the database could be made public, or a storage policy could allow the wrong users to read files. ACME should keep RDS in a private network, allow only required ports, encrypt data, and block public access to storage. Cloud settings should be written as code and reviewed before deployment. Automatic checks should reject unsafe settings, and the team should compare the real AWS setup with the approved design each week so that mistakes are found quickly.

The fourth threat is a weakness in the Java application or one of its libraries. Problems such as SQL injection, broken access checks, unsafe input, or an outdated library could let an attacker reach the application or database. Developers should use secure coding rules, review every pull request, and run code, dependency, and web-application scans during the pipeline. Critical problems should be fixed before release. EC2 should also be patched, the application should use a limited AWS role, and a web application firewall should block common attacks.

The fifth threat is damage to the database. A hacker, bad code update, or simple mistake could delete, encrypt, or corrupt RDS data. ACME should turn on automatic backups, point-in-time recovery, encryption, and deletion protection. Only a few approved roles should be able to delete a database or backup (AWS, 2024). The team should check backups every month and perform a test restore every quarter. This is important because a backup is only useful if the team knows it can restore the application within the four-hour recovery goal.

These protections need clear team rules. All code, cloud setup files, database changes, and pipeline files should go through a pull request. Normal changes need at least one reviewer, while major access, network, database, or pipeline changes need a second security or cloud reviewer (AWS, 2025). The architecture should be reviewed before the test launch, before the production launch, after major design changes, and every quarter during the first year. Security tests should run with every build, and stronger web and vulnerability tests should run before each production release. Access reviews, backup restores, and incident practice exercises should happen every quarter. If the team must skip a control, the project manager, security lead, and system owner must approve the reason, temporary protection, owner, and end date.

When a security event happens, the project manager or operations manager should lead the response. The security lead should investigate and guide containment, the DevOps lead should isolate cloud resources and stop unsafe deployments, and the application and database leads should check code and data. The team should open an incident record for unauthorized production access, a harmful pipeline change, public data exposure, a serious application attack, database damage, or an outage longer than 30 minutes. The record should include the time, affected systems, business impact, actions taken, and the people responsible.

The first response step is to collect and protect evidence from CloudTrail, CloudWatch, GuardDuty, CodePipeline, EC2, the application, and RDS. Next, the team should find out how the attacker entered, which accounts and systems were affected, and whether data was viewed or changed. Containment may include disabling an account, changing passwords and keys, stopping the pipeline, blocking an IP address, closing a security-group rule, placing the application in read-only mode, or isolating an EC2 instance (AWS, 2026). The team should save evidence before shutting down a system when it is safe to do so.

The exact response will depend on the threat. For a stolen account, ACME should revoke sessions, disable keys, change all secrets the account could reach, and remove any new users or permissions created by the attacker. For a pipeline attack, the team should stop deployments, preserve the code and build records, find the first unsafe change, rebuild from a trusted version, and scan the new build before release. For a cloud setup mistake, the unsafe setting should be closed immediately, logs should be checked for access during the exposure, and the approved setup should be redeployed from code. For an application attack, ACME should block the attack, isolate affected servers, patch the weakness, rebuild the server from a trusted image, and rotate secrets that may have been exposed.

A database incident needs extra care because restoring the wrong copy could cause more damage. The team should stop writes, protect the current database and logs, and restore a known-good point to a new RDS instance (Nelson et al., 2025). The database and business owners should check important records and decide whether any recent transactions were lost. Before returning to normal, ACME must confirm that the attack path is closed, passwords and keys are changed, the application and cloud setup match an approved version, security tests pass, logging and backups work, and the system is stable. Service should return in stages while the team watches closely.

During the incident, updates should be short, factual, and approved. The security and legal teams should decide whether customers, regulators, insurance providers, law enforcement, or AWS Support must be contacted. After recovery, the team should review what happened, what controls failed, what worked, and what needs to change. Every improvement should have an owner and due date. This assessment gives ACME a simple plan for preventing the five main threats and responding when prevention is not enough. Stakeholder approval will allow the team to treat failed security checks as release blockers and keep security part of the normal DevOps process.

**References**

Amazon Web Services. (2025). Use multi-factor authentication with your identities - AWS identity and access management. In *Amazon.com*. https://docs.aws.amazon.com/IAM/latest/UserGuide/gs-identities-mfa.html

AWS. (2024). Working with backups - amazon relational database service. In *docs.aws.amazon.com*. https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER\_WorkingWithAutomatedBackups.html

AWS. (2025). Security best practices - AWS CodePipeline. In *Amazon.com*. https://docs.aws.amazon.com/codepipeline/latest/userguide/security-best-practices.html

AWS. (2026). *Amazon elastic compute cloud (Amazon EC2) controls - AWS control tower*. Amazon.Com. https://docs.aws.amazon.com/controltower/latest/controlreference/ec2-rules.html

Nelson, A., Rekhi, S., Souppaya, M., & Scarfone, K. (2025). Incident response recommendations and considerations for cybersecurity risk management: *NIST*. https://doi.org/10.6028/nist.sp.800-61r3

OWASP. (2025). Owasp Dependency-Check project | owasp. In *owasp.org*. https://owasp.org/www-project-dependency-check/
