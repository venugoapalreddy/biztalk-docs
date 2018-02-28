---
title: "Warning - Promoted Field XPath Not Found | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bts10.edit.error.promoFieldXPathNotFound"
ms.assetid: 21b8c240-5d6f-499d-8211-6e3f2ce2a79c
caps.latest.revision: 6
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Warning - Promoted Field XPath Not Found
**Error Code**  
  
 BEC1005  
  
 **Explanation**  
  
 The node corresponding to the indicated property field promotion may not exist in the schema. BizTalk Editor cannot resolve complex XPath specifications, and if you edited the promoted property XPath in the **Edit Instance XPath** dialog box, it may or may not correctly identify the node you intended to promote.  
  
 **User Action**  
  
 You can keep this warning from appearing by changing the XPath for the promoted property in the <strong>Edit Instance XPath</strong> dialog box, which you can access from cells in the <strong>Node Path</strong> column of the <strong>Property Field List</strong> table on the <strong>Property Fields</strong> tab in the <strong>Promote Properties</strong> dialog box. You can access the <strong>Promote Properties</strong> dialog box from the <strong>Promote Properties</strong> property of the <strong>Schema</strong> node in the Microsoft® [!INCLUDE [btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] Properties window.