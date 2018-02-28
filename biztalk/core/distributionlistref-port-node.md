---
title: "DistributionListRef (Port Node) | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "DistributionListRef node [binding file]"
ms.assetid: 5d0d0121-1bcc-4c26-a1a3-8937ac7c282a
caps.latest.revision: 9
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# DistributionListRef (Port Node)
The DistributionListRef node of the Port node of a binding file contains information about a distribution list that is referenced by a service.  

> [!NOTE]
>  Distribution lists are referred to as send port groups in the BizTalk Server Administration Console.  

## Nodes in the DistributionListRef node  
 The following table lists the properties that can be set for this node of a binding file:  


| <strong>Name</strong> | <strong>Node Type</strong> | <strong>Data Type</strong> |                        <strong>Description</strong>                        | <strong>Restrictions</strong> | <strong>Comments</strong> |
|-----------------------|----------------------------|----------------------------|----------------------------------------------------------------------------|-------------------------------|---------------------------|
|         Name          |         Attribute          |         xs:string          | Specifies the name of a distribution list that is referenced by a service. |         Not required          |   Default value: empty    |

