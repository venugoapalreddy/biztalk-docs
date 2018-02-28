---
title: "How to Search for Tracked Message Events | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 18df4cf7-c307-4175-926c-9be9f30b29ed
caps.latest.revision: 8
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Search for Tracked Message Events
You can use the <strong>New Query</strong> tab in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console to search for tracked message events.  From the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console you can enable message body and message property tracking. In the Query Results pane you can view information about the message event, including schema information, event type, service instance ID, and all the promoted properties for the generated message.  

> [!NOTE]
>  In order to view the actual message body, you can invoke the **Message Details** context menu and go to the “Message Parts” tab, or save the message from the result list view by invoking **Save to File** from the context menu.  

## Prerequisites  
 To perform this procedure, you must be logged on as a member of the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Operators group.  

### To search for tracked message items  

1. Click <strong>Start</strong>, click <strong>All Programs</strong>, click [!INCLUDE [btsBizTalkServerStartMenuItemui](../includes/btsbiztalkserverstartmenuitemui-md.md)], and then click [!INCLUDE [btsBizTalkServerAdminConsoleui](../includes/btsbiztalkserveradminconsoleui-md.md)].  

2. In the console tree, expand **BizTalk Server Administration**, and then click the BizTalk group.  

3. In the details pane, click the **New Query** tab.  

4. In the **Query Expression** group, in the **Value** column, select **Tracked Message Events** from the drop-down list box.  

5. In the <strong>Field Name</strong> column, in the empty drop-down list box next to the asterisk (<strong>\</strong>*), select one or more of the following:  


   |                               Item                               |                                              Description                                               |
   |------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
   |                  <strong>Creation Time</strong>                  |                                   The time the message was created.                                    |
   |                   <strong>Event Type</strong>                    |                                    The type of event being tracked.                                    |
   |                 <strong>Maximum Matches</strong>                 |                                   The number of matches to display.                                    |
   |                      <strong>Party</strong>                      |                                The organization that sent the message.                                 |
   |                      <strong>Port</strong>                       |                                 The port used to process the message.                                  |
   |                   <strong>Schema Name</strong>                   |                                Name of the schema used by the message.                                 |
   |               <strong>Service Instance ID</strong>               |                             The service instance ID used for the message.                              |
   |                       <strong>URI</strong>                       |                                     The URI used for the message.                                      |
   | <strong>\<Select a Schema Name for Tracked Properties\></strong> | When you select a schema, any promoted properties in that schema are eligible to be used in the query. |


6. Complete the **Value** column as appropriate for the selection you made in the **Field Name** column.  

7. Continue adding additional lines to the query as appropriate by completing the **Field Name**, **Operator**, and **Values** columns, and then click **Run Query**.  

## See Also  
 [Using the Administration Console Query Tab](../core/using-the-administration-console-query-tab.md)