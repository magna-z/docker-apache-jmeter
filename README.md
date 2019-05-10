Apache JMeter in Docker
===

Java application designed to load test functional behavior and measure performance.

[![](https://images.microbadger.com/badges/image/devinotelecom/apache-jmeter.svg)](http://microbadger.com/images/devinotelecom/apache-jmeter)

Official website: <https://jmeter.apache.org>  
Latest release: **5.1.1**

### Available tags:
- **5.1.1** or **latest** ([Dockerfile](https://github.com/devinotelecom/docker-apache-jmeter/blob/5.1.1/Dockerfile)) [![](https://images.microbadger.com/badges/image/devinotelecom/apache-jmeter:5.1.1.svg)](https://microbadger.com/images/devinotelecom/apache-jmeter:5.1.1)

### Run as JMeter-server:
```bash
docker run -d -p 1099:1099 \
devinotelecom/apache-jmeter:latest \
-s \
-Dserver_port=1099 \
-Jserver.rmi.ssl.disable=true
```
Where:
- `-s`: run the JMeter server
- `-Dserver_port=1099`: RMI port used by the server
- `-Jserver.rmi.ssl.disable=true`: don't use SSL for RMI

Default logging on level INFO into console/STDOUT. See `/opt/apache-jmeter/bin/log4j2.xml`.
