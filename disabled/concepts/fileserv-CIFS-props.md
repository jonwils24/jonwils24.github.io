---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: Administration
option: file servers subsystem SMB CIFS
---

# CIFS file server properties

The following properties can be configured for the SMB/CIFS server.

-   **cifs.enabled**

    Enables or disables the CIFS server.

-   **cifs.serverName**

    Specifies the host name for the Alfresco CIFS server. This can be a maximum of 16 characters and must be unique on the network. The special token `{localname}` can be used in place of the local server's host name and a unique name can be generated by prepending/appending to it.

-   **cifs.domain**

    An optional property. When not empty, specifies the domain or workgroup to which the server belongs. This defaults to the domain/workgroup of the server, if not specified.

-   **cifs.hostannounce**

    Enables announcement of the CIFS server to the local domain/workgroup so that it shows up in Network Places/Network Neighborhood.

-   **cifs.sessionTimeout**

    Specifies the CIFS session timeout value in seconds. The default session timeout is 15 minutes. If no I/O occurs on the session within this time then the session will be closed by the server. Windows clients send keep-alive requests, usually within 15 minutes.


**Parent topic:**[Configuring SMB/CIFS server](../concepts/fileserv-subsystem-CIFS.md)

