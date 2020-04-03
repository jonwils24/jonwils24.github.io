---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
category: Customization
option: virtualization server AVM
---

# Configuring the virtualization server

WCM preview allows editorial users to preview the website in-context \(with the style, markup, and composition of the website\), but using the content from any sandbox in the system. Preview provides a way for contributors and reviewers to view changes as if they had been published to the live site, without publishing those changes.

This is primarily used for two activities:

-   To allow content approvers to review a change they have been asked to approve in the context of the website.
-   To allow content contributors to view their changes in the context of the website, while they are in the process of making those changes.

The virtualization server is the default WCM preview functionality when WCM is installed. The virtualization server \(which is a slightly modified Tomcat server\) interprets data in the AVM repository as a set of virtual websites, allowing users to browse these websites prior to deployment. These websites may include both static sites \(or example, .html, .gif, .png\) and simple Java-based sites \(virtualized servlets and JSPs\).

Each Web Project is assumed to be a self contained J2EE web application, and each sandbox in the Web Project is automatically "deployed" as a J2EE web application to the virtualization server. The virtualization server lazily "deploys" each sandbox the first time it receives a preview request, and no physical deployment occurs. The virtualization server has been customized to read the web application directly from the Alfresco repository, rather than from the file system.

To ensure the transparent preview of any sandbox in any Web Project in the system, Alfresco uses dynamic host names \(in tandem with wildcard DNS\) for accessing the virtualization server. From this enhanced host name, the virtualization server is able to determine from which sandbox and Web Project to read content and web application assets. This ensures that the web application itself has no knowledge of any WCM constructs \(sandboxes, Web Projects, virtualization server, and so on\); it runs as if it is in a native Tomcat server and the virtualization system ensures that assets are read from the correct sandbox for each preview request.

Each virtual view corresponds to a virtual website within its own virtual host. You can see the virtual view in the URL itself. The following URL shows the general format of an Alfresco virtual hyperlink:

http://virtual-hostname.www--sandbox.virtualization-domain:port/request-path

To configure virtual websites, the `virtualization-domain` and all its subdomains must resolve in DNS to the IP address of the virtualization server \(also known as a “wildcard DNS” mapping\). There are two ways to achieve this:

-   Use the appropriate subdomain of ip.alfrescodemo.net
-   Configure a nameserver, and setting up a wildcard domain pointing at your virtualization server's IP address

-   **[Using ip.alfrescodemo.net](../tasks/vs-ip-config.md)**  
To set up virtualization for a single machine or a LAN, use the appropriate subdomain of ip.alfrescodemo.net.
-   **[Configuring wildcard DNS on a nameserver](../tasks/vs-dns-config.md)**  
This section describes how to configure a nameserver and set up a wildcard domain pointing at your virtualization server machine's IP address to do the following:

**Parent topic:**[Configuring AVM](../concepts/wcm-config-intro.md)

