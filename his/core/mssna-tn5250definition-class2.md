---
title: "MsSna_TN5250Definition Class2 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 10936ed6-a32a-46ff-b3c2-326233dc2820
caps.latest.revision: 4
author: "gplarsen"
ms.author: "hisdocs; plarsen"
manager: "anneta"
---
# MsSna_TN5250Definition Class
The definition of a TN5250 session.  
  
 The following syntax is simplified from MOF code.  
  
## Syntax  
  
```  
  
class MsSna_TN5250Definition : MsSna_Config  
{  
   String Name;  
   String Service;  
   String RemoteLUAlias;  
   String LocalLUAlias;  
   String Comment;  
   String User;  
   String Password;  
   String Mode;  
   sint32 TermTypes;  
   sint32 Port;  
};  
```  
  
#### Parameters  
 <strong>Name</strong>  
 Data Type: <strong>String</strong> Qualifiers<strong>: Key,MAXLEN(10)</strong> Access Type: Read/Write  
  
 The session name.  
  
 **Service**  
 Data Type: **String** Qualifiers: **MAXLEN(20), TOUPPERCASE** Access Type: Read/Write  
  
 The SNA service to which this session belongs.  
  
 <strong>RemoteLUAlias</strong>  
 Data Type: <strong>String</strong> Qualifiers: <strong>MAXLEN(8)</strong>Access Type: Read/Write  
  
 The local LU alias used in the session.  
  
 **LocalLUAlias**  
 Data Type: **String** Qualifiers: **MAXLEN(8)** Access Type: Read/Write  
  
 The local LU alias used in the session.  
  
 <strong>Comment</strong>  
 Data Type: <strong>String</strong> Qualifiers: <strong>MAXLEN(25)</strong>Access Type: Read/Write  
  
 An optional comment field.  
  
 <strong>User</strong>  
 Data Type: <strong>String</strong> Qualifiers: <strong>MAXLEN(10)</strong>Access Type: Read/Write  
  
 The AS/400 user name used in the session.  
  
 <strong>Password</strong>  
 Data Type: <strong>String</strong> Qualifiers: <strong>MAXLEN(10)</strong>Access Type: Read/Write  
  
 The AS/400 password used in the session.  
  
 **Mode**  
 Data Type: **String** Access Type: Read/Write  
  
 The mode used in the session (QPCSUPP).  
  
 **TermTypes**  
 Data Type: **String** Qualifiers: **QualiferValueHere** Access Type: Read/Write  
  
 The terminal types allowed for the session. The following list describes the possible values for **TermType.**  
  
- 5555_C01  
  
- 5555_B01  
  
- 3477_FC  
  
- 3180_2  
  
- 3179_2  
  
- 3196_A1  
  
- 5292_2  
  
- 5291_1  
  
- 5251_11  
  
  <strong>Port</strong>  
  Data Type: <strong>sint32</strong> Qualifiers: <strong>MINVALUE(0), MAXVALUE(9999)</strong>Access Type: Read/Write  
  
  The port used for the session. By default the value is 0.  
  
## Requirements  
 **Platforms**: Windows Server 2003 R2 SP2, Windows Vista SP2, Windows 7, Windows Server 2008 SP2, Windows Server 2012  
  
## See Also  
 [WMISNA WMI Provider Classes](../core/wmisna-wmi-provider-classes2.md)   
 [Administration and Management Programmer's Guide](./administration-and-management-programmer-s-guide2.md)