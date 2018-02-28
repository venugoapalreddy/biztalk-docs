---
title: "Install and configure the Microsoft BizTalk ESB Toolkit | Microsoft Docs"
description: Step-by-steps instructions to install and configure the ESB Toolkit on BizTalk Server
caps.latest.revision: 8
author: "MandiOhlinger"
manager: "anneta"

ms.custom: ""
ms.date: "08/10/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 698843f7-8361-4d02-9278-0e66f2a9f472
ms.author: "mandia"
---

# Install and configure the Microsoft BizTalk ESB Toolkit
Starting with BizTalk Server 2013 and newer versions, [!INCLUDE [esbToolkit](../includes/esbtoolkit-md.md)] is integrated with the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] setup. This topic shows you how to install and configure [!INCLUDE [esbToolkit](../includes/esbtoolkit-md.md)], and also includes a community-written link to upgrade the ESB Toolkit.  

> [!IMPORTANT]
>  You must have BizTalk Server installed before you start installing the [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)].  

## Install 

1. Run the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] setup.exe file as Administrator. In setup, select <strong>Install <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[esbToolkit](../includes/esbtoolkit-md.md)]: Path(D:/a/1/s/target_repo/biztalk/esb-toolkit/install-and-configure-the-microsoft-biztalk-esb-toolkit.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[esbToolkit](../includes/esbtoolkit-md.md)]<!--END ERROR INCLUDE --></strong>.  

2. Accept the license agreement, and then select **Next**.  

3. In **Component Installation**, select the components you want to install, and then select **Next**.  

4. In the **Summary**, review what you chose, and then select **Install**.  

5. Select **Finish** to close the installation wizard.  

An install log file is created, similar to `C:\Users\yourUserName\AppData\Local\Temp\Setup(081017 175042).htm'. 

## Configure 

> [!IMPORTANT]
>  You must configure [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] before configuring [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)].  

1. From the <strong>Start</strong> menu, select <strong>Microsoft <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[esbToolkit](../includes/esbtoolkit-md.md)]: Path(D:/a/1/s/target_repo/biztalk/esb-toolkit/install-and-configure-the-microsoft-biztalk-esb-toolkit.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[esbToolkit](../includes/esbtoolkit-md.md)]<!--END ERROR INCLUDE --></strong>, and then select <strong>ESB Configuration Tool</strong>.  

   > [!IMPORTANT]
   >  Run the ESB Configuration Tool as an administrator.  

2. In the configuration, select <strong>Database Server</strong>. Enter the database server name that hosts the [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)] databases.   

3. In <strong>IIS Web Services</strong>, enter the user account and password that runs the IIS applications created by the [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)]. Next, enter the IIS website that hosts the applications.  

4. The **BizTalk User Groups** lists the default user groups typically used for ESB configuration.  

   > [!IMPORTANT]
   >  At this stage, you can select <strong>Apply Configuration</strong> to configure the [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)] with these default settings. However, if you want to do a custom configuration, complete the remaining steps. Rhe values you enter in the next steps take precedence over the default values.  

5. In the left pane, expand **ESB Configuration**, expand ** Exception Management**, and then:  

   -   If you don't want to configure an exception management database, then select **Database**, and uncheck the **Enable Exception Management Database**.

   -   If you want to use an existing database instead of creating a new database, then select **Database**, and select the **Use Existing Database**. Enter the database server name and the database name.  

   -   If you don't want to configure exception web service, then select **Exception Web Services**, and uncheck **Enable Exception Services**.  If you want to run these services under a different website, you can enter that here.  

6. In the left pane, expand **ESB Core Components**, and then:  

   -   If you don't want to configure an itinerary database, then select **Itinerary Database**, and uncheck **Itinerary Database** .  

   -   If you want to use an existing itinerary database, then select **Itinerary Database**, and select **Use Existing Database**. Enter the database server name and the database name.  

   -   If you don't want to configure these web service, then select **Core Web Services**, and uncheck **Enable Core Services**. If you want to run these services under a different website, you can enter that here.

7. In the left pane, select <strong>Configuration</strong>.  
   If you are installing and configuring the [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)] in a single server environment, select <strong>File Configuration Source</strong>. If you are setting up a multiple-machine deployment, select the <strong>SSO Configuration Source</strong>, and then enter the following:  

   -   **SSO Server**: Enter the name of the SSO server

   -   **Configuration file**: Select the ellipsis **(…)**, and then browse to the esb.config file (\Program Files (x86)\Microsoft BizTalk ESB Toolkit)

   -   **Application Name**: Enter a name for the SSO application. For example,  enter `ESB Toolkit`.  

   -   **Contact Information**: Enter a valid email address the appropriate contact information in the following format: `someone@example.com`.  

   -   **Administrator Group Name**: Select the ellipsis **(…)**, and then browse to the appropriate admin group  

   -   **User Group Name**: Select the ellipsis **(…)**, and then browse to the appropriate group  

8. Select <strong>Apply Configuration</strong>. Open IIS and notice that the applications required for [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)] are now created under the website you specified while configuring [!INCLUDE [esbToolkit_short](../includes/esbtoolkit-short-md.md)].  

9. In the **ESB Configuration Tool**, select **ESB BizTalk Applications**, and then:  

   - Select <strong>Enable ESB Core Components in BizTalk Server</strong> to create the application in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console. Select <strong>Use Default Binding</strong> to bind this application to the default host. Select <strong>Do not use Default Binding</strong> if you do not want to bind the application to the default host. In this scenario, you must explicitly bind the application to a host once the application is created.  

   - Select <strong>Enable ESB JMS/WMQ Components in BizTalk Server</strong> to create the application in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console. Select <strong>Use Default Binding</strong> to bind this application to the default host. Select <strong>Do not use Default Binding</strong> if you do not want to bind the application to the default host. In this scenario, you must explicitly bind the application to a host once the application is created.  

   - Select <strong>Apply Configuration</strong> to create the applications you selected. Verify that the applications are created in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console.  

## Upgrade ESB Toolkit – Community Addition  
 [In-place upgrade of ESB Toolkit 2.1 to 2.2](http://www.brianloesgen.com/blog/2013/10/10/in-place-upgrade-of-esb-toolkit-21-to-22.html) (http://www.brianloesgen.com/blog/2013/10/10/in-place-upgrade-of-esb-toolkit-21-to-22.html)

## See also
[Troubleshoot installation issues, and common errors & resolutions](troubleshooting-the-biztalk-esb-toolkit.md)