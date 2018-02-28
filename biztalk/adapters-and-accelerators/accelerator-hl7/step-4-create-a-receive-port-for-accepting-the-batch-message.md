---
title: "Step 4: Create a Receive Port for Accepting the Batch Message | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a37eb334-c4ae-40d1-a433-bf0ab39c0765
caps.latest.revision: 8
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 4: Create a Receive Port for Accepting the Batch Message
In this step, you create and configure a port to receive the incoming batch.  

 You create a request-response (two-way) receive port, because the scenario includes the generation of application-accept acknowledgments for the individual messages in the batch. In two-way mode, the MLLP receive adapter will not accept a new incoming message until the receive pipeline has generated the acknowledgment (ACK) for the previous message.  

## Create the receive port for accepting the batch message  

1. Open **BizTalk Server Administration**, expand **BizTalk Server Administration**, expand **BizTalk Group**, expand **Applications**, and then expand **BizTalk Application 1**.  

   > [!NOTE]
   >  The BizTalk Server Administration Console can also be opened from within Visual Studio by clicking **BizTalk Server Administration** in the **Tools** menu.  

2. Right-click **Receive Ports**, select **New**, and then select **Request Response Receive Port**.  

3. For the **Name**, enter **Tutorial_2WayReceive**.  

4. Select **Apply** to bind the port, and then select **Receive Locations**.  

5. Select **New**.  

6. For the **Name**, enter **Tutorial_2WayReceive**.

7. In the **Transport** section, select **Type**, and then select **MLLP** from the drop-down list.  

8. Select **Configure**. In **MLLP Transport Properties**, configure the following, and then select **OK**.  


   |                 Use this                  |                                                                                                                                                                                                                  To do this                                                                                                                                                                                                                   |
   |-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Connect retry time (sec)</strong> |                                                                 New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>The upper limit of time to wait before attempting to reconnect a dropped or closed connection. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.<br/><br/>Default is 20 seconds.                                                                  |
   | <strong>Connection initiated by</strong>  | New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter <strong>Local</strong> for the MLLP receive location to initiate the connection to a remote LOB server. This is the new option.<br/><br/>Enter <strong>Remote</strong> for the MLLP receive location to continue to listen for a connection from the remote LOB server. This is the backwards-compatible default option.<br/><br/>Default is Remote. |
   |     <strong>Connection Name</strong>      |                                                                                                                                                                                                         Enter <strong>2Way</strong>.                                                                                                                                                                                                          |
   |        <strong>Host name</strong>         |                                                                                                                                                     Specific to [!INCLUDE [bts2013r2_md](../../includes/bts2013r2-md.md)] and older versions. <br/><br/>Enter <strong>localhost</strong>.                                                                                                                                                     |
   |     <strong>Local Host name</strong>      |                                                                                  New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the DNS name or IP address of the local [!INCLUDE [btsBizTalkServerNoVersion_md](../../includes/btsbiztalkservernoversion-md.md)]. You can also enter <strong>localhost</strong>.                                                                                   |
   |           <strong>Port</strong>           |                                                                                                                                                      Specific to [!INCLUDE [bts2013r2_md](../../includes/bts2013r2-md.md)] and older versions. <br/><br/>Set to <strong>21000</strong>.                                                                                                                                                       |
   |        <strong>Local Port</strong>        |                                                                                 New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the TCP port number for the LocalHost connection. Applicable only when <strong>Connection Initiated by</strong> is <strong>Remote</strong>. <br/><br/>Set to <strong>21000</strong>.                                                                                 |
   |       <strong>Remote Host</strong>        |                                                                                                   New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the DNS name or IP address of the remote LOB server. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.                                                                                                    |
   |       <strong>Remote Port</strong>        |                                                                                New starting with [!INCLUDE [bts2016_md](../../includes/bts2016-md.md)]. <br/><br/>Enter the TCP port number for the remote host connection. Applicable when <strong>Connection Initiated by</strong> is set to <strong>Local</strong>.<br/><br/>Set to <strong>21000</strong>.                                                                                |


9. In the Receive Location properties, select the following:  


   |             Use this              |                                To do this                                |
   |-----------------------------------|--------------------------------------------------------------------------|
   | <strong>Receive Handler</strong>  | Select <strong>BizTalkServerApplication</strong> from the drop-down list |
   | <strong>Receive Pipeline</strong> |    Select <strong>BTAHL72XPipelines.BTAHL72XReceivePipeline</strong>     |
   |  <strong>Send Pipeline</strong>   |      Select <strong>BTAHL72XPipelines.BTAHL72XSendPipeline</strong>      |


10. Select **OK** to save your changes.  

11. Enable the receive location you just created by right-clicking it, and then select **Enable**.  

## Next step
[Step 5: Create a Send Port to Deliver Messages](../../adapters-and-accelerators/accelerator-hl7/step-5-create-a-send-port-to-deliver-messages.md)