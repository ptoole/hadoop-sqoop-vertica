
Vertica Connector for Hadoop Sqoop
----------------------------------
version 1.0a
see COPYRIGHT.txt for copyright information


This project is a basic implementation of sqoop integration into the Vertica JDBC driver. Similar
to the way the MySQL sqoop integration works, this is broken into 2 parts. Remote should be used 
unless there is a vsql client installed locally.

Remote Mode
- On import, generic result sets are leveraged.
- On export, Vertica's Driver is leveraged and uses the streaming COPY command and gzip to reduce network traffic.


Local Mode
- On import, generic result sets are leveraged.
- On export, Vertica uses named pipes to import the data, gzip is optional.

