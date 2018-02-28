---
title: "How to Configure a SOAP Send Port | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "SOAP adapters, send ports"
  - "SOAP adapters, code samples"
  - "code samples, SOAP adapters"
  - "configuring [SOAP adapters], code samples"
  - "configuring [SOAP adapters], send ports"
  - "send ports, SOAP adapters"
ms.assetid: 3a0622f4-d25d-4449-a063-d8ba217e9729
caps.latest.revision: 11
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# How to Configure a SOAP Send Port
You can configure a SOAP send port either programmatically or by using the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console.  

 **How to Configure a SOAP Send Port Programmatically**  

 The BizTalk Explorer object model exposes an adapter-specific interface for send ports named **ITransportInfo** that has the **TransportTypeData** read/write property. This property accepts a SOAP send port configuration property bag in the form of a name-value pair of XML strings. Note that to set this property in the BizTalk Explorer object model you must set the **OutboundTransportLocation** property of the **ITransportInfo** interface first.  

 The **TransportTypeData** property of the **ITransportInfo** interface is not required. If it is not set, the adapter uses the default values for the SOAP send port configuration, as indicated in the following table.  

 The following table lists the configuration properties you can set in the BizTalk Explorer object model for SOAP send ports.  

|Property name|Type|Description|  
|-------------------|----------|-----------------|  
|**URI**|String|Virtual directory containing the Web service on the deployment server.|  
|**Username**|String|User name to specify for accessing the target Web service.<br /><br /> Default value: Blank|  
|**Password**|String|User password to use for authentication with the server.<br /><br /> Default value: Blank|  
|**ClientCertificate**|String|Thumbprint of client SSL certificate.<br /><br /> Default value: Blank|  
|**AffiliateApplicationName**|String|The name of the SSO application to use to redeem the ticket for client credentials.<br /><br /> The **AffiliateApplicationName** is mutually exclusive to a **Username** and **Password** pair.<br /><br /> Default value: Blank|  
|**UseProxy**|Boolean|Indicates whether the SOAP send port uses a proxy server to access the target Web service. The proxy server can be shared by all SOAP send ports.<br /><br /> Default value: False|  
|**ProxyAddress**|String|Address of the HTTP proxy to use for the Web service call.<br /><br /> Default value: Blank|  
|**ProxyPort**|Integer|Port of the HTTP proxy to use for the Web service call.<br /><br /> Default value: Blank|  
|**ProxyUsername**|String|User name to use for the proxy.<br /><br /> Default value: Blank|  
|**ProxyPassword**|String|Password to use for the proxy.<br /><br /> Default value: Blank|  

 The following code shows the format to use to set these properties:  

```  
<CustomProps>  
   <URI vt="8"/>  
   <ClientCertificate vt="8"/>  
   <Password vt="8">Encrypted</Password>  
   <ProxyAddress vt="8"/>  
   <ProxyPassword vt="8">Encrypted</ProxyPassword>  
   <ProxyPort vt="3"/>  
   <ProxyUsername vt="8"/>  
   <UseProxy vt="11"/>  
   <Username vt="8"/>  
   <AffiliateApplicationName vt="8"/>  
</CustomProps>  
```  

 **How to Configure a SOAP Send Port with the BizTalk Server Administration Console**  

 You can set SOAP send port adapter variables in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console. If properties are not set for the send port, the default send handler values set in the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console are used.  

### To configure variables for a SOAP send port  

1. In the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console, create a new send port or double-click an existing send port to modify it. For more information, see [How to Create a Send Port](../core/how-to-create-a-send-port2.md). Configure all of the send port options and specify <strong>SOAP</strong> for the <strong>Type</strong> option in the <strong>Transport</strong> section of the <strong>General</strong> tab.  

2. On the **General** tab, in the **Transport** section next to **Type**, click **Configure**.  

3. In the **SOAP Transport Properties** dialog box, on the **General** tab, do the following:  


   |                    Use this                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          To do this                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
   |------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |        <strong>Web Service URL</strong>        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  Specify the address of the Web service you want to call. <strong>Note:</strong>  The URI for a send port or receive location cannot exceed 256 characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
   |        <strong>Authentication</strong>         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     Indicate the authentication method used by the Web service you are calling.<br /><br /> Options:<br /><br /> -   <strong>Anonymous .</strong> The default setting.<br />-   <strong>Basic .</strong> The SOAP connection sends the user name and password in plain text.<br />-   <strong>Digest .</strong> The SOAP connection sends the password in an encrypted format.<br />-   <strong>NTLM .</strong> Neither the user name nor the password is sent over a SOAP connection. The SOAP adapter always uses the credentials of the process under which the SOAP send adapter runs for this authentication type.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
   |          <strong>Credentials</strong>          | Specify the type of credentials to use.<br /><br /> Only available if the <strong>Authentication type</strong> is <strong>Basic</strong> or <strong>Digest</strong>.<br /><br /> Options:<br /><br /> -   <strong>Do Not Use Single Sign-On</strong><br />     <strong>User name</strong><br />     The user name to use for authentication with the destination server. If the <strong>Authentication type</strong> property is <strong>Anonymous</strong> or <strong>NTLM</strong>, this option is disabled. This property requires a value if <strong>Basic</strong> or <strong>Digest</strong> is selected, and Enterprise Single Sign-On is not used.<br />     Minimum length: 0<br />     Maximum length: 256<br />     <strong>Password</strong><br />     The password to use for authentication with the destination server. If the <strong>Authentication type</strong> property is <strong>Anonymous</strong> or <strong>NTLM</strong>, this option is disabled. This property requires a value if <strong>Basic</strong> or <strong>Digest</strong> is selected, and Single Sign-On is not used.<br />     Minimum length: 0<br />     Maximum length: 256<br />-   <strong>Use Single Sign-On</strong><br />     Specify whether to use Single Sign-On to retrieve client credentials for authentication with the destination server.<br />     <strong>Affiliate Application</strong><br />     Specifies the affiliate application to use for Single Sign-On. For information about populating this list, see [SSO Affiliate Applications](../core/sso-affiliate-applications.md).<br />     Minimum length: 0<br />     Maximum length: 256 |
   | <strong>Client Certificate Thumbprint</strong> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Specify the thumbprint of the client certificate to use for establishing a connection.<br /><br /> Example: 01 23 45 67 89 AB CD EF 01 23 45 67 89 AB CD EF 01 23 45 67<br /><br /> Minimum length: 0<br /><br /> Maximum length: 59                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |


4. In the **SOAP Transport Properties** dialog box, on the **Proxy** tab, do the following:  


   |                          Use this                          |                                                                                                                                                                                                                         To do this                                                                                                                                                                                                                         |
   |------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Use Handler's default proxy configuration</strong> |                                                                                            Specify the send port proxy handler configuration. When true, the port will use the proxy settings specified at the handler level. When false, the send adapter will use the proxy information specified on the send port.<br /><br /> The default setting is true.                                                                                             |
   |             <strong>Do not use proxy</strong>              |                                                                                                                                                                                                Indicate whether the SOAP send handler uses a proxy server.                                                                                                                                                                                                 |
   |                 <strong>Use proxy</strong>                 |                                                                                                                                                                     Indicate whether the SOAP send handler uses a proxy server. The proxy server can be shared by all SOAP send ports.                                                                                                                                                                     |
   |                  <strong>Server</strong>                   |                                                                                                                 Specifies the name of the proxy server.<br /><br /> This property only requires a value if <strong>Use proxy</strong> is selected.<br /><br /> Type: String<br /><br /> Minimum length: 0<br /><br /> Maximum length: 256                                                                                                                  |
   |                   <strong>Port</strong>                    |                                              Specify the port the SOAP send handler uses.<br /><br /> This property only requires a value if <strong>Use proxy</strong> is selected.<br /><br /> Default Value: 80<br /><br /> Type: Long<br /><br /> Minimum value: 0<br /><br /> Maximum value: 65535 <strong>Note:</strong>  Specifying a value of 0 indicates to use the default value, which is port 80.                                              |
   |                 <strong>User name</strong>                 | Specify the user name to use for authentication. If you use Windows integrated authentication, the user name includes the domain, <strong>domain\username</strong>. If you use Basic or Digest authentication, the user name does not include <strong>domain\\</strong>.<br /><br /> This property only requires a value if <strong>Use proxy</strong> is selected.<br /><br /> Type: String<br /><br /> Minimum length: 0<br /><br /> Maximum length: 256 |
   |                 <strong>Password</strong>                  |                                                                                                             Specify the password to use for authentication.<br /><br /> This property only requires a value if <strong>Use proxy</strong> is selected.<br /><br /> Type: String<br /><br /> Minimum length: 0<br /><br /> Maximum length: 256                                                                                                              |


5. In the **SOAP Transport Properties** dialog box, on the **Web Service** tab, do the following:  


   |                Use this                 |                                                                                                                                                                                                         To do this                                                                                                                                                                                                         |
   |-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Orchestration Web Port</strong> |                                                                                                                                 Specify to use the Web service that is exposed at the Web Service URL listed on the <strong>General</strong> tab.<br /><br /> This is the default setting.                                                                                                                                 |
   |     <strong>Assembly name</strong>      | Specify the name of the assembly containing the Web service proxy. This field can be populated by clicking the browse button to find an assembly. After selecting the assembly this box is populated with the fully qualified name of the assembly. <strong>Note:</strong>  The specified assembly must be present on all [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]s at runtime. |
   |       <strong>Type name</strong>        |                                                                                                                                     Specify the name of the class that contains the Web method to be invoked. This can be selected from a list of types contained within the assembly.                                                                                                                                     |
   |      <strong>Method name</strong>       |                                              Specify one of the methods in the list box or choose the option to "Specify later". If the option to "Specify later" is chosen, the Web method must be set by some other means, such as a pipeline component. In this scenario, the web method must be written to the Soap Adapter <strong>MethodName</strong> context property.                                              |
   |        <strong>SOAP 1.2</strong>        |                                                                                                                Specify to generate proxy code that will support the SOAP 1.2 protocol. If this option is left cleared, SOAP 1.1-compliant proxy code will be generated.<br /><br /> Default value: cleared                                                                                                                 |


6. Click **OK** and **OK** again to save settings.  

## See Also  
 [Publishing Web Services](../core/publishing-web-services.md)