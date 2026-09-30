\# Oracle 19c Database Validation Evidence



\## Validation Objective



Confirm that the Oracle 19c database and multitenant environment were successfully created and operational following DBCA deployment.



\## Database Status



Validation query:



```sql

SELECT name,

&#x20;      open\_mode,

&#x20;      database\_role,

&#x20;      log\_mode

FROM v$database;



| Database | Open Mode | Role | Log Mode |

|---|---|---|---|

| PROD | READ WRITE | PRIMARY | NOARCHIVELOG |



Instance Status

Validation query:

SELECT instance\_name,

&#x20;      status,

&#x20;      version

FROM v$instance;



Observed result:

Instance	Status	Version

prod	OPEN	19.0.0.0.0





PDB Status

Validation:

SHOW PDBS;



Observed state:

CON\_ID	PDB	Open Mode

2	PDB$SEED	READ ONLY

3	PRODPDB	READ WRITE







