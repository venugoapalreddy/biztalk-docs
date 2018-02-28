---
title: "How to Configure an HTTP Send Handler | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "send handlers, HTTP adapters"
  - "configuring [HTTP adapters], send handlers"
  - "HTTP adapters, send handlers"
ms.assetid: 821bf30c-b220-4ded-953d-7e745c0698b9
caps.latest.revision: 16
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Configure an HTTP Send Handler
Use the following procedure to change the host with which the HTTP send handler is associated.  

> [!NOTE]
>  Each host can have only one send handler associated with it.  
> 
> [!CAUTION]
>  When using HTTP or SOAP adapter handlers, it is recommended that you install the host instances for these handlers on Microsoft [!INCLUDE [btsWinSvr2k8](../includes/btswinsvr2k8-md.md)], [!INCLUDE [btsWinSvr2k8R2](../includes/btswinsvr2k8r2-md.md)] computers.  

### To change global variables for an HTTP send handler  

1. In the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console, expand [!INCLUDE [btsBizTalkServer2006r3ui](../includes/btsbiztalkserver2006r3ui-md.md)] <strong>Administration</strong>, expand <strong>BizTalk Group</strong>, expand <strong>Platform Settings</strong>, and then expand <strong>Adapters</strong>.  

2. In the expanded adapter list, click **HTTP**, in the right pane right-click the send handler that you want to configure, and then click **Properties**.  

3. In the **Adapter Handler Properties** dialog box, on the **General** tab, in the **Host Name** list, select the host with which the send handler will be associated.  

4. On the **Properties** tab, do the following.  


   |                Use this                |                                                                                                                                                                                                                           To do this                                                                                                                                                                                                                            |
   |----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Request timeout (sec)</strong> | Specify the time-out in seconds when waiting for a response from the server.<br /><br /> If set to zero (0), the HTTP adapter calculates the time-out based on the request message size.<br /><br /> If you do not provide a value, the value for the handler is used.<br /><br /> <strong>Default value:</strong> 0<br /><br /> <strong>Type:</strong> Long<br /><br /> <strong>Minimum value:</strong> 0<br /><br /> <strong>Maximum value:</strong> MAX_LONG |
   |   <strong>Maximum redirects</strong>   |                                                                                                       Specify the maximum redirects allowed for the message being sent.<br /><br /> <strong>Default value:</strong> 5<br /><br /> <strong>Type:</strong> Int<br /><br /> <strong>Minimum value:</strong> 0<br /><br /> <strong>Maximum value:</strong> 10                                                                                                       |
   |     <strong>Content type</strong>      |                                                                 Specify the content type of the request messages.<br /><br /> If you do not provide a value, the value for the handler is used.<br /><br /> <strong>Default value:</strong> Text/XML<br /><br /> <strong>Type:</strong> String<br /><br /> <strong>Minimum length:</strong> 0<br /><br /> <strong>Maximum length:</strong> 256                                                                  |


5. On the **Proxy** tab, do the following.  


   |          Use this          |                                                                                                                                                                 To do this                                                                                                                                                                  |
   |----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Use proxy</strong> |                                                                                          Specify whether the HTTP send handler uses the proxy server.<br /><br /> <strong>Default value:</strong> False<br /><br /> <strong>Type:</strong> Boolean                                                                                          |
   |  <strong>Server</strong>   |                      Specify the proxy server address for this send port.<br /><br /> This property requires a value if <strong>Use proxy</strong> is <strong>True</strong>.<br /><br /> <strong>Type:</strong> String<br /><br /> <strong>Minimum length:</strong> 0<br /><br /> <strong>Maximum length:</strong> 256                      |
   |   <strong>Port</strong>    | Specify the proxy server port for this send port.<br /><br /> This property requires a value if <strong>Use proxy</strong> is <strong>True</strong>.<br /><br /> <strong>Default Value:</strong> 80<br /><br /> <strong>Type:</strong> Long<br /><br /> <strong>Minimum value:</strong> 0<br /><br /> <strong>Maximum value:</strong> 65535 |
   | <strong>User name</strong> |             Specify the user name to use for authentication with the proxy server.<br /><br /> This property requires a value if <strong>Use proxy</strong> is <strong>True</strong>.<br /><br /> <strong>Type:</strong> String<br /><br /> <strong>Minimum length:</strong> 0<br /><br /> <strong>Maximum length:</strong> 256             |
   | <strong>Password</strong>  |              Specify the user password for authentication with the proxy server.<br /><br /> This property requires a value if <strong>Use proxy</strong> is <strong>True</strong>.<br /><br /> <strong>Type:</strong> String<br /><br /> <strong>Minimum length:</strong> 0<br /><br /> <strong>Maximum length:</strong> 256               |


6. Click **OK**.  

## See Also  
 [Configuring the HTTP Adapter](../core/configuring-the-http-adapter.md)