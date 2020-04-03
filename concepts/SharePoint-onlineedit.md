---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: [Installation, Administration, SharePoint Protocol, Extensions/Third Party Tools]
keyword: [SharePoint Protocol, Extensions/Third Party Tools]
---

# Configuring SharePoint Protocol for Online Editing

The following issues are known for configuring the SharePoint Protocol for Online Editing

-   There is a known issue with Office 2003 and 2007 Office documents opening as read-only in Internet Explorer for all versions before Vista SP1.

    Refer to the knowledge base article 870853 on the Microsoft website to enable the Online Editing functionality.

-   To use Online Editing on Windows 7, you must set `BasicAuthLevel` in the registry.

    Basic authentication is disabled on Office 2010 by default. To enable it, create or edit the following registry key: `HKCU\Software\Microsoft\Office\14.0\Common\Internet: BasicAuthLevel=2`.

    Alternatively, use Pass-through or Kerberos authentication.

    **Note:** It is important to set the `vti.server.external.host` and vti.server.external.port properties in the alfresco-global.properties file to the externally resolvable host and port name that SharePoint clients will communicate with. These properties default to the host machine's local name and port 7070, respectively. These values are used by Share to generate the **Edit Online** link, which opens the document using the SharePoint module.


**Parent topic:**[Installing and configuring Microsoft Office SharePoint Protocol Support](../concepts/SharePoint-intro.md)

