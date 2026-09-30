\# Project 01 — Oracle Database 19c Enterprise Lab Build



\## Project Overview



This project documents the deployment of an Oracle Database 19c Enterprise Edition environment on Oracle Linux 8.



The environment serves as the foundation for a larger hands-on Oracle DBA engineering lab covering multitenant administration, daily database operations, RMAN backup and recovery, disaster recovery scenarios, cloning, migration, performance tuning, patching, automation, security hardening, DISA STIG assessment, RMF/NIST control mapping, Data Guard, GoldenGate, RAC, and future Oracle database upgrades.



\## Objectives



\- Build an Oracle Linux 8 database server

\- Configure the operating system for Oracle Database

\- Install Oracle Database 19c Enterprise Edition

\- Configure Oracle environment variables

\- Configure Oracle Net Listener

\- Create a multitenant Oracle database using DBCA

\- Validate CDB and PDB availability

\- Establish an initial database/security baseline

\- Document troubleshooting and validation evidence



\## Environment



| Component | Configuration |

|---|---|

| Hostname | oradb19-prd |

| Operating System | Oracle Linux 8 |

| Database | Oracle Database 19c Enterprise Edition |

| Oracle Base | /u01/app/oracle |

| Oracle Home | /u01/app/oracle/product/19.3.0/dbhome\_1 |

| Oracle SID | prod |

| CDB | PROD |

| PDB | PRODPDB |

| Listener | TCP/1521 |

| Database Role | PRIMARY |

| Current Log Mode | NOARCHIVELOG |



\## Database Architecture



The initial multitenant environment consists of:



PROD (CDB)

\- PDB$SEED — READ ONLY

\- PRODPDB — READ WRITE



\## Validation Results



The installation was validated using SQL\*Plus and Oracle Net utilities.



Validated:



\- Oracle instance is OPEN

\- PROD database is READ WRITE

\- Database role is PRIMARY

\- PRODPDB is READ WRITE

\- Oracle listener is operational on TCP port 1521

\- PROD and PRODPDB services dynamically register with the listener

\- Two control files are configured

\- Initial Oracle account status was captured as a security baseline



\## Current Recovery Configuration



The database was intentionally left in NOARCHIVELOG mode at the completion of the installation phase.



The Fast Recovery Area (FRA) has also not yet been configured.



These settings will be addressed during the RMAN backup and recovery phases so the configuration changes and recovery implications can be tested and documented.



\## Troubleshooting Performed



During post-installation validation, `lsnrctl status` returned:



`TNS-12541: TNS:no listener`



The listener was started and validated on TCP port 1521. Database services subsequently registered dynamically with the listener.



The troubleshooting scenario is documented separately under the `troubleshooting` directory.



\## Security



The initial Oracle user/account configuration was captured before security hardening.



This baseline will later be used for:



\- Oracle Database Security Hardening

\- DISA STIG Assessment

\- STIG remediation and retesting

\- NIST SP 800-53 control mapping

\- RMF assessment

\- POA\&M development

\- Continuous monitoring exercises



No passwords, credentials, private keys, wallets, or other secrets are stored in this repository.



\## Project Status



\*\*Completed — Initial Oracle 19c deployment and validation\*\*



\## Next Phase



\*\*Project 02 — CDB/PDB Administration\*\*

