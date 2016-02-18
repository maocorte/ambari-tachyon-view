#### Ambari Tachyon View
Embed Tachyon UI into Ambari.
Tachyon is a memory-centric distributed storage system enabling reliable data sharing at memory-speed across cluster frameworks.
This is a simple example.

Author: [Mauro Cortellazzi](https://github.com/maocorte)

-----------------


##### Setup

To deploy the Tachyon view, run below.
On non-sandbox env, these steps should be run on node running Ambari server

```
#Pull code (pom.xml, view.xml, index.html)
cd
git clone https://github.com/maocorte/ambari-tachyon-view.git
cd ambari-tachyon-view

#Compile view
mvn clean package

#move jar to Ambari dir
cp target/*.jar /var/lib/ambari-server/resources/views

```
- Restart Ambari

```
#on sandbox
service ambari restart

#on non-sandbox
service ambari-server restart
```

- Now open Ambari and navigate to the Views as shown below and select 'Tachyon UI'
