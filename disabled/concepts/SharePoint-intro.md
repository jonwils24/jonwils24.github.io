---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: [Installation, Administration, SharePoint Protocol, Extensions/Third Party Tools]
keyword: [SharePoint Protocol, Extensions/Third Party Tools]
---

# Installing and configuring Microsoft Office SharePoint Protocol Support

The Microsoft Office SharePoint Protocol Support offers Microsoft users greater choice by providing a fully-compatible SharePoint repository that allows the Microsoft Office Suite applications \(for example, Word, PowerPoint, Excel\) to interact with Alfresco as if it was SharePoint. This enables your users to leverage the Alfresco repository directly from Microsoft Office.

You can also use Microsoft Office SharePoint Protocol Support to enable online editing for Office documents within Alfresco Share. It enables your users to modify Office files without checking them in and out. Alfresco locks the file while it is being modified and releases the lock when the file is saved and closed.

The following diagram shows the architecture of the SharePoint Protocol Support in relation to an Alfresco installation.

![](../images/SPP-arch.jpg)

The SharePoint Protocol Support architecture embeds a Jetty web server within the Alfresco repository. The Microsoft Office clients communicate directly with the Jetty server using WebDAV-like calls with proprietary extensions and on different port number from Alfresco Share. This port number can be configured in the SharePoint Protocol Support properties files.

-   **[Installing the SharePoint Protocol Support AMP](../tasks/SharePoint-install.md)**  
The SharePoint Protocol support functionality is installed from an Alfresco AMP. If you use the Windows or Linux installers to install Alfresco, the SharePoint Protocol Support is installed by default. These instructions describe how to install the SharePoint Protocol Support into the Alfresco WAR.
-   **[Prerequisites for using SharePoint Protocol](../concepts/SharePoint-reqs.md)**  
The SharePoint Protocol module lets you manage Alfresco content from within Microsoft office. To use SharePoint with Alfresco, you need to install an important update from Microsoft.
-   **[Configuring SharePoint Protocol Support](../tasks/SharePoint-config.md)**  
This section describes how to configure the SharePoint Protocol Support properties to complete the set up process.
-   **[Configuring SharePoint Protocol for Online Editing](../concepts/SharePoint-onlineedit.md)**  
The following issues are known for configuring the SharePoint Protocol for Online Editing
-   **[Setting up SharePoint Protocol Support to work with Office 2010](../tasks/SharePoint-config-office2010.md)**  
This section describes how to configure the SharePoint Protocol Support to work with Office 2010 on Windows 7.
-   **[Setting up sticky sessions with SharePoint Protocol Support](../tasks/cluster-SPP-stickysession.md)**  
This section describes how to configure sticky sessions in a high availability environment with the SharePoint Protocol Support embedded Jetty server.
-   **[Setting up SharePoint Protocol Support to work with HTTPS](../tasks/SharePoint-HTTPS-setup.md)**  
This section describes how to configure the Jetty server so that the SharePoint Protocol Support will run over HTTPS.

**Parent topic:**[Installing](../concepts/master-ch-install.md)

