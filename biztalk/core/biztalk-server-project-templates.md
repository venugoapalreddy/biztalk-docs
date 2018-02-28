---
title: "Visual Studio project templates | Microsoft Docs"
description: Describes the .btproj, BPEL, and .btaproj Visual Studio templates used by BizTalk Server
ms.custom: ""
ms.date: "11/07/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c2b3d494-db80-4314-afcd-d08d5a26e211
caps.latest.revision: 12
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# BizTalk Server Project Templates

## Overview
When you install [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)], the installation adds the BizTalk Projects folder to the <strong>New Project</strong> dialog box. The BizTalk Projects folder contains templates for creating an empty BizTalk Server project, BizTalk Server BPEL Import project, and a BizTalk Server Application Project.

## Available templates
The following table describes these project templates.  


|                            Use this                            |                                                                                                                                                                   To do this                                                                                                                                                                    |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|         <strong>Empty BizTalk Server Project</strong>          |                                                                                                                                                   Creates a new empty BizTalk Server project.                                                                                                                                                   |
|      <strong>BizTalk Server BPEL Import Project</strong>       |                                                                                       Imports Business Process Execution Language (BPEL), Web Services Description Language (WSDL), or XML Schema Definition Language (XSD) files into a BizTalk project.                                                                                       |
| <strong>BizTalk Server Application Project (.btaproj)</strong> | Starting with [!INCLUDE [bts2016](../includes/bts2016-md.md)] [Feature Pack 1](../core/configure-the-feature-pack.md), or later. <br/><br/>Used to automatically deploy and update applications using Visual Studio Team Services (VSTS). The project contains a `BizTalkServerInventory.json` file that is used by VSTS during the deployment. |

## See Also  
 [Working with BizTalk Projects](../core/working-with-biztalk-projects.md)
