---
title: "SendHandler (SecondaryTransport Node) | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "SendHandler node [binding file]"
ms.assetid: 32eb3e87-25ac-461e-9c09-3d6d9bcba3b2
caps.latest.revision: 6
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# SendHandler (SecondaryTransport Node)
The SendHandler node of the SecondaryTransport node of a binding file contains specific information about the send handler associated with a transport that is exported with the binding file.  

## Nodes in the SendHandler node  
 The following table lists the properties that can be set for this node of a binding file:  


|                             <strong>Name</strong>                             | <strong>Node Type</strong> | <strong>Data Type</strong> |                                   <strong>Description</strong>                                   | <strong>Restrictions</strong> |                                                 <strong>Comments</strong>                                                 |
|-------------------------------------------------------------------------------|----------------------------|----------------------------|--------------------------------------------------------------------------------------------------|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
|                                     Name                                      |         Attribute          |         xs:string          |              Specifies the name of the send handler associated with the transport.               |         Not required          |                                                   Default value: empty                                                    |
|                                  HostTrusted                                  |         Attribute          |         xs:boolean         |             Specifies whether the host associated with the send handler is trusted.              |           Required            | Default value: none<br /><br /> Set to <strong>true</strong> if host is trusted, otherwise set to <strong>false</strong>. |
| [TransportType (SendHandler Node)](../core/transporttype-sendhandler-node.md) |           Record           | ProtocolType (ComplexType) | Specifies the transport type, which is also the name of the adapter used with this send handler. |           Required            |                                                    Default value: none                                                    |

