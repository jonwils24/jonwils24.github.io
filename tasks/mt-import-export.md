---
author: [Alfresco Documentation, Alfresco Documentation]
source: wiki
audience: 
category: Administration
option: Multi-tenancy export import
---

# Multi-tenancy export and import

This section describes how a tenant administrator can export and import spaces and tenants using the Tenant Administration Console.

**Note:** Repository export does not apply to certain areas, such as in-flight workflows. A repository import must be into the same version of Alfresco from which the export was performed.

1.  Log in to Alfresco as the admin user and access: `http://localhost:8080/alfresco/faces/jsp/admin/tenantadmin-console.jsp`

2.  Use the export feature to export a tenant:

    `export <tenant domain> <destination directory>`

    This exports the tenant to a set of repository export files in a given destination directory. Export file names will be suffixed with <tenant domain\>\_.

3.  Use the import feature to import a tenant:

    `import <tenant domain> <source directory> [<root contentstore dir>]`

    This creates a tenant by importing the tenant files from the given source directory. The import file names must be suffixed with <tenant domain\>\_.

    **Note:** If an existing tenant needs to be re-imported, the tenant must be deleted first. To cleanly delete a tenant, the server must be restarted to clear the index threads. The tenant-specific index directories and tenant-specific content directories must also be manually deleted before starting the import.


**Parent topic:**[Multi-tenancy administration](../concepts/mt-webclient-admin.md)

