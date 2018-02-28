---
title: "Step 2: Creating the Contoso Partner Organization | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "double action tutorial, creating partner organizations"
ms.assetid: ebb3b166-3781-40b9-89d4-2ca0c83d05f3
caps.latest.revision: 7
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 2: Creating the Contoso Partner Organization
In this step, you use the [!INCLUDE [btsCoName](../../includes/btsconame-md.md)]® [!INCLUDE [BTARN_CurrentVersion_FirstRef](../../includes/btarn-currentversion-firstref-md.md)] Management Console to create a new trading partner. The trading partner for this tutorial is the Contoso organization.  

### To start the BTARN Management Console  

- Click <strong>Start</strong>, point to <strong>All Programs</strong>, point to <strong>Microsoft BizTalk \<version\> Accelerator for RosettaNet</strong>, and then click <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-2-creating-the-contoso-partner-organization.md) contains invalid char.
  Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console.  

### To create Fabrikam as a trading partner  

1. In the <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-2-creating-the-contoso-partner-organization.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console, expand [!INCLUDE [btaBTARNNoVersionui](../../includes/btabtarnnoversionui-md.md)], right-click <strong>Partners</strong>, point to <strong>New</strong>, and then click <strong>Partner</strong>.  

2. In the New Partner Properties dialog box, on the <strong>General</strong> tab, do the following<strong>:</strong>  


   |                Use this                 |                                    To do this                                    |
   |-----------------------------------------|----------------------------------------------------------------------------------|
   |          <strong>Name</strong>          |                          Type <strong>CONTOSO</strong>.                          |
   |          <strong>GBI</strong>           |                         Type <strong>123456789</strong>.                         |
   | <strong>Partner Classification</strong> |          Select <strong>Manufacturer</strong> from the drop-down list.           |
   | <strong>Signature Certificate</strong>  | Select <strong>Contoso Signature [Thumbprint]</strong> from the drop-down list.  |
   | <strong>Encryption Certificate</strong> | Select <strong>Contoso Encryption [Thumbprint]</strong> from the drop-down list. |


3. Click the **Contact Properties** tab, and then do the following:  


   |              Use this              |                  To do this                  |
   |------------------------------------|----------------------------------------------|
   |   <strong>Contact Name</strong>    |       Type <strong>John Doe</strong>.        |
   |  <strong>E-mail Address</strong>   |   Type <strong>jdoe@contoso.com</strong>.    |
   | <strong>Telephone Number</strong>  |     Type <strong>555-555-5555</strong>.      |
   |    <strong>Fax Number</strong>     |     Type <strong>555-555-5555</strong>.      |
   | <strong>Supply chain code</strong> | Type <strong>Electronic Components</strong>. |


4. Click **OK**.  

## See Also  
 [Step 3: Creating the Fabrikam 0C2 Trading Partner Agreement](../../adapters-and-accelerators/accelerator-rosettanet/step-3-creating-the-fabrikam-0c2-trading-partner-agreement.md)