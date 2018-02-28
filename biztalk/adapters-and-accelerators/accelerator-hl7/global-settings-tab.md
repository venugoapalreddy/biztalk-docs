---
title: "Global Settings Tab | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "btahl7.configurationexplorer.tab.globalsettings"
helpviewer_keywords: 
  - "configuring, auditing"
  - "configuring, logging"
  - "logging, configuring"
  - "Global Settings tab [Configuration Explorer]"
  - "auditing, configuring"
ms.assetid: 057189f7-9072-4841-950f-371ba1f73a15
caps.latest.revision: 6
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Global Settings Tab
You use the <strong>Global Settings</strong> tab to configure the logging store used by [!INCLUDE [HL7_CurrentVersion_FirstRef](../../includes/hl7-currentversion-firstref-md.md)].  

 In the **BTAHL7 Configuration Explorer** dialog box, on the **Global Settings** tab, do the following:  


|            Use this            |                                                                                                                                                       To do this                                                                                                                                                        |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      <strong>WMI</strong>      |                                                                        Select this option if you want to generate [!INCLUDE [btsWinNoVersion](../../includes/btswinnoversion-md.md)] Management Instrumentation (WMI) notifications for BTAHL7.                                                                         |
|      <strong>SQL</strong>      | Select this option if you want to use [!INCLUDE [btsCoName](../../includes/btsconame-md.md)][!INCLUDE [btsSQLServerNoVersion](../../includes/btssqlservernoversion-md.md)] as your logging store for BTAHL7. <strong>Note:</strong>  BTAHL7 automatically creates the tables required for logging if they do not exist. |
|  <strong>SQL Server</strong>   |            Type the [!INCLUDE [btsSQLServerNoVersion](../../includes/btssqlservernoversion-md.md)] name. This is required when you select the <strong>SQL</strong> option. The maximum allowed length is 64 characters.<br /><br /> The default server and database name is the configured BTAHL7 database.             |
| <strong>Database name</strong> |                                                 Type the [!INCLUDE [btsSQLServerNoVersion](../../includes/btssqlservernoversion-md.md)] database name. This is required when you select the <strong>SQL</strong> option. The maximum allowed length is 128 characters.                                                  |
|   <strong>Event Log</strong>   |                       Select this option if you want to use the [!INCLUDE [btsWinNoVersion](../../includes/btswinnoversion-md.md)] Event Log as the logging store for BTAHL7. You use the [!INCLUDE [btsWinNoVersion](../../includes/btswinnoversion-md.md)] Event Viewer to view event messages.                       |

