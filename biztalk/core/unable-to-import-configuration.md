---
title: "Unable to import configuration | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2887da50-4f74-4259-a7d6-c87bc9b9fc58
caps.latest.revision: 10
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Unable to import configuration
## Details  
  
|                 |                                                                                     |
|-----------------|-------------------------------------------------------------------------------------|
|  Product Name   | [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] |
| Product Version |             [!INCLUDE [btsWCFVersion](../includes/btswcfversion-md.md)]             |
|    Event ID     |                                          0                                          |
|  Event Source   |                                          0                                          |
|    Component    |                                          0                                          |
|  Symbolic Name  |                                          0                                          |
|  Message Text   |                   Unable to import configuration from file "{0}"                    |
  
## Explanation  
 There could be multiple reasons for this error:  
  
-   The configuration file may contain invalid character in the given encoding.  
  
-   The root element may be missing.  
  
-   The data at the root level may be invalid.  
  
> [!NOTE]
>  This situation, and the user action, applies only to WCF-Custom and WCF-CustomIsolate adapters.  
  
## User Action  
 Use the following procedure to import a valid configuration file.  
  
#### To import a valid configuration file  
  
1. Click <strong>Start</strong>, click <strong>All Programs</strong>, click [!INCLUDE [btsBizTalkServerStartMenuItemui](../includes/btsbiztalkserverstartmenuitemui-md.md)], and click <strong>BizTalk Server Administration</strong>.  
  
2. In the Console Root, expand [!INCLUDE [btsBizTalkServerAdminConsoleui](../includes/btsbiztalkserveradminconsoleui-md.md)], expand <strong>BizTalk Group</strong>, and expand  <strong>Applications</strong>.  
  
3. Locate your application and then locate your transport.  
  
4. Right-click the transport name.  
  
5. Click **Properties**.  
  
6. In the port **Type** list, select the correct port.  
  
7. Click **Configure**.  
  
8. In the <strong>WCF [</strong><em>transport type</em><strong>] Transport Properties</strong> dialog box, click the <strong>Import/Export</strong> tab.  
  
9. Click **Import**. Import a valid and complete configuration file.  
  
   You can also verify the validity of the configuration file by opening it with the Service Configuration Editor **(Start > All Programs > Windows SDK)** (this step assumes you have the Windows SDK installed.) Open **svcConfigEditor.exe** and verify each property of the configuration file.