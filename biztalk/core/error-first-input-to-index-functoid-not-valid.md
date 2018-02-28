---
title: "Error - First Input to Index Functoid Not Valid | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bts10.map.error.firstInputToIndexNotValid"
ms.assetid: f7dbe9cc-9cfa-4fc7-af3e-1241cb2b50a9
caps.latest.revision: 8
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Error - First Input to Index Functoid Not Valid
**Error Code**  
  
 btm1015  
  
 **Explanation**  
  
 The first input parameter to the indicated **Index** functoid is not from a **Field** node within a looping **Record** node in the source schema.  
  
 **User Action**  
  
 Create the appropriate input link by dragging between a <strong>Field</strong> node within a looping <strong>Record</strong> node in the source schema and the indicated <strong>Index</strong> functoid. It may be necessary to open the <strong>Configure \<Functoid\> Functoid</strong> dialog box by selecting the indicated <strong>Index</strong> functoid and clicking the ellipsis (<strong>...</strong>) button associated with the <strong>Input Parameters</strong> property in the Microsoft [!INCLUDE [btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] Properties window in order to ensure that the newly created link is the first input parameter to the indicated <strong>Index</strong> functoid.