---
title: "Step 4: Creating the Fabrikam 0C4 Trading Partner Agreement | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "double action tutorial, creating agreements"
ms.assetid: a99c2cd1-0d42-4fae-a380-a53d77cd87d0
caps.latest.revision: 6
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 4: Creating the Fabrikam 0C4 Trading Partner Agreement
In this step, you create a trading partner agreement between Contoso and Fabrikam using the [!INCLUDE [btsCoName](../../includes/btsconame-md.md)]® [!INCLUDE [BTARN_CurrentVersion_FirstRef](../../includes/btarn-currentversion-firstref-md.md)] Management Console. You create a new trading partner agreement for the 0C4 Partner Interface Process (PIP).  

### To start the BTARN Management Console  

- Click <strong>Start</strong>, point to <strong>All Programs</strong>, point to <strong>Microsoft BizTalk \<version\> Accelerator for RosettaNet</strong>, and then click <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-4-creating-the-fabrikam-0c4-trading-partner-agreement.md) contains invalid char.
  Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console.  

### To create the 0C4 trading partner agreement  

1. In the <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-4-creating-the-fabrikam-0c4-trading-partner-agreement.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console, expand [!INCLUDE [btaBTARNNoVersionui](../../includes/btabtarnnoversionui-md.md)], right-click <strong>Agreements</strong>, point to <strong>New</strong>, and then click <strong>Agreement</strong>.  

2. In the New Agreement Properties dialog box, on the **General** tab, do the following:  


   |                Use this                |                               To do this                               |
   |----------------------------------------|------------------------------------------------------------------------|
   |         <strong>Name</strong>          |             Type <strong>Fabrikam_To_Contoso_0C4</strong>.             |
   | <strong>Process Configuration</strong> |    Select <strong>STD_0C4_R01.02</strong> from the drop-down list.     |
   |    <strong>My Organization</strong>    |       Select <strong>Fabrikam</strong> from the drop-down list.        |
   | <strong>Partner Organization</strong>  |        Select <strong>Contoso</strong> from the drop-down list.        |
   |     <strong>RNIF Version</strong>      |       Select <strong>V02.00.01</strong> from the drop-down list.       |
   |       <strong>Home Role</strong>       | Select <strong>Initiator (Initiator)</strong> from the drop-down list. |
   |         <strong>Usage</strong>         |         Select <strong>Test</strong> from the drop-down list.          |


3. Click the **Ports** tab, and then do the following:  


   |          Use this           |                                 To do this                                 |
   |-----------------------------|----------------------------------------------------------------------------|
   | <strong>Action URL</strong> | Type <strong>https://<contoso_machine>/BTARNApp/RNIFReceive.aspx</strong>. |
   | <strong>Signal URL</strong> | Type <strong>https://<contoso_machine>/BTARNApp/RNIFReceive.aspx</strong>. |
   |  <strong>Sync URL</strong>  | Type <strong>https://<contoso_machine>/BTARNApp/RNIFReceive.aspx</strong>. |


4. Click **OK**.  

5. Right-click the **Fabrikam_To_Contoso_0C4** agreement, and then click **Activate**.  

## See Also  
 [Step 5: Creating the Fabrikam 3A2 Trading Partner Agreement](../../adapters-and-accelerators/accelerator-rosettanet/step-5-creating-the-fabrikam-3a2-trading-partner-agreement.md)