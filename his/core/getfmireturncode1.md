---
title: "GetFmiReturnCode1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6383b568-6918-4e60-8379-873239056f44
caps.latest.revision: 3
author: "gplarsen"
ms.author: "hisdocs; plarsen"
manager: "anneta"
---
# GetFmiReturnCode
The **GetFmiReturnCode** function converts link status and error codes to a printable string. This function provides a standard set of error strings for use by Function Management Interface (FMI) applications.  

## Syntax  

```  

int WINAPI GetFmiReturnCode (  
    UINT errcode1,  
    UINT errcode2,  
    UINT buffer_length,  
    unsigned char FAR *buffer_addr  
);  
```  

#### Parameters  
 *errcode1*  
 Supplied parameter; see Remarks.  

 *errcode2*  
 Supplied parameter; see Remarks.  

 *buffer_length*  
 Supplied parameter; specifies the length of the buffer pointed to by *buffer_addr*. The recommended length is 256 characters.  

 *buffer_addr*  
 Supplied/returned parameter; specifies the address of the buffer that will hold the formatted, null-terminated string.  

## Return Values  
 0x20000001  
 The parameters are invalid; the function could not read the specified error codes or could not write to the specified buffer.  

 0x20000002  
 The specified buffer is too small.  

## Remarks  
 The *errcode1* and *errcode2* parameters are set according to the way that **GetFmiReturnCode** is used, as shown in the following table.  


|                                                                                                                                                                                                         Codes to be translated                                                                                                                                                                                                         |        Value for <em>errcode1</em>        | Value for <em>errcode2</em> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|-----------------------------|
| The <em>errcode1</em> and <em>errcode2</em> values specified in [Error and Sense Codes](./error-and-sense-codes2.md) includes messages for<strong>Open(SSCP) Response</strong>, <strong>Open(PLU) Confirm</strong>, <strong>Status-Acknowledge(Nack-2)</strong>, <strong>Status-Control(...) Nack2</strong>, <strong>Status-Error</strong>, and <strong>Appl-Data</strong> messages with the system detected error indicator (SDI) set |          Unchanged from message           |   Unchanged from message    |
|                                                                                                                                                                  The status and qualifier codes returned from a [Status-Session](../core/status-session2.md) message                                                                                                                                                                   | <em>status</em>\*256 + <em>qualifier</em> |           0xFFFF            |
|                                                                                                                                                                                     The return code from <strong>WinLUAGetLastInitStatus</strong>                                                                                                                                                                                      |              The return code              |           0xFFFF            |

