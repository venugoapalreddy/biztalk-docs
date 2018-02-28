---
title: "Batch Definition Tab | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "btahl7.configurationexplorer.tab.batchdefinition"
helpviewer_keywords: 
  - "Batch Definition tab [Configuration Explorer]"
  - "batching, configuring"
  - "configuring, batching"
ms.assetid: fe8685ef-5de5-4337-8691-8e4094056ace
caps.latest.revision: 4
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Batch Definition Tab
You use the **Batch Definition** tab to enable inbound batching, batch in/batch out batching, and select available schemas for outbound batching.  

 In the **BTAHL7 Configuration Explorer** dialog box, on the **Batch Definition** tab, do the following:  


|                         Use this                          |                                                                                                                                                                                                         To do this                                                                                                                                                                                                          |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          <strong>Fragmentation required</strong>          |                                                                        Select one of the following options:<br /><br /> -   <strong>Yes</strong>. To enable fragmentation.<br />-   <strong>No</strong>. To disable fragmentation. <strong>Note:</strong>  For a new party, <strong>Fragmentation Required</strong> defaults to <strong>No</strong>.                                                                        |
| <strong>Recoverable interchange support required</strong> | Select one of the following options:<br /><br /> -   <strong>True</strong>. To enable recoverable interchange support.<br />-   <strong>FALSE</strong>. To disable recoverable interchange support. <strong>Note:</strong>  For a new party, <strong>Fragmentation Required</strong> defaults to <strong>FALSE</strong> and is enabled only if the value of <strong>Fragmentation Required</strong> is <strong>No</strong>. |
|             <strong>Select Messages</strong>              |                                                                     Select the message types you want to send as a batch from the Available Messages window and then click the Move to right arrow (<strong>>></strong>).<br /><br /> To batch incoming ACK messages, you must add the ACK message type. You do so by deploying the ACK message schema.                                                                     |
|      <strong>Select Message Acknowledgments</strong>      |                                                                      Select the message types for which you want [!INCLUDE [btaBTAHL71.3abbrevnonumber](../../includes/btabtahl71-3abbrevnonumber-md.md)] to send the acknowledgments as a batch from the Available Message Acks window, and then click the Move to right arrow (<strong>>></strong>).                                                                      |

