---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: Customization
option: extended services MIME type
---

# Adding a MIME type

This section describes how to add a MIME type definition.

There are two files that contain MIME type default definitions:

-   <configRoot\>mimetype-map.xml
-   <configRoot\>mimetype-map-openoffice.xml

Do not edit these files directly. Instead, override the `mimetypeConfigService` bean in an extension file.

1.  Open the <extension\>\\mimetypes-extension.xml.sample file.

2.  Modify the inserted MIME type to match your requirements.

3.  Save the file without the .sample extension.

4.  Ensure that the MIME type extension file is pointed to in the mimetype-map-extension-context.xml file.

    This file contains the following line, which points to your modified file:

    ```
    <value\>classpath:alfresco/extension/mimetypes-extension.xml</value\>
    ```


**Parent topic:**[Configuring the repository](../concepts/intro-core.md)

