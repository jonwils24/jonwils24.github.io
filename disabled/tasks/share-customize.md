---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: [Customization, Alfresco Share]
option: [Share, customize]
---

# Customizing Alfresco Share configuration items

This section describes how to customize Alfresco Share configuration items.

A number of options are available to customize Alfresco Share. Many of these mechanisms are provided by the underlying Surf platform, therefore a knowledge of Surf is useful for anyone wishing to implement substantial customizations.

To configure the Share application, you can use the custom configuration file named share-config-custom.xml.sample.

1.  Open the following file:

    <web-extension\>\\share-config-custom.xml.sample

2.  Uncomment any <config\> items that you want to enable.

3.  Add any <config\> items that you want to include.

4.  Save the edited file without the .sample extension.


-   **[Share repository document library](../concepts/share-repodoclib.md)**  
The Share repository document library is a feature that gives full access to the Alfresco repository.
-   **[Configuring the Share default port](../tasks/share-change-port.md)**  
This section describes how to configure the default port configuration for Alfresco Share.
-   **[Configuring the RSS Feed Dashlet with HTTP authentication](../tasks/rss-http-config.md)**  
This section describes how to enable the RSS Feed Dashlet for accessing sites over secure connections is a JDK configuration issue connected with absence of certificate\(s\) of the target feeds sender in the JDK keystore. To do this, you must add the certificate\(s\) from each site into the keystore of the JDK.
-   **[Enabling Google Docs integration](../tasks/googledocs-enable.md)**  
The Google Docs integration enables documents from Google Docs to be imported into the Alfresco repository, and therefore benefit from Alfresco features, such as checkin and checkout. Google Docs is disabled by default.
-   **[Share themes](../concepts/themes-intro.md)**  
When you run Alfresco Share, the look and feel is set by a default theme. This section describes how to select one of the alternative themes available in Share, and also how to create and use your own themes for corporate branding.
-   **[Forms](../concepts/forms-intro.md)**  
Alfresco Share presents data view and entry forms throughout its user interface, which are built on the Surf framework. This framework provides a convention for implementing forms.

**Parent topic:**[Customizing and extending Alfresco Share](../concepts/dev-Share-intro.md)

