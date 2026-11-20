# Group Policy Security Baseline Design for an Active Directory Domain

**Course:** CIS256L Windows Active Directory Lab · ECPI University · Jul 2025  
**Work:** Individual

## Scenario

A layered Group Policy plan for a fictional company domain: domain-wide password and account lockout policy, then OU-level settings to standardize and secure users and computers.

## Skills and tools

- **Skills:** Active Directory, Group Policy design, Account security
- **Tools and references:** Active Directory, Group Policy Management

## My work

*Converted from my original submission. The assignment prompt, grade and instructor feedback are not included.*

**4.2 Capstone Project: Group Policy Object Planning Phase 4**

**4.2 Capstone Project: Group Policy Object Planning Phase 4**

This proposed plan aims to enhance security per future guidelines. It will also standardize user and computer environments, improve efficiency, and ensure regulatory compliance. The policies are designed using a layered approach: broad settings will be applied at the domain level, and more specific configurations will be applied at the organization unit (OU) level.

Domain-Level Policies

These policies apply to all authenticated users and computers within the wetdog.com domain. This policy will establish a baseline of security. The first line of defense against unauthorized access will be enforcing strong passwords and account lockout policies for all domain accounts. It will also ensure that the organization meets audit and compliance requirements for account security. A brief overview of the password and account lockout policies is as follows:

  - Password Policy
    
      - Minimum Length: 14 Characters
    
      - Complexity: Must contain all character types and numbers
    
      - History: Remembers the last 12 passwords

  - Account Lockout Policy
    
      - Lockout Threshold: 5 invalid logon attempts
    
      - Lockout Duration: 15 minutes

Workstation OU Policies

This policy applies to all hospital computer objects, ensuring a secure and standardized configuration regardless of who logs on. The main goal of this policy is to strengthen the operating system to reduce threats on all endpoints. We will also centralize management by making sure all workstations get critical updates and have a uniform security setup. Key points include forcing all workstations to retrieve updates from the local Windows Server Update Services (WSUS) server. It is also vital to configure a host-based firewall and set rules to allow traffic only for approved host-based applications. Using AppLocker to create a whitelist of approved applications will stop unauthorized software from running. Turning off USB storage to help prevent data theft and malware risks is also important.

Departmental OU Policies

This policy will standardize the user experience and create a consistent, professional environment for employees. It will also enhance data integrity by ensuring user data is backed up and accessible. This will be the location of the department's secure network file share. Additionally, we will have a separate administrator organizational unit (OU). They will ensure that admin users have the necessary tools and grant access to specific admin network resources. Admins will have a less restrictive experience, as this policy allows access to the entire desktop and control panel as needed for their roles, unlike other policies.

This Group Policy structure will give the domain a robust, scalable, and secure AD environment. The main benefit is improved security, as it implements a layered defense model that strengthens endpoints and enforces strong authentication. It also boosts efficiency by automating system and user configurations, reducing manual IT workload and enabling focus on more critical tasks.

---

**4.2 Capstone Project: Planning Phase 4**

**4.2 Capstone Project: Planning Phase 4**

Password policy requirements are essential for security. The policy is established as a standard or guideline for creating a strong, secure password, which, in theory, will protect sensitive information from unauthorized access. Compliance with the proposed policy is critical for maintaining security and the integrity of our infrastructure.

All passwords must have a minimum length of 14 characters; longer ones provide significantly higher protection against brute force attacks. Passwords must also contain characters from ALL of the categories below:

  - Uppercase letters: (A-Z)

  - Lowercase letters (a-z)

  - Numbers (0-9)

  - Special characters (<~!@#$%^&*()_-+={[}]|\:;"'<,>.?/>)

Users are also prevented from reusing their previous 12 passwords. This policy mitigates risks associated with the compromise of old passwords. Accounts will also temporarily lock for 15 minutes after five failed login attempts. This is implemented to decrease the possibility of automated brute-force attacks.

The system will also automatically reject passwords that are easily guessable words or patterns. The list includes, but isn’t limited to:

  - Passwords that are on a list of known compromised passwords.

  - Contains your username, first name, or last name

  - Common dictionary words such as “password” or “baseball”

  - Uses sequential or repetitive character (e.g., 12345, abcde, ccccc”

In addition to a strong encrypted password, Multi-Factor Authentication (MFA) will be mandatory for accounts, especially those with access to sensitive data or administrative privileges. MFA requires user to provide at least one additional verification factor to prove their identity, such as:

  - A code that is autogenerated from an authenticator app (e.g., Google Authenticator, Authy)

  - A physical security key (Titan Security Key)

  - A push notification sent to a pre-registered mobile device.

It is also recommended that you do the following for password management and protection:

  - Do not write down passwords or store them in unencrypted files. You must use an appropriate password manager to store credentials securely.

  - Do not share passwords with anyone, including IT staff or supervisors. No representative will ever ask you for your password.

  - Change your password immediately and report it to the security team if you suspect it has been compromised, no matter how small the vulnerability.

---

*First worksheet, exported as CSV:*

```csv
Site,Location,Room,Resource,Device Name
Bayside Memorial,,Server Room,Domain Controller,BaysideDC
Bayside Memorial,Administration,1,Client PC,BaysidePC-1-Admin
Bayside Memorial,Administration,2,Client PC,BaysidePC-2-Admin
Bayside Memorial,Administration,3,Client PC,BaysidePC-3-Admin
Bayside Memorial,Administration,4,Client PC,BaysidePC-4-Admin
Bayside Memorial,Administration,5,Client PC,BaysidePC-5-Admin
Bayside Memorial,Administration,6,Client PC,BaysidePC-6-Admin
Bayside Memorial,Administration,7,Client PC,BaysidePC-7-Admin
Bayside Memorial,Administration,8,Client PC,BaysidePC-8-Admin
Bayside Memorial,Administration,9,Client PC,BaysidePC-9-Admin
Bayside Memorial,Administration,10,Client PC,BaysidePC-10-Admin
Bayside Memorial,Administration,11,Client PC,BaysidePC-11-Admin
Bayside Memorial,Prep,Prep-1,Client PC,BaysidePC-Prep-1
Bayside Memorial,Prep,Prep-2,Client PC,BaysidePC-Prep-2
Bayside Memorial,Prep,Prep-3,Client PC,BaysidePC-Prep-3
Bayside Memorial,Prep,Prep-4,Client PC,BaysidePC-Prep-4
Bayside Memorial,Operating Room,OR-1,Tablet,BaysideTablet-OR-1
Bayside Memorial,Operating Room,OR-2,Tablet,BaysideTablet-OR-2
Bayside Memorial,Operating Room,OR-2,Tablet,BaysideTablet-OR-2
Bayside Memorial,Operating Room,OR-3,Tablet,BaysideTablet-OR-3
Bayside Memorial,Operating Room,OR-3,Tablet,BaysideTablet-OR-3
Bayside Memorial,Operating Room,OR-4,Tablet,BaysideTablet-OR-4
Bayside Memorial,Ward,Ward-1,Tablet,BaysideTablet-Ward-1
Bayside Memorial,Ward,Ward-2,Tablet,BaysideTablet-Ward-2
Bayside Memorial,Ward,Ward-3,Tablet,BaysideTablet-Ward-3
Bayside Memorial,Ward,Ward-4,Tablet,BaysideTablet-Ward-4
Bayside Memorial,Ward,Ward-5,Tablet,BaysideTablet-Ward-5
Bayside Memorial,Ward,Ward-6,Tablet,BaysideTablet-Ward-6
Bayside Memorial,Ward,Ward-7,Tablet,BaysideTablet-Ward-7
Bayside Memorial,Ward,Ward-8,Tablet,BaysideTablet-Ward-8
,,,,
Tiburon Medical,,Server Room,Domain Controller,TiburonDC
Tiburon Medical,Cardio/Thoracic,Office,Client PC,TiburonPC-Office-CT
Tiburon Medical,Cardio/Thoracic,Office,Client PC,TiburonPC-Office-CT
Tiburon Medical,Cardio/Thoracic,Exam 1,Tablet,TiburonTablet-Exam 1-CT
Tiburon Medical,Cardio/Thoracic,Exam 2,Tablet,TiburonTablet-Exam 2-CT
Tiburon Medical,Dermatology,Office,Client PC,TiburonPC-Office-D
Tiburon Medical,Dermatology,Office,Client PC,TiburonPC-Office-D
Tiburon Medical,Dermatology,Exam 1,Tablet,TiburonTablet-Exam 1-D
Tiburon Medical,Dermatology,Exam 2,Tablet,TiburonTablet-Exam 2-D
Tiburon Medical,Dermatology,Exam 3,Tablet,TiburonTablet-Exam 3-D
Tiburon Medical,Neurology,Office,Client PC,TiburonPC-Office-N
Tiburon Medical,Neurology,Office,Client PC,TiburonPC-Office-N
Tiburon Medical,Neurology,Exam 1,Tablet,TiburonTablet-Exam 1-N
Tiburon Medical,Neurology,Exam 2,Tablet,TiburonTablet-Exam 2-N
Tiburon Medical,Neurology,Exam 3,Tablet,TiburonTablet-Exam 3-N
Tiburon Medical,Oncology,Office,Client PC,TiburonPC-Office-O
Tiburon Medical,Oncology,Office,Client PC,TiburonPC-Office-O
Tiburon Medical,Oncology,Exam 1,Tablet,TiburonTablet-Exam 1-O
Tiburon Medical,Oncology,Exam 2,Tablet,TiburonTablet-Exam 2-O
Tiburon Medical,Oncology,Exam 3,Tablet,TiburonTablet-Exam 3-O
Tiburon Medical,Pediatrics,Office,Client PC,TiburonPC-Office-P
Tiburon Medical,Pediatrics,Office,Client PC,TiburonPC-Office-P
Tiburon Medical,Pediatrics,Exam 1,Tablet,TiburonTablet-Exam 1-P
Tiburon Medical,Pediatrics,Exam 2,Tablet,TiburonTablet-Exam 2-P
Tiburon Medical,Pediatrics,Exam 3,Tablet,TiburonTablet-Exam 3-P
Tiburon Medical,Pediatrics,Exam 4,Tablet,TiburonTablet-Exam 4-P
Tiburon Medical,Pediatrics,Exam 5,Tablet,TiburonTablet-Exam 5-P
Tiburon Medical,Urology,Office,Client PC,TiburonPC-Office-U
Tiburon Medical,Urology,Office,Client PC,TiburonPC-Office-U
Tiburon Medical,Urology,Exam 1,Tablet,TiburonTablet-Exam 1-U
Tiburon Medical,Urology,Exam 2,Tablet,TiburonTablet-Exam 2-U
Tiburon Medical,Urology,Exam 3,Tablet,TiburonTablet-Exam 3-U
,,,,
Larkspur Ambulatory,,Server Room,Domain Controller,LarkspurDC
Larkspur Ambulatory,Administration,Office,Client PC,LarkspurPC-Office-Admin
Larkspur Ambulatory,Administration,Office,Client PC,LarkspurPC-Office-Admin
Larkspur Ambulatory,Administration,Office,Client PC,LarkspurPC-Office-Admin
Larkspur Ambulatory,Administration,Office,Client PC,LarkspurPC-Office-Admin
Larkspur Ambulatory,Administration,Office,Client PC,LarkspurPC-Office-Admin
Larkspur Ambulatory,Prep,1,Tablet,LarkspurTablet-1-Prep
Larkspur Ambulatory,Prep,2,Tablet,LarkspurTablet-2-Prep
Larkspur Ambulatory,Prep,3,Tablet,LarkspurTablet-3-Prep
Larkspur Ambulatory,Prep,4,Tablet,LarkspurTablet-4-Prep
Larkspur Ambulatory,Prep,5,Tablet,LarkspurTablet-5-Prep
Larkspur Ambulatory,Prep,6,Tablet,LarkspurTablet-6-Prep
Larkspur Ambulatory,Prep,7,Tablet,LarkspurTablet-7-Prep
Larkspur Ambulatory,Prep,8,Tablet,LarkspurTablet-8-Prep
Larkspur Ambulatory,Prep,9,Tablet,LarkspurTablet-9-Prep
Larkspur Ambulatory,Surgery,OR-1,Tablet,LarkspurTablet-OR-1-Surgery
Larkspur Ambulatory,Surgery,OR-1,Tablet,LarkspurTablet-OR-1-Surgery
Larkspur Ambulatory,Surgery,OR-2,Tablet,LarkspurTablet-OR-2-Surgery
Larkspur Ambulatory,Surgery,OR-2,Tablet,LarkspurTablet-OR-2-Surgery
Larkspur Ambulatory,Surgery,OR-3,Tablet,LarkspurTablet-OR-3-Surgery
Larkspur Ambulatory,Surgery,OR-3,Tablet,LarkspurTablet-OR-3-Surgery
Larkspur Ambulatory,Surgery,OR-4,Tablet,LarkspurTablet-OR-4-Surgery
Larkspur Ambulatory,Surgery,OR-4,Tablet,LarkspurTablet-OR-4-Surgery
Larkspur Ambulatory,Surgery,OR-5,Tablet,LarkspurTablet-OR-5-Surgery
Larkspur Ambulatory,Surgery,OR-5,Tablet,LarkspurTablet-OR-5-Surgery
Larkspur Ambulatory,Surgery,OR-5,Tablet,LarkspurTablet-OR-5-Surgery
Larkspur Ambulatory,Surgery,OR-6,Tablet,LarkspurTablet-OR-6-Surgery
Larkspur Ambulatory,Surgery,OR-6,Tablet,LarkspurTablet-OR-6-Surgery
Larkspur Ambulatory,Surgery,OR-6,Tablet,LarkspurTablet-OR-6-Surgery
Larkspur Ambulatory,Surgery,OR-7,Tablet,LarkspurTablet-OR-7-Surgery
Larkspur Ambulatory,Surgery,OR-7,Tablet,LarkspurTablet-OR-7-Surgery
Larkspur Ambulatory,Surgery,OR-7,Tablet,LarkspurTablet-OR-7-Surgery
, ,,,
```
