\# Oracle 19c Lab Architecture



\## Logical Architecture



Windows Workstation

|

|-- Git / GitHub Portfolio

|

`-- Oracle VirtualBox

&#x20;   |

&#x20;   `-- oradb19-prd

&#x20;       |

&#x20;       |-- Oracle Linux 8

&#x20;       |

&#x20;       |-- Oracle Database 19c Enterprise Edition

&#x20;       |

&#x20;       `-- PROD

&#x20;           |

&#x20;           |-- CDB$ROOT

&#x20;           |-- PDB$SEED

&#x20;           `-- PRODPDB



\## Oracle Database Architecture



\### Container Database



`PROD`



\### Pluggable Databases



| PDB | Initial State |

|---|---|

| PDB$SEED | READ ONLY |

| PRODPDB | READ WRITE |



\## Oracle Home



`/u01/app/oracle/product/19.3.0/dbhome\_1`



\## Oracle Base



`/u01/app/oracle`



\## Listener



Protocol: TCP  

Port: 1521  

Host: oradb19-prd



\## Purpose



This server is the primary Oracle 19c environment used throughout the enterprise Oracle lab.



Future projects will extend the architecture to include backup/recovery infrastructure, cloned databases, migration targets, Data Guard standby databases, GoldenGate replication, RAC, security assessment, and newer Oracle database releases.

