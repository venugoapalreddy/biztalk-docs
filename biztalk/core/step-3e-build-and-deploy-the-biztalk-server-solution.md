---
title: "Step 3e: Build and Deploy the BizTalk Server Solution | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bbfc382b-ed4a-4401-9343-be1bffd747c9
caps.latest.revision: 2
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Step 3e: Build and Deploy the BizTalk Server Solution
In this topic, we’ll deploy the two [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] projects (<strong>BtsSalesforceIntegration</strong> and <strong>CustomPipeline</strong>) that we created in the earlier steps.  
  
### To build and deploy the BizTalk Server projects  
  
1. In the Solution Explorer, right-click the <strong>BtsSalesforceIntegration</strong>[!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] project, and then click <strong>Properties</strong>.  
  
2. In the **Deployment** tab, for **Application Name**, enter **SalesforceIntegration**. Click **Save**.  
  
3. Similarly, right-click the <strong>CustomPipeline</strong>[!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] project, click <strong>Properties</strong>, and in the <strong>Deployment</strong> tab, for the <strong>Application Name</strong> property, enter <strong>SalesforceIntegration</strong> again. Click <strong>Save</strong>. This ensures that the custom pipeline component is deployed to the same application as the <strong>BtsSalesforceIntegration</strong> project.  
  
4. Right-click the solution name in the Solution Explorer, and click **Properties**. In the Solution Property Pages dialog box, click **Configuration Properties**, and verify that the **Build** and **Deploy** check boxes are selected both for **BtsSalesforceIntegration** and **CustomPipeline** projects.  
  
5. Right-click the solution name in the Solution Explorer and then click <strong>Build Solution</strong>. After the solution builds successfully, right-click the solution name again, and then click <strong>Deploy Solution</strong>. The solution is deployed to the [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] Administration console.  
  
## See Also  
 [Step 3: Create the BizTalk Server Solution in Visual Studio](../core/step-3-create-the-biztalk-server-solution-in-visual-studio.md)