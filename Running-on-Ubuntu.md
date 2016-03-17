# Ubuntu 14.04

Java RE from your repos doesn't work correctly with gngr. You're going to need to download JRE binary blob from Oracle.

Steps:

1. Go to http://www.oracle.com/technetwork/java/javase/downloads/index.html
2. Click on JRE
3. Download the .tar.gz package relevant for your architecture
4. `tar zxf jre-8u74-linux-x64.tar.gz`
5. `jre1.8.0_74/bin/java -jar gngr-0.3.10.jar`

This will not install the binary blobs from Oracle system-wide or run any code from Oracle as root user.