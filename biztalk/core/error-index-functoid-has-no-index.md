---
title: "Error - Index Functoid Has No Index | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bts10.map.error.indexFunctoidHasNoIndex"
ms.assetid: a523705e-6134-4d98-8ea6-dbfc7b43dae5
caps.latest.revision: 8
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Error - Index Functoid Has No Index
**Error Code**  
  
 btm1014  
  
 **Explanation**  
  
 No index value(s) have been provided for the indicated **Index** functoid.  
  
 **User Action**  
  
 Provide an appropriate number of index input parameters for the indicated <strong>Index</strong> functoid, where the appropriate number is determined by the number of looping <strong>Record</strong> nodes within which the <strong>Field</strong> node in the source schema is nested. To created index input parameters, select the indicated functoid, click the ellipsis (<strong>...</strong>) button associated with the <strong>Input Parameters</strong> property in the Microsoft [!INCLUDE [btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] Properties window, and then use the  ![](../core/media/bts-tls-paraminsert.gif "bts_tls_paraminsert") button within the <strong>Configure \<Functoid\> Functoid</strong> dialog box to add one or more constant input parameters, where the first one represents an index into the immediate parent looping <strong>Record</strong> node, and subsequent index input parameters represent increasingly remote ancestor looping <strong>Record</strong> nodes.