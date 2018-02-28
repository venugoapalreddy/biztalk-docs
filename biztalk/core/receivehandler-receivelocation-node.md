---
title: "ReceiveHandler (ReceiveLocation Node) | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "ReceiveHandler node [binding file]"
ms.assetid: dd105052-ec71-4762-aa74-e8cdb806a6bf
caps.latest.revision: 5
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# ReceiveHandler (ReceiveLocation Node)
The ReceiveHandler node of the ReceiveLocation node of a binding file contains specific information about the receive handler associated with a transport that is exported with the binding file.  

## Nodes in the ReceiveHandler node  
 The following table lists the properties that can be set for this node of a binding file:  


|                                <strong>Name</strong>                                | <strong>Node Type</strong> | <strong>Data Type</strong> |                                    <strong>Description</strong>                                     | <strong>Restrictions</strong> |                                                 <strong>Comments</strong>                                                 |
|-------------------------------------------------------------------------------------|----------------------------|----------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
|                                        Name                                         |         Attribute          |         xs:string          |              Specifies the name of the receive handler associated with the transport.               |         Not required          |                                                   Default value: empty                                                    |
|                                     HostTrusted                                     |         Attribute          |         xs:boolean         |             Specifies whether the host associated with the receive handler is trusted.              |           Required            | Default value: none<br /><br /> Set to <strong>true</strong> if host is trusted, otherwise set to <strong>false</strong>. |
| [TransportType (ReceiveHandler Node)](../core/transporttype-receivehandler-node.md) |           Record           | ProtocolType (ComplexType) | Specifies the transport type, which is also the name of the adapter used with this receive handler. |           Required            |                                                    Default value: none                                                    |

