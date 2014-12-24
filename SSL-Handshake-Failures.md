### SSL Handshake Failures

There are currently two issues when navigating to HTTPS web-sites.

* [SSL Handshake fails for servers that use only strong ciphers](https://github.com/UprootLabs/gngr/issues/11)
* [SSL Handshake fails for almost all https URLs on MacOSX](https://github.com/UprootLabs/gngr/issues/8)

The first issue is caused by a crippled policy in Oracle JVM builds, and in Zulu builds. To comply with import laws of different countries, the key length of the ciphers available in the JVM is restricted to 128-bit. The user needs to install the [JCE Unlimited Jurisdiction Policy](http://www.oracle.com/technetwork/java/javase/downloads/index.html) manually.

OpenJDK builds in Debian / Ubuntu don't suffer from this limitation.

This is inconvenient to say the least. We are working on this in two ways:

  1. Trying to rewrite our code to be Java 7 compliant. Since OpenJDK-7 builds are more readily available, this will mitigate the problem a bit.
  2. Contacting vendors of JREs to reduce the pain at the source. For example, they could bundle the unlimited JCE jars along with appropriate notices.

We are currently not sure about the root cause for the second issue, but it is perhaps related to the first one.