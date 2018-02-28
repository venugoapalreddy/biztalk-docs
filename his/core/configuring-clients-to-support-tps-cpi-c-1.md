---
title: "Configure Clients to Support TPs (CPI-C) | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b02b239d-04a2-4707-a8fa-d26222019d3d
caps.latest.revision: 3
author: "gplarsen"
ms.author: "hisdocs; plarsen"
manager: "anneta"
---
# Configure Clients to Support TPs (CPI-C)

## Overview
On client computers, invokable transaction programs (TPs) are configured through the Windows registry.  

> [!NOTE]
>  On client computers, the recommended method for setting registry variables for autostarted invokable TPs is to use the sample TP configuration program, TPSETUP. Compile INSTALL.C, the source code for TPSETUP, for the target environment. When you write an installation program for autostarted invokable TPs, it is recommended that you add code similar to TPSETUP to the installation program.   

 For clients it is recommended that autostarted invokable TPs be written as Windows services. Be sure to include code like that in TPSETUP in the program that installs your TPs. Among other things, TPSETUP shows how to use the **CreateService** function when installing a TP.  

 The following table lists the registry entries used for the types of invokable TPs that can be run on Windows client computers.  


|                                                        Type of TP                                                         |                                                                                                                                    Location in registry                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                             Possible registry entries                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                Autostarted invokable TP running as a service on a client.                                 |                                        <strong>HKEY_LOCAL_MACHINE</strong><br /> <strong>SYSTEM</strong><br /> <strong>CurrentControlSet</strong><br /> <strong>Services</strong> <br /> <strong><em>TPName</em></strong><br /><br /> (and subkeys)                                        | Registry entries created by the <strong>CreateService</strong> call, including entries that specify the path, display name, and other characteristics of the service.<br /><br /> —plus—<br /><br /> Linkage OtherDependencies:REG_MULTI_SZ:SnaBase<br /><br /> Parameters SNAServiceType:REG_DWORD:0x5 LocalLU:REG_SZ:<em>LUalias</em> Parameters:REG_SZ:<em>ParameterList</em> Timeout:REG_DWORD:<em>number</em> AcceptNames:REG_SZ:<em>TPNameList</em> ConversationSecurity:REG_SZ:{ YES &#124; NO } AlreadyVerified:REG_SZ:{ YES &#124; NO }<em>Username1</em>:REG_SZ:<em>Password1</em> ...<em>UsernameX</em>:REG_SZ:<em>PasswordX</em><br /><br /> For more information, see the notes following this table. |
| Autostarted invokable TP running as an application on a client. For more information, see the notes following this table. | <strong>HKEY_LOCAL_MACHINE</strong><br /> <strong>SYSTEM</strong><br /> <strong>CurrentControlSet</strong><br /> <strong>Services</strong><br /> <strong>SnaBase</strong><br /> <strong>Parameters</strong><br /> <strong>TPs</strong> <br /> <strong><em>TPName</em></strong>  Parameters |                           <strong>SNAServiceType:</strong>REG_DWORD:{ 0x5 &#124; 0x6 }<strong>PathName:</strong>REG_EXPAND_SZ:<em>path</em><strong>LocalLU:</strong>REG_SZ:<em>LUalias</em><strong>Parameters:</strong>REG_SZ:<em>ParameterList</em><strong>TimeOut:</strong>REG_DWORD:<em>number</em><strong>AcceptNames:</strong>REG_SZ:<em>TPNameList</em><strong>ConversationSecurity:</strong>REG_SZ:{ YES &#124; NO }<strong>AlreadyVerified:</strong>REG_SZ:{ YES &#124; NO }<strong><em>Username1</em>:</strong>REG_SZ:<em>Password1</em> ...<strong><em>UsernameX</em>:</strong>REG_SZ:<em>PasswordX</em><br /><br /> For more information, see the notes following this table.                           |
|                              Operator-started invokable TP running as a service on a client.                              |                                        <strong>HKEY_LOCAL_MACHINE</strong><br /> <strong>SYSTEM</strong><br /> <strong>CurrentControlSet</strong><br /> <strong>Services</strong> <br /> <strong><em>TPName</em></strong><br /><br /> (and subkeys)                                        |                                         Registry entries created by the <strong>CreateService</strong> call, including entries that specify the path, display name, and other characteristics of the service.<br /><br /> —plus—<br /><br /> Linkage OtherDependencies:REG_MULTI_SZ:SnaBase<br /><br /> Parameters SNAServiceType:REG_DWORD:0x1A LocalLU:REG_SZ:<em>LUalias</em> Timeout:REG_DWORD:<em>number</em> ConversationSecurity:REG_SZ:{ YES &#124; NO } AlreadyVerified:REG_SZ:{ YES &#124; NO }<em>Username1</em>:REG_SZ:<em>Password1</em> ...<em>UsernameX</em>:REG_SZ:<em>PasswordX</em><br /><br /> For more information, see the note following this table.                                         |
|                           Operator-started invokable TP running as an application on a client.                            | <strong>HKEY_LOCAL_MACHINE</strong><br /> <strong>SYSTEM</strong><br /> <strong>CurrentControlSet</strong><br /> <strong>Services</strong><br /> <strong>SnaBase</strong><br /> <strong>Parameters</strong><br /> <strong>TPs</strong> <br /> <strong><em>TPName</em></strong>  Parameters |                                                                                                                     <strong>SNAServiceType:</strong>REG_DWORD:0x1A<strong>LocalLU:</strong>REG_SZ:<em>LUalias</em><strong>TimeOut:</strong>REG_DWORD:<em>number</em><strong>ConversationSecurity:</strong>REG_SZ:{ YES &#124; NO }<strong>AlreadyVerified:</strong>REG_SZ:{ YES &#124; NO }<strong><em>Username1</em>:</strong>REG_SZ:<em>Password1</em> ...<strong><em>UsernameX</em>:</strong>REG_SZ:<em>PasswordX</em><br /><br /> For more information, see the note following this table.                                                                                                                     |

> [!NOTE]
>  Before an autostarted TP can be started as an application on a client, the TPSTART program must be started. 

> [!NOTE]
>  AlreadyVerified and Username/Password entries are used only if ConversationSecurity is set to YES.  

## Next steps

-   [Registry Entries for Clients (CPI-C)](../core/registry-entries-for-clients-cpi-c-1.md)  

-   [Example of Registry Entries (CPI-C)](../core/example-of-registry-entries-cpi-c-1.md)