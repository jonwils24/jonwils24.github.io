---
author: [Alfresco Documentation, Alfresco Documentation]
source: 
audience: 
category: [Installation, Configuration, WQS]
option: Web Quick Start
---

# Installing Web Quick Start on an existing Alfresco Enterprise install

If you have an existing Alfresco Enterprise installation, you can use the standalone installation wizard for installing Web Quick Start.

Ensure that Alfresco is not running before you start the WQS installer.

1.  Download the Web Quick Start installer.

    \(Windows\) alfresco-enterprise-wcmqs-<version\>-win-installer.exe

    \(Linux\) alfresco-enterprise-wcmqs-<version\>-linux-installer.bin

    \(Mac\) alfresco-enterprise-wcmqs-<version\>-osx-installer.app.tar.gz \(the uncompressed file is alfresco-enterprise-wcmqs-<version\>-osx-installer\)

2.  Run the setup wizard.

3.  In the Setup – Alfresco Enterprise Quick Start window, click **Next**.

4.  In the Installation Directory window, enter the directory where Alfresco Enterprise is installed, and then click **Next**.

    The installer tries to locate the default Alfresco installation directory:

    \(Windows\) C:\\Alfresco

    \(Linux\) /op/alfresco

    \(Mac\) /Applications/alfresco-<version\>

    The installation starts.

5.  In the Completing the Alfresco Enterprise Quick Start Setup Wizard window, ensure that you deselect the checkbox to automatically launch Share, and then click **Finish**.

6.  Delete the existing alfresco and share directories.

7.  Restart the Alfresco server.


**Parent topic:**[Web Quick Start](../concepts/WQS-intro.md)

