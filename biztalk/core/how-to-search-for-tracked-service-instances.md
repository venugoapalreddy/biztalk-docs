---
title: "How to Search for Tracked Service Instances | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b6337df9-8c2e-4d4a-a64b-cc040f83bd91
caps.latest.revision: 5
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Search for Tracked Service Instances
You can use the <strong>Query</strong> tab in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console to search for all tracked service instances. To locate service instances, you can search on the name and version of the assembly, the start and end times of its lifetime, the name or instance ID of the service class, host name, error code, and the state of the service instance.  

## Prerequisites  
 To perform this procedure, you must be logged on as a member of the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Operators group.  

### To search for tracked service instances  

1. Click <strong>Start</strong>, click <strong>Programs</strong>, click [!INCLUDE [btsBizTalkServerStartMenuItemui](../includes/btsbiztalkserverstartmenuitemui-md.md)], and then click [!INCLUDE [btsBizTalkServerAdminConsoleui](../includes/btsbiztalkserveradminconsoleui-md.md)].  

2. In the console tree, expand **BizTalk Server Administration**, and then click the BizTalk group.  

3. In the details pane, click the **New Query** tab.  

4. In the **Query Expression** group, in the **Value** column, select **Tracked Service Instances** from the drop-down list box.  

5. In the <strong>Field Name</strong> column, in the empty drop-down list box next to the asterisk (<strong>\</strong>*), select one or more of the following:  


   |                 Item                 |                     Description                      |
   |--------------------------------------|------------------------------------------------------|
   |    <strong>Assembly Name</strong>    |    Name of the assembly for the service instance.    |
   |  <strong>Assembly Version</strong>   |           Version of the service instance.           |
   |      <strong>End Time</strong>       |          End time of the service instance.           |
   |     <strong>Error Code</strong>      | Any error code associated with the service instance. |
   |      <strong>Host Name</strong>      |        The host name of the service instance.        |
   |   <strong>Maximum Matches</strong>   |          The number of matches to display.           |
   |    <strong>Service Class</strong>    |          The class of the service instance.          |
   | <strong>Service Instance ID</strong> |               The service instance ID.               |
   |    <strong>Service Name</strong>     |          The name of the service instance.           |
   |     <strong>Start Time</strong>      |       The start time of the service instance.        |
   |        <strong>State</strong>        |          The state of the service instance.          |


6. Complete the **Value** column as appropriate for the selection you made in the **Field Name** column.  

7. Continue adding additional lines to the query as appropriate by completing the **Field Name**, **Operator**, and **Values** columns, and then click **Run Query**.  

## See Also  
 [Using the Administration Console Query Tab](../core/using-the-administration-console-query-tab.md)