---
title: "Step 5: Create the Send Port for the Message Batch | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5db815df-5b76-4ba4-99ab-c7766b0c301a
caps.latest.revision: 8
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 5: Create the Send Port for the Message Batch
In this step, you create a send port to deliver the message batch that you create to the destination party. This is a static one-way port with a FILE adapter type. You designate a file folder for the destination (\Tutorial_BatchMsgDrop) where [!INCLUDE [btsBizTalkServerNoVersion](../../includes/btsbiztalkservernoversion-md.md)] will drop the message batch file. You define a filter for the port indicating what type of message batches the ports will send. The filter specifies the destination of Tutorial_BatchDest and the message type of OutboundBatch.  

> [!NOTE]
>  When running this part of the tutorial, you can simplify the results by stopping the send port used in Part 2 of the tutorial: the **Tutorial_BTAHL7Drop** send port.  

### To create the send port for the message batch  

1. In the BizTalk Server Administration Console, right-click **Send Ports**, point to **New**, and then click **Static One-way Send Port**.  

2. In the Send Port Properties dialog box, do the following:  


   |          Use this          |                                     To do this                                     |
   |----------------------------|------------------------------------------------------------------------------------|
   |   <strong>Name</strong>    |                     Type <strong>Tutorial_BatchDest</strong>.                      |
   |   <strong>Type</strong>    |               Select <strong>FILE</strong> from the drop-down list.                |
   | <strong>Configure</strong> | Click <strong>Configure</strong> to open the FILE Transport Properties dialog box. |


3. In the **FILE Transport Properties** dialog box, do the following:  


   |              Use this               |                                                                                                                                                                                      To do this                                                                                                                                                                                      |
   |-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Destination folder</strong> | Browse to <strong>\<<em>drive</em>:\>\Program Files\Microsoft  BizTalk \<version\> Accelerator for HL7\SDK\End-to-End Tutorial\Tutorial_BatchMsgDrop</strong>. This is the path to the location on the file system or public share to which [!INCLUDE [btsBizTalkServerNoVersion](../../includes/btsbiztalkservernoversion-md.md)] will write the file containing the message batch. |
   |     <strong>File name</strong>      |                                                                                                                                             Type <strong>%MessageID%.txt</strong> (replace the .xml extension with the .txt extension).                                                                                                                                              |
   |     <strong>Copy mode</strong>      |                                                                                                                                                                         Select <strong>Create New</strong>.                                                                                                                                                                          |


4. Click **OK**.  

5. In the Send Port Properties dialog box, for **Send pipeline**, select **BTAHL72XPipelines.BTAHL72XSendPipeline**.  

6. In the console tree, click **Filters**, and then do the following:  


   |         Use this          |                                                                           To do this                                                                           |
   |---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Property</strong> | Click the field under <strong>Property</strong>, and then select <strong>Microsoft.Solutions.BTAHL7.BatchOrchestration.Party</strong> from the drop-down list. |
   | <strong>Operator</strong> |                                                           Leave <strong>==</strong> as the operator.                                                           |
   |  <strong>Value</strong>   |                                                           Type <strong>Tutorial_BatchDest</strong>.                                                            |
   | <strong>Group By</strong> |                                                      Select <strong>And</strong> from the drop-down list.                                                      |
   | <strong>Property</strong> |                                                    Select <strong>BTAHL7Schemas.BTAHL7MessageType</strong>.                                                    |
   | <strong>Operator</strong> |                                                           Leave <strong>==</strong> as the operator.                                                           |
   |  <strong>Value</strong>   |                                                              Type <strong>OutboundBatch</strong>.                                                              |


7. Press **Enter**. In the pane at the bottom of the dialog box, verify that you entered the filter expression correctly, and then click **OK**.  

8. In the BizTalk Administration Console, select **Send Ports**, right-click **Tutorial_BatchDest**, and then click **Start**.  

### To associate the send port with the destination party  

1. In the BizTalk Server Administration Console, expand **Parties**, click **Tutorial_BatchDest**, and then right-click **Properties**.  

2. In the Party Properties dialog box, click  **Send Ports** in the console tree.  Select **Tutorial_BatchDest** from the drop-down list, and then click **OK**.  

   > [!NOTE]
   >  If a concurrency violation occurs while the **Tutorial_DestBatch** party was being updated, click **OK** and close the dialog box. In the Administration Console, right-click **BizTalk Group**, click **Refresh**, and then repeat steps 1 and 2.  

   Proceed to [Step 6: Create the Send Port for the Acknowledgment Batch](../../adapters-and-accelerators/accelerator-hl7/step-6-create-the-send-port-for-the-acknowledgment-batch.md).