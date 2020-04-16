---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: Administration
option: authentication subsystem chain
---

# Configuring the authentication chain

This section describes how you can add to or completely replace the default authentication chain.

The chain is controlled by the `authentication.chain` global property.

1.  Open the alfresco-global.properties file.

2.  Locate the `authentication.chain` global property.

    This is a comma separated list of the form:

    ```
    instance_name1:type1,...,instance_namen:typen
    ```

3.  Set the property to the required values.

    For example, set the property to the following value:

    ```
    alfrescoNtlm1:alfrescoNtlm,ldap1:ldap
    ```

    When you navigate to the `Alfresco:Type=Configuration,Category=Authentication,id1=manager` MBean in global property overrides, then a new authentication subsystem instance called `ldap1` will be brought into existence and added to the end of the authentication chain.

4.  Save the file.


The following example integrates Alfresco with Active Directory has the requirements:

-   Built-in Alfresco users and Windows users should be able to log in, with Alfresco taking precedence
-   The Windows domain server should handle CIFS authentication directly
-   LDAP should be used to synchronize user and group details

To achieve these requirements, configure the following authentication chain:

```
alfrescoNtlm1:alfrescoNtlm,passthru1:passthru,ldap1:ldap
```

Next, deactivate SSO in order to activate chained password-based login, target CIFS at `passthru1` and target synchronization \(but not authentication\) at `ldap1` by setting the properties as follows:

-   **alfrescoNtlm1**

    `ntlm.authentication.sso.enabled=false`

    `alfresco.authentication.authenticateCIFS=false`

-   **passthru1**

    `ntlm.authentication.sso.enabled=false`

    `passthru.authentication.authenticateCIFS=true`

-   **ldap1**

    `ldap.authentication.active=false`

    `ldap.synchronization.active=true`


**Parent topic:**[Configuring authentication](../concepts/auth-config-examples.md)

