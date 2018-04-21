# Ubuntu 16.04 and above

You can simply install `openjdk-8-jre` or `openjdk-8-jre` from the official repositories.


# Ubuntu 14.04

The Java RE from your repos is version 7, whereas gngr requires Java RE 8. You will need to download one of the JRE binary blobs, either from Oracle or Zulu.

# Installing and using the Oracle JRE

1. Visit http://www.oracle.com/technetwork/java/javase/downloads/index.html
2. Click on JRE
3. Download the .tar.gz package relevant for your architecture
4. `tar zxf jre-8u74-linux-x64.tar.gz`
5. `jre1.8.0_74/bin/java -jar gngr-0.3.10.jar`

This will not install the binary blobs from Oracle system-wide or run any code from Oracle as root user.

# Installing the JRE from Zulu

1. Visit https://zulu.org/download/
2. Download the latest package
3. Extract and run as described above for Oracle JRE