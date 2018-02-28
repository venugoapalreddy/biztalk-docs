---
title: "Service Bus messaging adapter | Microsoft Docs"
description: Send and receive messages using the Azure SB-Messaging adapter in BizTalk Server
ms.custom: ""
ms.date: "11/21/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c06c4934-45b2-4f6f-9d19-3ebd937c32ae
caps.latest.revision: 5
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---

# SB-Messaging Adapter
The Service Bus (<strong>SB-Messaging</strong>) adapter is used to receive and send from Service Bus entities like Queues, Topics, and Relays. You can use the <strong>SB-Messaging</strong> adapter to connect your on-premises [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] to Azure.

<strong>Starting with <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[bts2016_md](../includes/bts2016-md.md)]: Path(D:/a/1/s/target_repo/biztalk/core/sb-messaging-adapter.md) contains invalid char.
Parameter name: path -->[!INCLUDE[bts2016_md](../includes/bts2016-md.md)]<!--END ERROR INCLUDE --> Feature Pack 2</strong>, Service Bus Premium is supported. When configuring a send port using this adapter, you can send messages to partitioned queues and topics. 

## Authenticating with Service Bus
Service Bus provides two methods to authenticate: 

- Access Control Service (ACS) 
- Shared Access Signature (SAS)

We recommend using Shared Access Signature (SAS) to authenticate with Service Bus. The Shared Access Key value is listed in the [Azure portal](https://portal.azure.com).

When you create a Service Bus namespace, the Access Control (ACS) namespace is not automatically created. To use Access Control, you need the Issuer Name and Issuer Key values of this namespace. These values are available when you create a new ACS namespace using Windows PowerShell. These values are not listed in the Azure portal.

To use ACS for authentication, and get the Issuer Name and Issuer Key values, the overall steps include:

1. Install the [Azure Powershell cmdlets](https://azure.microsoft.com/documentation/articles/powershell-install-configure/).
2. Add your Azure account: `Add-AzureAccount`
3. Return your subscription name: `get-azuresubscription`
4. Select your subscription: `select-azuresubscription <name of your subscription>` 
5. Create a new namespace: `new-azuresbnamespace <name for the service bus> "Location" -CreateACSNamespace $true -NamespaceType Messaging`

    Example:
      `new-azuresbnamespace biztalksbnamespace "South Central US" -CreateACSNamespace $true -NamespaceType Messaging`

5. When the new ACS namespace is created (which can take several minutes), the IssuerName and IssuerKey values are listed in the connection string: 

    ```
    Name                  : biztalksbnamespace
    Region                : South Central US
    DefaultKey            : abcdefghijklmnopqrstuvwxyz
    Status                : Active
    CreatedAt             : 10/18/2016 9:36:30 PM
    AcsManagementEndpoint : https://biztalksbnamespace-sb.accesscontrol.windows.net/
    ServiceBusEndpoint    : https://biztalksbnamespace.servicebus.windows.net/
    ConnectionString      : Endpoint=sb://biztalksbnamespace.servicebus.windows.net/;SharedSecretIssuer=owner;SharedSecretValue=abcdefghijklmnopqrstuvwxyz
    NamespaceType         : Messaging
    ```

See [New-AzureSBNamespace](https://docs.microsoft.com/powershell/module/Azure/New-AzureSBNamespace) for guidance.

## Receive messages from Service Bus

1. In the BizTalk Server Administration console, expand **BizTalk Group**, expand **Applications**, and then expand your application. 

2. Right-click **Receive Ports**, select **New**, and select **One-Way receive port**. 

3. Give it a name, and select **Receive Locations**. 

4. Select **New**, give it a **Name**. In the **Transport** section, select **SB-Messaging** from the **Type** drop-down list, and then select **Configure**.  

5. Configure the **General** properties:  


   |                  Use this                  |                                                                                                                                                                                                                                                                                                                                                     To do this                                                                                                                                                                                                                                                                                                                                                     |
   |--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <strong>Queue or Subscription URL</strong> |                                                                                                                                                                                                                                                                     Specify the URL where the Service Bus queue is deployed. Typically the URL is in the following format:<br /><br /> `sb://<namespace>.servicebus.windows.net/<queue_name>`                                                                                                                                                                                                                                                                      |
   |       <strong>Open Timeout</strong>        |                                                                                                                                                                                                                                                                                 Specifies a time span value that indicates the time for a channel open operation to complete.<br /><br /> <strong>Default value:</strong> 1 minute                                                                                                                                                                                                                                                                                 |
   |       <strong>Close Timeout</strong>       |                                                                                                                                                                                                                                                                                Specifies a time span value that indicates the time for a channel close operation to complete.<br /><br /> <strong>Default value:</strong> 1 minute                                                                                                                                                                                                                                                                                 |
   |      <strong>Receive timeout</strong>      |                                                                                                                                                                                                                                                                                  Specifies a time span value that indicates the time for a receive operation to complete.<br /><br /> <strong>Default value:</strong> 10 minutes                                                                                                                                                                                                                                                                                   |
   |      <strong>Prefetch count</strong>       | Specifies the number of messages that are received simultaneously from the Service Bus Queue or a topic. Prefetching enables the queue or subscription client to load additional messages from the service when it performs a receive operation. The client stores these messages in a local cache. The size of the cache is determined by the value for the Prefetch Count property you specify here.<br /><br /> For more information, refer to the section “Prefetching” at [https://azure.microsoft.com/documentation/articles/service-bus-performance-improvements/](https://azure.microsoft.com/documentation/articles/service-bus-performance-improvements/)<br /><br /> <strong>Default value:</strong> -1 |
   |        <strong>Use Session</strong>        |                                                                                                                                                                                                                                                                                                       Select this check box to use a Service Bus session to receive messages from a queue or a subscription.                                                                                                                                                                                                                                                                                                       |


6. Configure the **Authentication** properties:  


   |                                                      Use this                                                       |                                                                                                                                                                                             To do this                                                                                                                                                                                             |
   |---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                                       <strong>Access Control Service</strong>                                       | Select this to use ACS for authentication and provide the following values:<br /><br /> - Enter the Service Bus Access Control Service STS URI. Typically the URI is in the following format:<br /><br /> `https://<namespace>-sb.accesscontrol.windows.net/`<br /><br /> - Enter the issuer name for the Service Bus namespace.<br /><br /> - Enter the issuer key for the Service Bus namespace. |
   | <strong>Shared Access Signature</strong> (new starting with [!INCLUDE [bts2013r2_md](../includes/bts2013r2-md.md)]) |                                                                                                                                          Select this to use Shared Access Signature (SAS) for authentication, and provide the SAS key name and key value.                                                                                                                                          |


7. In the <strong>Properties</strong> tab, in the <strong>Namespace for Brokered Message Properties</strong>, enter the namespace that the adapter uses to write the brokered message properties as message context properties on the message received by [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]. If you want to promote the brokered message properties, select the <strong>Promote Brokered Message Properties</strong> check box.  

8. Select **OK**.  

9. Select your **Receive handler**, and the **Receive pipeline**. Select **OK** to save your changes. [Create a Receive Location](../core/how-to-create-a-receive-location.md) provides some guidance.  

## Send messages to Service Bus

1. In the BizTalk Server Administration console, right-click **Send Ports**, select **New**, and select **Static One-way send port**.

   [Create a Send Port](../core/how-to-create-a-send-port2.md) provides some guidance.

2. Enter a **Name**. In **Transport**, set the **Type** to **SB-Messaging**, and select **Configure**. 

3. Configure the **General** properties:  


   |               Use this                |                                                                                                                                                                                                                                                    To do this                                                                                                                                                                                                                                                    |
   |---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |   <strong>Destination URL</strong>    |                                                                                                                                                                     Enter the URL where the Service Bus queue is deployed. Typically the URL is in the following format:<br /><br /> `sb://<namespace>.servicebus.windows.net/<queue_name>`                                                                                                                                                                      |
   | <strong>Batch Flush Interval</strong> | Specifies a time span value that indicates the interval when the message batches being sent to a Queue or a Topic are flushed. The default value is 20 milliseconds.<br /><br /> For more information about batching with respect to Service Bus Queues and Topics, see the <strong>Client-side batching</strong> section at [https://azure.microsoft.com/documentation/articles/service-bus-performance-improvements](https://azure.microsoft.com/documentation/articles/service-bus-performance-improvements). |
   |     <strong>Open Timeout</strong>     |                                                                                                                                                                                Specifies a time span value that indicates the time for a channel open operation to complete.<br /><br /> <strong>Default value:</strong> 1 minute                                                                                                                                                                                |
   |     <strong>Send Timeout</strong>     |                                                                                                                                                                                    Specifies a time span value that indicates the time for a send operation to complete.<br /><br /> <strong>Default value:</strong> 1 minute                                                                                                                                                                                    |
   |    <strong>Close Timeout</strong>     |                                                                                                                                                                               Specifies a time span value that indicates the time for a channel close operation to complete.<br /><br /> <strong>Default value:</strong> 1 minute                                                                                                                                                                                |


4. Configure the **Authentication** properties: 


   |                                                      Use this                                                       |                                                                                                                                                                                             To do this                                                                                                                                                                                             |
   |---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                                       <strong>Access Control Service</strong>                                       | Select this to use ACS for authentication and provide the following values:<br /><br /> - Enter the Service Bus Access Control Service STS URI. Typically the URI is in the following format:<br /><br /> `https://<namespace>-sb.accesscontrol.windows.net/`<br /><br /> - Enter the issuer name for the Service Bus namespace.<br /><br /> - Enter the issuer key for the Service Bus namespace. |
   | <strong>Shared Access Signature</strong> (new starting with [!INCLUDE [bts2013r2_md](../includes/bts2013r2-md.md)]) |                                                                                                                                          Select this to use Shared Access Signature (SAS) for authentication, and provide the SAS key name and key value.                                                                                                                                          |


5. In the **Properties** tab, enter the **Namespace for the user defined Brokered Message Properties** that contains the BizTalk message context properties that you want to write on the outgoing message to Service Bus. All the namespace properties are written to the message as user-defined Brokered Message properties. The adapter ignores the namespace while writing the properties as Brokered Message properties. It uses the namespace only to ascertain what properties to write.  

    You can also enter the values for the BrokeredMessage properties. These properties are described at [BrokeredMessage Properties](https://docs.microsoft.com/dotnet/api/microsoft.servicebus.messaging.brokeredmessage), including the **Partition Key**.

6. Select **OK** to save your changes.  

## See also
[Using adapters](../core/using-adapters.md)