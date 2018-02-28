---
title: "Step 4: Create a Trade Agreement | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "creating, trade agreeements"
  - "loopback tutorial, creating trade agreements"
  - "agreements, creating"
ms.assetid: 9bcb80b1-fefc-4f1c-ae03-fb736cdfd524
caps.latest.revision: 7
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 4: Create a Trade Agreement
In this step, you create a trade agreement between the home and partner organization using the [!INCLUDE [btsCoName](../../includes/btsconame-md.md)]® [!INCLUDE [BTARN_CurrentVersion_FirstRef](../../includes/btarn-currentversion-firstref-md.md)] Management Console.  

### To create a trade agreement  

1. In the <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-4-create-a-trade-agreement.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console, expand <strong>BizTalk \<version\> Accelerator for RosettaNet</strong>, right-click <strong>Agreements</strong>, click <strong>New</strong>, and then click <strong>Agreement</strong>.  

2. In the **New Agreement Properties** dialog box, on the **General** tab, do the following:  


   |                Use this                |                           To do this                            |
   |----------------------------------------|-----------------------------------------------------------------|
   |         <strong>Name</strong>          |             Type <strong>Trade Agreement</strong>.              |
   | <strong>Process Configuration</strong> | Select <strong>STD_0C1_R01.02</strong> from the drop-down list. |
   |    <strong>My organization</strong>    |      Select <strong>HOME</strong> from the drop-down list.      |
   | <strong>Partner organization</strong>  |    Select <strong>PARTNER</strong> from the drop-down list.     |
   |       <strong>Home role</strong>       |   Select <strong>Initiator</strong> from the drop-down list.    |


3. In the **New Agreement Properties** dialog box, on the **Ports** tab, do the following:  


   |          Use this           |                                         To do this                                         |
   |-----------------------------|--------------------------------------------------------------------------------------------|
   | <strong>Action URL</strong> |             Type <strong>http://localhost/BTARNApp/RNIFReceive.aspx</strong>.              |
   | <strong>Signal URL</strong> |             Type <strong>http://localhost/BTARNApp/RNIFReceive.aspx</strong>.              |
   |  <strong>Sync URL</strong>  | Leave blank. Sync URL is not required for the synchronous Partner Interface Process (PIP). |


4. Click **Apply**, and then click **OK**.  

   After you create the trade agreement, you must activate it.  

### To activate the trade agreement  

- In the [!INCLUDE [BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)] Management Console, expand [!INCLUDE [btaBTARNNoVersionui](../../includes/btabtarnnoversionui-md.md)], click <strong>Agreements</strong>, right-click <strong>Trade Agreement</strong> in the results pane, and then click <strong>Activate</strong>.  

## See Also  
 [Step 5: Create a Mirror Agreement](../../adapters-and-accelerators/accelerator-rosettanet/step-5-create-a-mirror-agreement.md)