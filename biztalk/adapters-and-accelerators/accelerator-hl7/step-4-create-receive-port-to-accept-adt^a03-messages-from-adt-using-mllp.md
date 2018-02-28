---
title: "Step 4: Create the Receive Port for Accepting ADT^A03 Messages from ADT Systems Using the MLLP Adapter | Microsoft Docs"
ms.custom: ""
ms.date: "2015-12-09"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "receive ports"
  - "end-to-end tutorial, receive ports"
  - "creating, receive ports"
ms.assetid: 3c4192d5-d011-48b0-a3f9-47c5225780ee
caps.latest.revision: 9
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 4: Create the Receive Port for Accepting ADT^A03 Messages from ADT Systems Using the MLLP Adapter
You use the receive port to specify the receive location for incoming messages. Use the following procedure to create the receive port for accepting ADT^A03 messages from the ADT System using the MLLP adapter.  

## Create the receive port  

1. Open **BizTalk Server Administration**, expand **BizTalk Server Administration**, expand **BizTalk Group**, expand **Applications**, and then expand **BizTalk Application 1**.  

   > [!NOTE]
   >  The BizTalk Server Administration Console can also be opened from within Visual Studio by clicking **BizTalk Server Administration** in the **Tools** menu.  

2. Right-click **Receive Ports**, select **New**, and then select **One-way Receive Port**.  

3. For the **Name**, enter **Tutorial_1WayReceive**.  

4. Select **Apply** to bind the port, and then select **Receive Locations**.  

5. Select **New**.  

6. For the **Name**, enter **Tutorial_MLLPReceive**.  

7. In the **Transport** section, select **Type**, and then select **MLLP** from the drop-down list.  

8. Select **Configure**. In **MLLP Transport Properties**, configure the following, and then select **OK**.  


   |                 Use this                  |                                                                                                                                                                                                                  To do this                                                                                                                                                                                                                   |
   |-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Connect retry time (sec)</strong> |                                                                 New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>The upper limit of time to wait before attempting to reconnect a dropped or closed connection. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.<br/><br/>Default is 20 seconds.                                                                  |
   | <strong>Connection initiated by</strong>  | New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter <strong>Local</strong> for the MLLP receive location to initiate the connection to a remote LOB server. This is the new option.<br/><br/>Enter <strong>Remote</strong> for the MLLP receive location to continue to listen for a connection from the remote LOB server. This is the backwards-compatible default option.<br/><br/>Default is Remote. |
   |     <strong>Connection Name</strong>      |                                                                                                                                                                                                         Enter <strong>1Way</strong>.                                                                                                                                                                                                          |
   |        <strong>Host name</strong>         |                                                                                                                                                     Specific to [!INCLUDE [bts2013r2_md](../../includes/bts2013r2-md.md)] and older versions. <br/><br/>Enter <strong>localhost</strong>.                                                                                                                                                     |
   |     <strong>Local Host name</strong>      |                                                                                  New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the DNS name or IP address of the local [!INCLUDE [btsBizTalkServerNoVersion_md](../../includes/btsbiztalkservernoversion-md.md)]. You can also enter <strong>localhost</strong>.                                                                                   |
   |           <strong>Port</strong>           |                                                                                                                                                    Specific to [!INCLUDE [bts2013r2_md](../../includes/bts2013r2-md.md)] and older versions. <br/><br/>Default is <strong>11000</strong>.                                                                                                                                                     |
   |        <strong>Local Port</strong>        |                                                                               New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the TCP port number for the LocalHost connection. Applicable only when <strong>Connection Initiated by</strong> is <strong>Remote</strong>. <br/><br/>Default is <strong>11000</strong>.                                                                               |
   |       <strong>Remote Host</strong>        |                                                                                                   New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the DNS name or IP address of the remote LOB server. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.                                                                                                    |
   |       <strong>Remote Port</strong>        |                                                                                                    New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the TCP port number for the remote host connection. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.                                                                                                    |


9. Set the **Receive Handler** to **BizTalkServerApplication**.  

10. Set the **Receive Pipeline** to **BTAHL72XPipelines.BTAHL72XReceivePipeline**.  

11. Select **OK** to save your changes.  

12. Enable the receive location you just created by right-clicking it, and then select **Enable**.  

## Next step  
[Step 5: Create a Send Port to Deliver Acknowledgments to the ADT System Using the File Adapter](../../adapters-and-accelerators/accelerator-hl7/step-5-create-send-port-to-deliver-acknowledgments-to-adt-system-using-file.md)