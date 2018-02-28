---
title: "Step 7: Create a Send Port to Deliver Response Messages | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "interrogative tutorial, send ports"
ms.assetid: 5edaefb6-72f2-4317-9477-f3a0d0027e0c
caps.latest.revision: 3
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 7: Create a Send Port to Deliver Response Messages
In this step, you create the send port to deliver the query responses back to the Admissions, Discharge, and Transfer (ADT) system.  

### To create the ADT_Send send port  

1. In the BizTalk Server Administration Console, right-click **Send Ports**, point to **New**, and then select **Static One-way Send Port**.  

2. In the Send Port Properties dialog box, do the following:  


   |            Use this             |                                     To do this                                     |
   |---------------------------------|------------------------------------------------------------------------------------|
   |      <strong>Name</strong>      |                          Type <strong>ADT_Send</strong>.                           |
   | <strong>Transport type</strong> |                           Select <strong>MLLP</strong>.                            |
   |   <strong>Configure</strong>    | Click the <strong>Configure</strong> button to the right of <strong>Type</strong>. |


3. In the MLLP Transport Properties dialog box, enter the following information, and then click **OK**.  


   |             Use this             |             To do this              |
   |----------------------------------|-------------------------------------|
   | <strong>Connection Name</strong> | Type <strong>ADT_SendMLLP</strong>. |
   |      <strong>Host</strong>       |  Type <strong>localhost</strong>.   |
   |      <strong>Port</strong>       |    Type <strong>25000</strong>.     |


4. In the Send Port Properties dialog box, for **Send Pipeline**, select **BTAHL72XPipelines.BTAHL72XSendPipeline**.  

5. In the Console Tree, click **Filters**, and then do the following:  


   |         Use this          |                                              To do this                                               |
   |---------------------------|-------------------------------------------------------------------------------------------------------|
   | <strong>Property</strong> |                               Select <strong>BTS.MessageType</strong>.                                |
   | <strong>Operator</strong> |                          Select <strong>==</strong> from the drop-down list.                          |
   |  <strong>Value</strong>   |           Type <strong>http://microsoft.com/HealthCare/HL7/2X#DSR_Q01_24_GLO_DEF</strong>.            |
   | <strong>Group By</strong> |                         Select <strong>AND</strong> from the drop-down list.                          |
   | <strong>Property</strong> | Under the first property, click the blank box, and then select <strong>BTAHL7Schemas.MSH5_1</strong>. |
   | <strong>Operator</strong> |                          Select <strong>==</strong> from the drop-down list.                          |
   |  <strong>Value</strong>   |                                      Type <strong>ADT</strong>.                                       |

   > [!NOTE]
   >  The first filter specifies that the send port only selects messages conforming to the DSR^Q01 schema you created in step 3A. The second filter specifies the destination to which the [!INCLUDE [btaBTAHL71.3abbrevnonumber](../../includes/btabtahl71-3abbrevnonumber-md.md)] Interface Engine sends these messages.  

6. Click **OK**.  

7. In the Administration Console, click **Send Ports**, right-click **ADT_Send**, and then click **Start**.  

   Proceed to [Step 8: Configure Party Information](../../adapters-and-accelerators/accelerator-hl7/step-8-configure-party-information-hl7-main.md).