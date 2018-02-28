---
title: "The Sample Operations Error Handler | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Ops adapters, error handler"
  - "process management solution tutorial, Ops adapters"
ms.assetid: e6c55f01-c004-4340-beaa-d77764ae34c1
caps.latest.revision: 11
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# The Sample Operations Error Handler
The sample operations error handler has three major assemblies: **OperationsClient**, **OperationsHandler**, and **OperationsServer**.  
  
 The solution configures the adapter to use the **OpsClient** object in the **OperationsClient** assembly. As you'd expect, the **OpsClient** object implements the **IOpsAIC** interface.  
  
 The <strong>OpsClient</strong> object uses the <strong>IOperationsSystem</strong> interface to call the <strong>OpsHandler</strong> object through the [!INCLUDE [btsDotNetFramework](../includes/btsdotnetframework-md.md)] remoting feature. The <strong>IOperationsSystem</strong> interface appears as follows:  
  
```  
public interface IOperationsSystem  
{  
    void Initialize(string initData);  
    void Post(string originMachine, byte[] message);  
}  
  
```  
  
 The <strong>OperationsServer</strong>, a console application, listens for requests for the <strong>OpsHandler</strong> object and acts as the server for the [!INCLUDE [btsDotNetFramework](../includes/btsdotnetframework-md.md)] remoting feature. Calling the <strong>Execute</strong> method of the <strong>OpsClient</strong> object in turn invokes the <strong>Post</strong> method of the <strong>OpsHandler</strong> object.  
  
 The <strong>OpsHandler</strong> methods respond by writing out their argument strings using the <strong>Trace</strong> object. This posts the errors to the console. For more information about the <strong>Trace</strong> object, see "Trace Class" in the [!INCLUDE [btsDotNetFramework](../includes/btsdotnetframework-md.md)] Class Library.  
  
> [!NOTE]
>  The pattern here is the same as that in the **OrderHandler** in which an interface specifies the method calls between a client and a remoted object. There is, however, an additional layer of indirection here between the **OpsClient** and the **OpsHandler**.  
  
## See Also  
 [The Ops Adapter](../core/the-ops-adapter.md)