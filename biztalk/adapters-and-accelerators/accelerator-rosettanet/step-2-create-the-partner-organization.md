---
title: "Step 2: Create the Partner Organization | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "partner organization"
  - "trading partners, partner organization"
  - "loopback tutorial, creating partner organization"
ms.assetid: 489bc961-dcb6-4610-989d-c06ba9f71b02
caps.latest.revision: 7
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 2: Create the Partner Organization
In this step, you create the partner organization using the [!INCLUDE [btsCoName](../../includes/btsconame-md.md)]® [!INCLUDE [BTARN_CurrentVersion_FirstRef](../../includes/btarn-currentversion-firstref-md.md)] Management Console.  

### To create the partner organization  

1. In the  <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/accelerator-rosettanet/step-2-create-the-partner-organization.md) contains invalid char.
   Parameter name: path -->[!INCLUDE[BTARN_CurrentVersion_abbrev](../../includes/btarn-currentversion-abbrev-md.md)]<!--END ERROR INCLUDE --></strong> Management Console, expand <strong>BizTalk \<version\> Accelerator for RosettaNet</strong>, right-click <strong>Partners</strong>, click <strong>New</strong>, and then click <strong>Partner</strong>.  

2. In the **New Partner Properties** dialog box, do the following:  


   |       Use this        |            To do this            |
   |-----------------------|----------------------------------|
   | <strong>Name</strong> |  Type <strong>PARTNER</strong>.  |
   | <strong>GBI</strong>  | Type <strong>987654321</strong>. |


3. In the **New Partner Properties** dialog box, on the **Contact Properties** tab, do the following:  


   |              Use this              |                  To do this                  |
   |------------------------------------|----------------------------------------------|
   |   <strong>Contact Name</strong>    |       Type <strong>Jane Doe</strong>.        |
   |  <strong>E-mail Address</strong>   |   Type <strong>jdoe@fabrikam.com</strong>.   |
   | <strong>Telephone Number</strong>  |     Type <strong>555-555-5555</strong>.      |
   |    <strong>Fax Number</strong>     |     Type <strong>555-555-5555</strong>.      |
   | <strong>Supply chain code</strong> | Type <strong>Electronic Components</strong>. |


4. Click **Apply**, and then **OK**.  

> [!NOTE]
>  If you have an encryption certificate, you configure it here. For information about configuring encryption certificates, see [Managing Certificates](../../adapters-and-accelerators/accelerator-rosettanet/managing-certificates1.md).  

## See Also  
 [Step 3: Edit the Partner Interface Process](../../adapters-and-accelerators/accelerator-rosettanet/step-3-edit-the-partner-interface-process.md)