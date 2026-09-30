\# Initial Oracle Security Baseline



\## Purpose



This document records selected security-related conditions immediately following creation of the Oracle 19c database.



This is a baseline only.



Security hardening will be performed later as a dedicated project so that findings, remediation, and before/after evidence can be demonstrated.



\## Account Baseline



The initial account review was performed using:



```sql

SELECT username,

&#x20;      account\_status,

&#x20;      authentication\_type

FROM dba\_users

ORDER BY username;



The initial database contained 36 accounts.

Most Oracle-maintained accounts were observed in LOCKED or EXPIRED \& LOCKED states.

SYS and SYSTEM were OPEN.

Future Assessment Areas

The dedicated security projects will assess areas including:

\- Oracle users and account status

\- Privileged accounts

\- Roles and system privileges

\- Least privilege

\- Password profiles

\- PUBLIC privileges

\- Unified Auditing

\- Failed authentication attempts

\- Oracle Net security

\- Operating-system permissions

\- Database patch status

\- Encryption controls

\- TDE where applicable

\- DISA STIG requirements

\- Security findings and remediation

RMF Integration

Later phases will map selected technical and administrative controls to applicable NIST SP 800-53 controls and produce assessment artifacts such as:

\- Findings

\- Risk statements

\- Evidence

\- Remediation plans

\- POA\&M entries

\- Risk register entries

\- Continuous monitoring evidence

Baseline Status

No security changes were made as part of this evidence collection.

The purpose is to preserve the original post-installation state for later comparison.

