---
title: "How to Configure an MSMQ Send Port | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "MSMQ adapters, send ports"
  - "send ports, MSMQ adapters"
  - "configuring [MSMQ adapters], send ports"
ms.assetid: 37313d45-8148-4aaf-a3f2-ea05b3b8b448
caps.latest.revision: 29
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Configure an MSMQ Send Port
You can set MSMQ send port adapter variables in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console. If properties are not set for the send port, the default send handler values set in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console are used.  

> [!IMPORTANT]
>  If a host instance is associated with an MSMQ send port or receive location, verify the MSMQ service is running on that machine. If the service is not running, the MSMQ receive ports will shut down shortly after they are started, and messages sent to the MSMQ send ports will be suspended.  
>   
>  In a clustered scenario, not only does the clustered MSMQ instance need to be running, but the local MSMQ service on each cluster machine should be running, as well.  

## To configure variables for an MSMQ send port  
 Follow these steps to configure variables for an MSMQ send port:  

1. In the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console, create a new send port or double-click an existing send port to modify it. See [How to Create a Send Port](../core/how-to-create-a-send-port2.md) for more information. Configure all of the send port options. On the <strong>General</strong> tab, in the <strong>Transport</strong> section, specify <strong>MSMQ</strong> for the <strong>Type</strong> option.  

2. On the **General** tab, in the **Transport** section, click the **Configure** button next to **Type**.  

3. In the **MSMQ Transport Properties** dialog box, do the following:  


   |                  Use this property                   |                                                                                                                                                 To do this                                                                                                                                                  |  Data type  | Default value |
   |------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|---------------|
   |              <strong>Password</strong>               |                                                                                                                Specify the password for a remote queue. Use with <strong>User Name</strong>.                                                                                                                |   String    |     Blank     |
   |              <strong>User Name</strong>              |                                                                            Specify the user name for a remote queue. Use with <strong>Password</strong>. You cannot use the local user of the remote computer for the user name.                                                                            |   String    |     Blank     |
   |        <strong>Acknowledgement Type</strong>         |                Specify the type of acknowledgement message for Message Queuing to return to the sending application. You can select more than one acknowledgment type. Any of the acknowledgement types in the <strong>System.Messaging.AcknowledgeTypes</strong> enumeration are available.                |   String    |     None      |
   |        <strong>Administration Queue</strong>         |                                                                                                                      Specify the queue name that receives the acknowledgement message.                                                                                                                      |   String    |     Blank     |
   |              <strong>Body Type</strong>              |                                                                                              Specify the message body type in MSMQ. Valid values are members of the .NET <strong>VarEnum</strong> enumeration.                                                                                              |     Int     |     8209      |
   |       <strong>Certificate Thumbprint</strong>        |      Specify the thumbprint of the certificate to use for message authentication. Use this property in combination with the <strong>Use Authentication</strong> property to verify the message. Use the <strong>User Name</strong> and <strong>Password</strong> properties to gain access to queues.       |   String    |     Blank     |
   |          <strong>Destination Queue</strong>          |                                    Specify the destination queue. For more information about queues, see [Message Queuing Queues](../core/message-queuing-queues.md). <strong>Note:</strong>  The URI for a send port or receive location cannot exceed 256 characters.                                     |   String    |     Blank     |
   |        <strong>Encryption Algorithm</strong>         |                                                                                                  Select <strong>RC2</strong>, <strong>RC4</strong>, or <strong>None</strong> for the encryption algorithm.                                                                                                  |    Enum     |     None      |
   | <strong>Maximum Message Size (in kilobytes)</strong> |                                                                                                             Specify the maximum message size for messages that you send to the specified queue.                                                                                                             | UnsignedInt |     1024      |
   |          <strong>Message Priority</strong>           |                                                                                                                                          Set the message priority.                                                                                                                                          |    Enum     |    Normal     |
   |             <strong>Recoverable</strong>             |                                                                                                                        Specify whether to guarantee the recoverability of a message.                                                                                                                        |   Boolean   |     False     |
   |        <strong>Support Segmentation</strong>         |                                                                                                       Set this Boolean property value to <strong>True</strong> to segment messages larger than 4 MB.                                                                                                        |   Boolean   |     False     |
   |               <strong>Timeout</strong>               |                                                                                          Specify the maximum time to wait for the messages to reach the destination queue. Applies only when you use transactions.                                                                                          |     Int     |       0       |
   |            <strong>Timeout Unit</strong>             |                                                           Set the unit to use for the <strong>Timeout</strong> property.<br /><br /> Select <strong>Days</strong>, <strong>Hours</strong>, <strong>Minutes</strong>, or <strong>Seconds</strong>.                                                           |    Enum     |     Days      |
   |            <strong>Transactional</strong>            |                                                                                                              Set this value to <strong>True</strong> to send messages if you use transactions.                                                                                                              |   Boolean   |     False     |
   |         <strong>Use Authentication</strong>          | Set this Boolean property value to <strong>True</strong> to control authentication. Use this property in combination with the <strong>Certificate Thumbprint</strong> property to verify the message. Use the <strong>User Name</strong> and <strong>Password</strong> properties to gain access to queues. |   Boolean   |     False     |
   |        <strong>Use Dead Letter Queue</strong>        |                                                                                                   Set this value to <strong>True</strong> to send messages to the dead letter queue if a failure occurs.                                                                                                    |   Boolean   |     True      |
   |          <strong>Use Journal Queue</strong>          |                                                                                                  Set this value to <strong>True</strong> to save a copy of the message whenever the message is processed.                                                                                                   |   Boolean   |     False     |


4. Click **OK** and **OK** again to save settings.  

## See Also  
 [How to Configure an MSMQ Receive Location](../core/how-to-configure-an-msmq-receive-location.md)   
 [Configuring the MSMQ Adapter](../core/configuring-the-msmq-adapter.md)