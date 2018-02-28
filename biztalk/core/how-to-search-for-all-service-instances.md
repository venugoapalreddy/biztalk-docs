---
title: "How to Search for All Service Instances | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "service instances, Query tab [Administration Console]"
  - "Query tab [Administration Console], service instances"
  - "Query tab [Administration Console], searching"
  - "service instances, searching"
  - "instances, services"
ms.assetid: 48cb885c-aaf1-44e8-9810-2e70cf63db81
caps.latest.revision: 18
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Search for All Service Instances
You can use the **Query** tab in the BizTalk Server Administration Console to search for all service instances. You cannot unenlist a specific service type if there are any running or suspended instances. For example, before you can unenlist a specific service type, you can search for all service instances to ensure that there are no running or suspended instances.  

> [!NOTE]
>  When Grouping and Filtering by URI, only send and receive ports are displayed in the results. Grouping and Filtering by URI is not possible for orchestrations, which are not included in the displayed results.  

## Prerequisites  
 To perform this procedure, you must be logged on as a member of the BizTalk Server Operators group.  

### To search for all service instances  

1. Click <strong>Start</strong>, click <strong>All Programs</strong>, click [!INCLUDE [btsBizTalkServerStartMenuItemui](../includes/btsbiztalkserverstartmenuitemui-md.md)], and then click <strong>BizTalk Server Administration</strong>.  

2. In the console tree, expand [!INCLUDE [btsBizTalkServerAdminConsoleui](../includes/btsbiztalkserveradminconsoleui-md.md)], and then click the BizTalk group.  

3. In the details pane, click the **New Query** tab.  

4. In the **Query Expression** group, in the **Value** column, select **All In-Progress Service Instances** from the drop-down list box.  

5. In the <strong>Field Name</strong> column, in the empty drop-down list box next to the asterisk (<strong>\</strong>*), select one or more of the following:  


   |               Use this               |                                                                                                              To do this                                                                                                              |
   |--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  <strong>Application Name</strong>   |                                                                                                   The BizTalk Server application.                                                                                                    |
   |    <strong>Creation Time</strong>    |                                                                                Find all service instances created before or after the specified date.                                                                                |
   |  <strong>Group Results By</strong>   |                                                              You can group results by application, host name, service class, service instance status, or service name.                                                               |
   |      <strong>Host Name</strong>      |                                                                                                    The name of the BizTalk Host.                                                                                                     |
   |   <strong>Instance Status</strong>   | You can search for all running instances, all suspended instances, active instances, dehydrated instances, ready to run instances, scheduled instances, suspended but not resumable instances, or suspended and resumable instances. |
   |   <strong>Maximum Matches</strong>   |               The number of matches to display (required). This is usually set to 50, the default.<br /><br /> When you include Group Results By, this displays the number of groups, not the total number of records.               |
   |    <strong>Service Class</strong>    |                                                 You can search for isolated adapters; messaging; messaging, and isolated adapters; MSMQT; Orchestration; or Routing Failure Report.                                                  |
   | <strong>Service Instance ID</strong> |                                                                                  You can group or filter service instances by service instance ID.                                                                                   |
   |    <strong>Service Name</strong>     |                                                                                      You can group or filter service instances by service name.                                                                                      |
   |   <strong>Service Type ID</strong>   |                                                                                    You can group or filter service instances by service type ID.                                                                                     |


6. Complete the **Value** column as appropriate for the selection you made in the **Field Name** column.  

7. Continue adding additional lines to the query as appropriate, by completing the **Field Name**, **Operator**, and **Values** columns, and then click **Run Query**.  

## See Also  
 [Using the Administration Console Query Tab](../core/using-the-administration-console-query-tab.md)