---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: Administration
option: authentication subsystem synchronization
---

# Synchronization configuration properties

The synchronization subsystem manages synchronization of Alfresco by configuring the subsystem's properties.

The following properties can be configured for the synchronization subsystem.

-   **synchronization.synchronizeChangesOnly**

    Specifies if the scheduled synchronization job is run in differential mode. The default value is false, which means that the scheduled sync job is run in full mode. Regardless of this setting a differential sync may still be triggered when a user is successfully authenticated who does not yet exist in Alfresco.

-   **synchronization.allowDeletions**

    Specifies if deletion of local users and groups is allowed. See the sections on [Synchronization deletion](sync-delete.md) and [Collision resolution](sync-collision.md) for the circumstances under which this may happen. The default is true. If false, then no sync job will be allowed to delete users or groups during the handling of removals or collision resolution.

-   **synchronization.import.cron**

    Specifies a cron expression defining when the scheduled synchronization job should run, by default at midnight every day.

-   **synchronization.syncOnStartup**

    Specifies whether to trigger a differential sync when the subsystem starts up. The default value is true. This ensures that when user registries are first configured, the bulk of the synchronization work is done on server startup, rather than on the first login.

-   **synchronization.syncWhenMissingPeopleLogIn**

    Specifies whether to trigger a differential sync when a user is successfully authenticated who does not yet exist in Alfresco. The default value is true.

-   **synchronization.autoCreatePeopleOnLogin**

    Specifies whether to create a user with default properties when a user is successfully authenticated, who does not yet exist in Alfresco, and was not returned by a differential sync \(if enabled with the property above\). The default value is true. Setting the value to false allows you to restrict Alfresco to a subset of those users who could be authenticated by LDAP; only those created by synchronization are allowed to log in. You can control the set of users in this more restricted set by overriding the user query properties of the LDAP authentication subsystem.


**Parent topic:**[Configuring synchronization](../concepts/sync-intro.md)

