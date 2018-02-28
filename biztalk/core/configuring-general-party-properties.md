---
title: "Configuring General Party Properties | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bbabf7e5-6388-4900-ad47-cf5d5af396b5
caps.latest.revision: 20
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Configuring General Party Properties
A party or trading partner represents a participating organization in a business relationship. Party properties contain the following information:  

- General information such as party name  

- Send ports associated with the party  

- Certificates associated with the party  

  For more information about parties or trading partners, see [Trading Partners](../core/trading-partners-and-business-profiles.md).  

## Prerequisites  
 You must be logged on as a member of the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administrators or [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] B2B Operators group.  

### To configure party properties  

1. In the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration Console, right-click <strong>Parties</strong>, point to <strong>New</strong>, and then click <strong>Party</strong>.  

2. On the **General** page of the **Party Properties** dialog box, do the following:  


   |                                                       Use this                                                       |                                                                                                                                                                                                                                                                                    To do this                                                                                                                                                                                                                                                                                     |
   |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                                                <strong>Name</strong>                                                 |                                                                                                                                                                                                                                                                                Enter a party name.                                                                                                                                                                                                                                                                                |
   | <strong>Local BizTalk processes messages received by the party or supports sending messages from this party</strong> | Select this checkbox to specify that the party represents the same trading partner that also hosts [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]. <strong>Important:</strong>  For a two-party TPM solution that uses out-of-the-box pipelines shipped with [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)], you must select this check box for at least one party. <strong>Note:</strong>  If you clear this check box, some properties will be disabled while creating the agreements for this party. |
   |                                <strong>Additional Properties – Name / Value</strong>                                 |                                                                                                                                                        Enter a name-value pair to store any information about the party. You can add as many name-value pairs as you want. <strong>Note:</strong>  The name-value pairs are not used by the BizTalk Server for any processing; this data is for information purposes only.                                                                                                                                                        |
   |                                               <strong>Delete</strong>                                                |                                                                                                                                                                                                                                                                   Click to delete the selected name-value pair.                                                                                                                                                                                                                                                                   |


3. On the **Send Ports** page of the **Party Properties** dialog box, do the following.  

   > [!NOTE]
   >  In BizTalk Server, the send port association is done at the agreement level. The **Send Ports** page available as part of the party properties is purely for backward compatibility. Whenever you associate a send port with an agreement, the send port setting is also propagated to the party setting and you can see the send port association in this page as well. However, the reverse is not true. You cannot associate a send port with a party and then have that send port be automatically available as part of the agreement settings. For more information on how to associate send ports with agreement, see [Configuring Send Port Association (X12)](../core/configuring-send-port-association-x12.md) or [Configuring Send Port Association (EDIFACT)](../core/configuring-send-port-association-edifact.md).  

   |              Use this              |                                            To do this                                             |
   |------------------------------------|---------------------------------------------------------------------------------------------------|
   | <strong>Send ports - Name</strong> |                From the drop-down list, select a send port to bind to this party.                 |
   | <strong>Send ports - URI</strong>  |                                  Displays the send port address.                                  |
   |      <strong>Remove</strong>       |                      Click to remove the selected send port from the party.                       |
   |    <strong>Properties</strong>     | Click to display the <strong>Send Port Properties</strong> dialog box for the selected send port. |


4. On the **Certificate** page, do the following:  


   |              Use this               |                                                                                                                                                 To do this                                                                                                                                                 |
   |-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |       <strong>Browse</strong>       |                                          Click to display the <strong>Select Certificate</strong> dialog box, where you select the signature certificate from the Local Machine or Other People certificate store to apply to messages transmitted to the party.                                           |
   |    <strong>Common Name</strong>     |                                                                                                                            Displays a description of the selected certificate.                                                                                                                             |
   |     <strong>Thumbprint</strong>     | Displays the thumbprint of the private key certificate that is used for party resolution and signature verification. The certificate thumbprint has the format HHHH HHHH HHHH HHHH HHHH HHHH HHHH HHHH HHHH HHHH, where H is a hexadecimal digit (a number from 0 through 9 or a letter from A through F). |
   | <strong>Remove certificate</strong> |                                                                                                                                 Click to remove the displayed certificate.                                                                                                                                 |


5. Click **Apply** to accept the properties, or click **OK** to complete the configuration setting. Either action will validate the settings.  

## See Also  
 [Configuring EDI Properties](../core/configuring-edi-properties.md)