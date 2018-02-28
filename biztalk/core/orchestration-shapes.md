---
title: "Orchestration Shapes | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Delay shape [Orchestration Designer]"
  - "Loop shape [Orchestration Designer]"
  - "Throw Exception shape [Orchestration Designer]"
  - "Expression shape [Orchestration Designer]"
  - "Decide shape [Orchestration Designer]"
  - "Receive shape [Orchestration Designer]"
  - "Compensate shape [Orchestration Designer]"
  - "orchestrations, shapes"
  - "Suspend shape [Orchestration Designer]"
  - "Send shape [Orchestration Designer]"
  - "Group shape [Orchestration Designer]"
  - "Listen shape [Orchestration Designer]"
  - "shapes, about shapes"
  - "Construct Message shape [Orchestration Designer]"
  - "Parallel Actions shape [Orchestration Designer]"
  - "Call Rules shape [Orchestration Designer]"
  - "Start Orchestration shape [Orchestration Designer]"
  - "Transform shape [Orchestration Designer]"
  - "Message Assignment shape [Orchestration Designer]"
  - "Role Link shape [Orchestration Designer]"
  - "Call Orchestration shape [Orchestration Designer]"
  - "Port shape [Orchestration Designer]"
  - "shapes"
  - "Scope shape [Orchestration Designer]"
  - "Terminate shape [Orchestration Designer]"
  - "Orchestration Designer, shapes"
  - "Insufficient Configuration Smart Tag [Orchestration Designer]"
ms.assetid: a1d03baa-a267-499d-94fc-700b3e959458
caps.latest.revision: 14
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Orchestration Shapes
Orchestration Designer is a visual tool for creating orchestrations. It provides several shapes that you can place on the design surface as visual representations of underlying actions, and they can help you to efficiently design and implement an orchestration.  

 **Insufficient Configuration Action**  

 ![](../core/media/ebiz-orch-insufficconfig.gif "ebiz_orch_insufficconfig")  

> [!NOTE]
>  The Insufficient Configuration Action is displayed in the Orchestration designer when the Orchestration Designer detects that the associated shape is not completely configured. If a shape in an Orchestration is not completely configured then the associated Orchestration will not compile.  

 The following table lists the available shapes, along with a brief description of the function of each shape.  


|                                   Shape                                    |              Shape Name              |                                                                    Purpose                                                                     |
|----------------------------------------------------------------------------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| ![](../core/media/ebiz-orch-callorchestrat.gif "ebiz_orch_callorchestrat") | <strong>Call Orchestration</strong>  |                                    Enables your orchestration to call another orchestration synchronously.                                     |
|     ![](../core/media/ebiz-orch-call-rules.gif "ebiz_orch_call_rules")     |     <strong>Call Rules</strong>      |                             Enables you to configure a Business Rules policy to be executed in your orchestration.                             |
|     ![](../core/media/ebiz-orch-compensate.gif "ebiz_orch_compensate")     |     <strong>Compensate</strong>      |           Enables you to call code to undo or compensate for operations already performed by the orchestration when an error occurs.           |
|   ![](../core/media/ebiz-orch-constructmsg.gif "ebiz_orch_constructmsg")   |  <strong>Construct Message</strong>  |                                                      Enables you to construct a message.                                                       |
|         ![](../core/media/ebiz-orch-decide.gif "ebiz_orch_decide")         |       <strong>Decide</strong>        |                                           Enables you to conditionally branch in your orchestration.                                           |
|          ![](../core/media/ebiz-orch-delay.gif "ebiz_orch_delay")          |        <strong>Delay</strong>        |                                Enables you to build delays in your orchestration based on a time-out interval.                                 |
|         ![](../core/media/ebiz-orch-assign.gif "ebiz_orch_assign")         |     <strong>Expression</strong>      |                                         Enables you to assign values to variables or make .NET calls.                                          |
|          ![](../core/media/ebiz-orch-group.gif "ebiz_orch_group")          |        <strong>Group</strong>        |                     Enables you to group operations into a single collapsible and expandable unit for visual convenience.                      |
|         ![](../core/media/ebiz-orch-listen.gif "ebiz_orch_listen")         |       <strong>Listen</strong>        |            Enables your orchestration to conditionally branch depending on messages received or the expiration of a timeout period.            |
|           ![](../core/media/ebiz-orch-loop.gif "ebiz_orch_loop")           |        <strong>Loop</strong>         |                                          Enables your orchestration to loop until a condition is met.                                          |
|         ![](../core/media/ebiz-orch-assign.gif "ebiz_orch_assign")         | <strong>Message Assignment</strong>  |                                                     Enables you to assign message values.                                                      |
|   ![](../core/media/ebiz-orch-paralactions.gif "ebiz_orch_paralactions")   |  <strong>Parallel Actions</strong>   |                           Enables your orchestration to perform two or more operations independently of each other.                            |
|           ![](../core/media/ebiz-orch-port.gif "ebiz_orch_port")           |        <strong>Port</strong>         |                                                Defines where and how messages are transmitted.                                                 |
|        ![](../core/media/ebiz-orch-receive.gif "ebiz_orch_receive")        |       <strong>Receive</strong>       |                                            Enables you to receive a message in your orchestration.                                             |
|       ![](../core/media/ebiz-orch-rolelink.gif "ebiz_orch_rolelink")       |      <strong>Role Link</strong>      | Enables you to create a collection of ports that communicate with the same logical partner, perhaps through different transports or endpoints. |
|          ![](../core/media/ebiz-orch-scope.gif "ebiz_orch_scope")          |        <strong>Scope</strong>        |                                         Provides a framework for transactions and exception handling.                                          |
|           ![](../core/media/ebiz-orch-send.gif "ebiz_orch_send")           |        <strong>Send</strong>         |                                             Enables you to send a message from your orchestration.                                             |
| ![](../core/media/ebiz-orch-strtorchestrat.gif "ebiz_orch_strtorchestrat") | <strong>Start Orchestration</strong> |                                    Enables your orchestration to call another orchestration asynchronously.                                    |
|        ![](../core/media/ebiz-orch-suspend.gif "ebiz_orch_suspend")        |       <strong>Suspend</strong>       |                   Suspends the operation of your orchestration to enable intervention in the event of some error condition.                    |
|      ![](../core/media/ebiz-orch-terminate.gif "ebiz_orch_terminate")      |      <strong>Terminate</strong>      |                    Enables you to immediately end the operation of your orchestration in the event of some error condition.                    |
|    ![](../core/media/ebiz-orch-throwexcept.gif "ebiz_orch_throwexcept")    |   <strong>Throw Exception</strong>   |                                     Enables you to explicitly throw an exception in the event of an error.                                     |
|      ![](../core/media/ebiz-orch-transform.gif "ebiz_orch_transform")      |      <strong>Transform</strong>      |                                    Enables you to map the fields from existing messages into new messages.                                     |

