---
title: "Step 5: Create a Send Port to Deliver Acknowledgments to the ADT System Using the File Adapter | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "end-to-end tutorial, send ports"
  - "send ports, acknowledgements"
  - "creating, send ports"
  - "acknowledgements, send ports"
  - "send ports, creating"
ms.assetid: 565a2adf-fd86-46e3-8035-7e4748aefffc
caps.latest.revision: 7
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 5: Create a Send Port to Deliver Acknowledgments to the ADT System Using the File Adapter
In this step, you create the send port to generate acknowledgments using the File adapter.  

### To create the Tutorial_sendAck_ADT send port  

1. Using [!INCLUDE [btsWinNoVersion](../../includes/btswinnoversion-md.md)] Explorer, create the \<<em>drive</em>:\>\Program Files\Microsoft BizTalk \<version\> Accelerator for HL7\SDK\End-to-End Tutorial\Tutorial_sendAck_ADT folder.  

2. In the BizTalk Server Administration Console, right-click **Send Ports**, point to **New**, and then click **Static One-way Send Port**.  

3. In the Send Port Properties dialog box, do the following:  


   |            Use this             |                                             To do this                                              |
   |---------------------------------|-----------------------------------------------------------------------------------------------------|
   |      <strong>Name</strong>      |                             Type <strong>Tutorial_sendAck_ADT</strong>.                             |
   | <strong>Transport type</strong> |                        Select <strong>FILE</strong> from the drop-down list.                        |
   |   <strong>Configure</strong>    | Click <strong>Configure</strong> to open the <strong>File Transport Properties</strong> dialog box. |


4. In the FILE Transport Properties dialog box, do the following and then click **OK**.  


   |              Use this               |                                                                                  To do this                                                                                   |
   |-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Destination folder</strong> | Browse to <strong>\<</strong><em>drive</em><strong>:\>\Program Files\Microsoft BizTalk \<version\> Accelerator for HL7\SDK\End-to-End Tutorial\Tutorial_sendAck_ADT</strong>. |
   |     <strong>File name</strong>      |                                          Type <strong>%MessageID%.txt</strong> (replace the .xml extension with the .txt extension).                                          |


5. In the Send Port Properties dialog box, for **Send pipeline**, select **BTAHL72XPipelines.BTAHL72XSendPipeline**.  

6. In the left pane, click **Filters**, and then do the following:  

   > [!NOTE]
   >  The first filter means that you are subscribing for the acknowledgment message. The second filter means that you are subscribing to the acknowledgment that is destined for the publisher Tutorial_ADTSystem.  

    Click **OK** when you are ready to continue.  


   |                Use this                 |                                                         To do this                                                         |
   |-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |        <strong>Property</strong>        | Click the field under <strong>Property</strong>, and then select <strong>BTS.MessageType</strong> from the drop-down list. |
   |        <strong>Operator</strong>        |                                    Select <strong>==</strong> from the drop-down list.                                     |
   |         <strong>Value</strong>          |                        Type <strong>http://microsoft.com/HealthCare/HL7/2X#ACK_24_GLO_DEF</strong>.                        |
   |        <strong>Group By</strong>        |                                    Select <strong>OR</strong> from the drop-down list.                                     |
   | <strong>Property (second line)</strong> | Click the field under <strong>Property</strong>, and then select <strong>BTS.MessageType</strong> from the drop-down list. |
   |        <strong>Operator</strong>        |                                    Select <strong>==</strong> from the drop-down list.                                     |
   |         <strong>Value</strong>          |                        Type <strong>http://microsoft.com/HealthCare/HL7/2X#ACK_25_GLO_DEF.</strong>                        |
   |        <strong>Group By</strong>        |                                    Select <strong>AND</strong> from the drop-down list.                                    |
   |        <strong>Property</strong>        |           Under the first property, click the blank box, and then select <strong>BTAHL7Schemas.MSH5_1</strong>.            |
   |        <strong>Operator</strong>        |                                    Select <strong>==</strong> from the drop-down list.                                     |
   |         <strong>Value</strong>          |                                         Type <strong>Tutorial_ADTSystem</strong>.                                          |

   > [!NOTE]
   >  For the send port Tutorial_sendAck_ADT, BTAHL7 drops the acknowledgments at the file drop location \<*drive*\>:Program FilesMicrosoft BizTalk <version> Accelerator for HL7SDKEnd-to-End TutorialTutorial_sendAck_ADT.  

7. Click **Apply**, and then click **OK.**  

8. In the Administration Console, click **Send Ports**, right-click **Tutorial_sendAck_ADT**, and then click **Start**.  

   Proceed to [Step 6: Create a Send Port to Deliver the ADT^A03 Message to the RX System Using the File Adapter](../../adapters-and-accelerators/accelerator-hl7/step-6-create-send-port-to-deliver-adt^a03-message-to-rx-system-using-file.md).