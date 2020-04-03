---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
category: Customization
option: ip.alfrescodemo.net virtualization server
---

# Using ip.alfrescodemo.net

To set up virtualization for a single machine or a LAN, use the appropriate subdomain of ip.alfrescodemo.net.

In this example, `192.168.1.5` is the IP address of the machine hosting the virtualization server. Alfresco has set up a nameserver at ip.alfrescodemo.net that is able to resolve any domain name of the form `AAA-BBB-CCC-DDD.ip.alfrescodemo.net` \(or any of its subdomains\) as the IP address `AAA.BBB.CCC.DDD`.

For example, if your browser asks for the virtual host name: `alice.mysite.www--sandbox.192-168-1-5.ip.alfrescodemo.net`, the IP address returned will be: `192.168.1.5`. Therefore, ip.alfrescodemo.net provides "wildcard dns" for all valid IPV4 address. By default, the virtualization server is configured to use the virtualization domain `127-0-0-1.ip.alfrescodemo.net`. This returns the IP address `127.0.0.1`. This special IP address always refers to your local machine \(hence its name: `localhost`\). Therefore, if you use the default virtualization domain `127-0-0-1.ip.alfrescodemo.net`, you will only be able to do in-context preview on the same machine that hosts the virtualization server. To enable everybody on a LAN to use in-context preview, you need to use a network-accessible IP address.

1.  Open the $VIRTUAL\_TOMCAT\_HOME/conf/alfresco-virtserver.properties file.

    Where $VIRTUAL\_TOMCAT\_HOME represents the directory in which you installed the virtualization server.

2.  Locate the property `alfresco.virtserver.domain=127-0-0-1.ip.alfrescodemo.net.`

3.  Edit the property to contain the hyphen-encoded IP address you want.

    For example: alfresco.virtserver.domain=192-168-1-5.ip.alfrescodemo.net.

    **Important:** When specifying alfresco.virtserver.domain that uses ip.alfrescodemo.net, the IP address for a DNS wildcard domain must be hyphen-encoded. Otherwise, ip.alfrescodemo.net will assume an error, and return 127.0.0.1 for all DNS name lookups within your malformed virtualization domain.

    For example:

    Valid: alfresco.virtserver.domain=192-168-1-5.ip.alfrescodemo.net

    Malformed: alfresco.virtserver.domain=192.168.1.5.ip.alfrescodemo.net

    Alfresco can now generate URLs that address the virtualization server's network-accessible address, such as 192.168.1.5 and not 127.0.0.1, allowing users on a LAN to use in-context preview.

4.  Restart the Tomcat instance that runs Alfresco.

5.  Near WCM assets, click the icon resembling an eyeball.

    A list of URLs displays, for example: http://<hostname\>.www--sandbox.192-168-1-5.ip.alfrescodemo.net

    These links will resolve to your virtualization server, which is on 192.168.1.5.

6.  To view this in isolation, run one of the following commands:

    -   `ping alice.mysite.www--sandbox.192-168-1-5.ip.alfrescodemo.net`
    -   `ping mysite.www--sandbox.19`

**Parent topic:**[Configuring the virtualization server](../concepts/vs-intro-config.md)

