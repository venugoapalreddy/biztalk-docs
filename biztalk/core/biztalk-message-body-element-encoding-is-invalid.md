---
title: "BizTalk message body element encoding is invalid | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b407e5c3-4655-4b2f-8ecc-30eb080ec47c
caps.latest.revision: 9
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# BizTalk message body element encoding is invalid
## Details  
  
|                 |                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------|
|  Product Name   |              [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]               |
| Product Version |                          [!INCLUDE [btsWCFVersion](../includes/btswcfversion-md.md)]                           |
|    Event ID     |                                                       0                                                        |
|  Event Source   |                                                       0                                                        |
|    Component    |                                                       0                                                        |
|  Symbolic Name  |                                                       0                                                        |
|  Message Text   | BizTalk message body element encoding "{0}" is invalid. Expected encoding: "xml", "base64", "hex", or "string" |
  
## Explanation  
 This error indicates the use of the BizTalk body template option for the outgoing messages; however, the encoding type specified for the BizTalk body is invalid.  
  
## User Action  
 Use the following procedure to configure the encoding type.  
  
#### To configure the encoding type  
  
1. Click <strong>Start</strong>, click <strong>All Programs</strong>, click [!INCLUDE [btsBizTalkServerStartMenuItemui](../includes/btsbiztalkserverstartmenuitemui-md.md)], and click <strong>BizTalk Server Administration</strong>.  
  
2. In the Console Root, expand [!INCLUDE [btsBizTalkServerAdminConsoleui](../includes/btsbiztalkserveradminconsoleui-md.md)], expand <strong>BizTalk Group</strong>, and expand  <strong>Applications</strong>.  
  
3. Locate your application and then locate your transport.  
  
4. Right-click the transport name.  
  
5. Click **Properties**.  
  
6. In the port **Type** list, select the correct port.  
  
7. Click **Configure**.  
  
8. In the <strong>WCF [</strong><em>transport type</em><strong>] Transport Properties</strong> dialog box, click the <strong>Messages</strong> tab.  
  
9. In the <strong>Outbound WCF message body</strong> section, click the <strong>Template – Content specified by template</strong> radio button. In the <strong>XML</strong> text box, the format of the BizTalk body should be   
    \<<strong>bts-msg-body xmlns="<http://www.microsoft.com/schemas/bts2007>" encoding="[xml&#124;base64&#124;hex&#124;string]"/</strong>\>  (valid values, which are case-sensitive, for encoding are xml&#124;base64&#124;hex&#124;string)