---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
category: Customization
option: DNS nameserver virtualization server
---

# Configuring wildcard DNS on a nameserver

This section describes how to configure a nameserver and set up a wildcard domain pointing at your virtualization server machine's IP address to do the following:

-   Virtualize content on a machine or LAN with no access to the Internet \(for example: a demo laptop\)
-   Attain faster speeds on the first DNS lookup of a name than when served locally \(IP address answers have a one day TTL\)
-   Keep everything centralized if you already have BIND, djbdns, Microsoft DNS, or other DNS solution in place
-   Be independent from the Alfresco alfrescodemo.net uptime

1.  Set the directory where you installed the virtualization server, for example: $VIRTUAL\_TOMCAT\_HOME.

    In this example, the LAN's domain name is localdomain.lan, a wildcard DNS record resolves to an IP address such as 192.168.1.5, and the wildcard DNS names are within ip.localdomain.lan.

2.  Open the file $VIRTUAL\_TOMCAT\_HOME/conf/alfresco-virtserver.properties.

3.  Modify the value of the `alfresco.virtserver.domain` property to resemble the following:

    `alfresco.virtserver.domain=ip.localdomain.lan`

    **Note:** You cannot use the “hosts” file to create a wildcard DNS domain on Windows or Unix. To create a DNS wildcard that is usable when you are not connected to the Internet, you must install, configure, and maintain a real nameserver.


**Parent topic:**[Configuring the virtualization server](../concepts/vs-intro-config.md)

