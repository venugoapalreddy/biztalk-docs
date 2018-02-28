---
title: "Error - Input Instance File Missing | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bts10.edit.error.inputInstanceFileMissing"
ms.assetid: b7271bee-19b0-41ae-b8b1-644034f7d877
caps.latest.revision: 7
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Error - Input Instance File Missing
**Explanation**  
  
 No input instance message file has been specified, preventing the **Validate Instance** command from running.  
  
 **User Action**  
  
 Right-click the relevant schema file in Microsoft [!INCLUDE [btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] Solution Explorer, and then click <strong>Properties</strong> to open the <strong>Property Pages</strong> dialog box for this schema. In this dialog box, on the <strong>General</strong> tab, click the ellipsis (<strong>...</strong>) button in the value field of the <strong>Input Instance Filename</strong> property, and then use the <strong>Select Input File</strong> dialog box to identify the file that contains the input instance message. You can also type the file name directly in the value field of the <strong>Input Instance Filename</strong> property.