\# Oracle Environment Configuration



\## Oracle Environment



| Variable | Value |

|---|---|

| ORACLE\_SID | prod |

| ORACLE\_BASE | /u01/app/oracle |

| ORACLE\_HOME | /u01/app/oracle/product/19.3.0/dbhome\_1 |



\## Database



| Attribute | Value |

|---|---|

| Database Name | PROD |

| Instance | prod |

| Database Role | PRIMARY |

| Open Mode | READ WRITE |

| Log Mode | NOARCHIVELOG |



\## Multitenant Configuration



PROD contains:



\- CDB$ROOT

\- PDB$SEED

\- PRODPDB



At initial validation:



\- PDB$SEED was READ ONLY

\- PRODPDB was READ WRITE



\## Recovery Configuration



At completion of the initial build:



\- ARCHIVELOG mode was not yet enabled.

\- Fast Recovery Area was not yet configured.



These items are intentionally deferred to the RMAN/recovery project.

