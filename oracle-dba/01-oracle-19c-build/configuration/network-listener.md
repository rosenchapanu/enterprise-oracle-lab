\# Oracle Net Listener Configuration



\## Listener



Listener Name: LISTENER



Protocol: TCP



Host:



`oradb19-prd`



Port:



`1521`



Listener configuration:



`$ORACLE\_HOME/network/admin/listener.ora`



\## Registered Database Services



Post-installation validation confirmed registration of services including:



\- prod

\- prodXDB

\- prodpdb



The PROD database instance reported READY status.



\## Service Registration



After the listener was started, it initially reported no registered services.



Shortly afterward, Oracle dynamic service registration registered the database services with the listener.



This behavior was observed and validated using:



`lsnrctl status`

