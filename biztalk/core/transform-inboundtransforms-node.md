---
title: "Transform (InboundTransforms Node) | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Transform node [binding file]"
ms.assetid: c1bad23e-78a4-4fd4-95ef-30601393d53c
caps.latest.revision: 5
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Transform (InboundTransforms Node)
The Transform node of the InboundTransforms node of a binding file contains specific information about a BizTalk Server map that is exported with the binding file.  

## Nodes in the Transform node  
 The following table lists the properties that can be set for this node of a binding file:  


| <strong>Name</strong> | <strong>Node Type</strong> | <strong>Data Type</strong> |           <strong>Description</strong>            | <strong>Restrictions</strong> | <strong>Comments</strong> |
|-----------------------|----------------------------|----------------------------|---------------------------------------------------|-------------------------------|---------------------------|
|       FullName        |         Attribute          |         xs:string          |        Specifies the full name of the map.        |         Not required          |   Default value: empty    |
| AssemblyQualifiedName |         Attribute          |         xs:string          | Specifies the assembly qualified name of the map. |         Not required          |   Default value: empty    |

