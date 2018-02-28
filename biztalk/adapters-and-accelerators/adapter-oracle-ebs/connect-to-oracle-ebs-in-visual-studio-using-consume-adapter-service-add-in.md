---
title: "Connect to Oracle E-Business Suite in Visual Studio using Consume Adapter Service Add-in | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 62d60216-5065-4048-b073-8618b7685e00
caps.latest.revision: 6
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Connect to Oracle E-Business Suite in Visual Studio using Consume Adapter Service Add-in
The [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] is installed when you install [!INCLUDE [afproductnameshort](../../includes/afproductnameshort-md.md)]. The [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] loads all the WCF-Custom bindings installed on the computer. To connect to Oracle E-Business Suite using the WCF-based [!INCLUDE [adapteroraclebusinessshort](../../includes/adapteroraclebusinessshort-md.md)] in a BizTalk project, you must use the <strong>oracleEBSBinding</strong>.  

 This topic provides instructions on how to use the [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)].  

## Connecting to Oracle E-Business Suite Using the Consume Adapter Service Add-in  
 Perform the following steps to connect to Oracle E-Business Suite using the [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)].  

#### To connect to Oracle E-Business Suite  

1. To connect using the [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] in a BizTalk solution:  

   1. Create a BizTalk project using Visual Studio.  

   2. Right-click the project in Solution Explorer, point to **Add**, and then click **Add Generated Items**.  

   3. In the **Add Generated Items** dialog box, do the following:  


      |          Use this           |                   To do this                    |
      |-----------------------------|-------------------------------------------------|
      | <strong>Categories</strong> | Click <strong>Consume Adapter Service</strong>. |
      | <strong>Templates</strong>  | Click <strong>Consume Adapter Service</strong>. |


   4. Click <strong>Add</strong>. The [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] opens.  

2. From the **Select a binding** drop-down list, select **oracleEBSBinding** and click **Configure**.  

3. In the **Configure Adapter** dialog box, click the **Security** tab, and from the **Client credential type** drop-down list box, select **Username** and specify the user name and password to connect to the Oracle E-Business Suite.  


   |                                                Use this                                                |                                                                                                                                                                                      To do this                                                                                                                                                                                       |
   |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                     <strong>To connect using Oracle database credentials</strong>                      |                                                                                       Specify the <strong>ClientCredentialType</strong> binding property to <strong>Database</strong> and specify database credentials for <strong>User name</strong> and <strong>Password</strong> text boxes.                                                                                       |
   |                 <strong>To connect using Oracle E-Business Suite credentials</strong>                  | Specify the <strong>ClientCredentialType</strong> binding property to <strong>EBusiness</strong> and specify Oracle E-Business Suite credentials for <strong>User name</strong> and <strong>Password</strong> text boxes. In this case, you must also specify Oracle database credentials for <strong>OracleUserName</strong> and <strong>OraclePassword</strong> binding properties. |
   | <strong>To connect using Windows Authentication if ClientCredentialType is set to “Database”</strong>  |                                                                                                                                   Specify a “/” for the <strong>User name</strong> text box and leave the <strong>Password</strong> text box blank.                                                                                                                                   |
   | <strong>To connect using Windows Authentication if ClientCredentialType is set to “EBusiness”</strong> |                                                    Specify Oracle E-Business Suite credentials for <strong>User name</strong> and <strong>Password</strong> text boxes. You must also specify a “/” for the <strong>OracleUserName</strong> binding property and leave the <strong>OraclePassword</strong> binding property blank.                                                    |


4. Click the <strong>URI Properties</strong> tab, and specify values for the connection parameters. For more information about the connection URI for the [!INCLUDE [adapteroraclebusinessshort](../../includes/adapteroraclebusinessshort-md.md)], see [Create the Oracle E-Business Suite connection URI](../../adapters-and-accelerators/adapter-oracle-ebs/create-the-oracle-e-business-suite-connection-uri.md).  

   > [!NOTE]
   >  If the connection parameters contain any reserved characters, you must specify them as-is in the **URI Properties** tab, that is, without using any escape characters. However, if you specify the URI directly in the **Configure a URI** field and the connection parameters contain reserved characters, you must specify the connection parameters using proper escape characters.  

5. Click the **Binding Properties** tab, and then specify values for the binding properties, if any, required by the operations you want to target. For more information about binding properties, see [Read about the BizTalk Adapter for Oracle E-Business Suite binding properties](../../adapters-and-accelerators/adapter-oracle-ebs/read-about-the-biztalk-adapter-for-oracle-e-business-suite-binding-properties.md).  

6. Click **OK**.  

7. Click **Connect**. After the connection is established, the connection status is shown as **Connected**.  

    The following figure shows the [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] immediately after the connection is established.  

    ![Consume Adapter Service dialog box](../../adapters-and-accelerators/adapter-oracle-ebs/media/6a2b21ed-0fd2-4874-a6a6-e59a467533f8.gif "6a2b21ed-0fd2-4874-a6a6-e59a467533f8")  

    The [!INCLUDE [consumeadapterservshort](../../includes/consumeadapterservshort-md.md)] displays different nodes containing various operations that can be performed on the Oracle E-Business Suite and the Oracle database. For more information on how the metadata is categorized under the various nodes, see [Connect to Oracle E-Business Suite in Visual Studio using Add Adapter Metadata Wizard](../../adapters-and-accelerators/adapter-oracle-ebs/connect-to-oracle-ebs-in-visual-studio-using-add-adapter-metadata-wizard.md).  

## See Also  
 [Connect to the Oracle E-Business Suite in Visual Studio](../../adapters-and-accelerators/adapter-oracle-ebs/connect-to-the-oracle-e-business-suite-in-visual-studio.md)   
 [Connect to Oracle E-Business Suite using Windows Authentication](../../adapters-and-accelerators/adapter-oracle-ebs/connect-to-oracle-e-business-suite-using-windows-authentication.md)