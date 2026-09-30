\# Troubleshooting — TNS-12541: No Listener



\## Scenario



During post-installation validation, Oracle Net Listener status was checked using:



`lsnrctl status`



The connection attempt failed with:



`TNS-12541: TNS:no listener`



and:



`Linux Error: 111: Connection refused`



\## Initial Assessment



The error indicated that no Oracle listener was accepting connections on the configured listener endpoint.



The configured endpoint was:



\- Host: oradb19-prd

\- Protocol: TCP

\- Port: 1521



\## Action



The listener was started using:



`lsnrctl start`



The listener successfully started using:



`$ORACLE\_HOME/network/admin/listener.ora`



and began listening on TCP port 1521.



\## Service Registration



Immediately after startup, the listener initially reported:



`The listener supports no services`



A subsequent listener status check showed successful dynamic registration of the database services.



Registered services included:



\- prod

\- prodXDB

\- prodpdb



The PROD instance reported READY status.



\## Validation



Validation command:



`lsnrctl status`



confirmed that the listener was operational and database services were registered.



\## Root Cause



The Oracle listener process was not running during the initial validation.



\## Resolution



The listener was started and database service registration was subsequently verified.



\## Production Considerations



In a production incident, I would not assume that every TNS-12541 error means the listener simply needs to be started.



Additional checks could include:



\- Listener process status

\- Configured listener hostname and port

\- listener.ora configuration

\- Database service registration

\- LOCAL\_LISTENER configuration

\- DNS/hostname resolution

\- Network connectivity

\- Firewall rules

\- Listener and database alert logs

\- OS port availability



\## Lesson Learned



TNS-12541 identifies a listener connectivity failure at the requested endpoint. Troubleshooting should establish whether the listener is stopped or whether the client is attempting to reach the wrong or inaccessible endpoint before corrective action is taken.

