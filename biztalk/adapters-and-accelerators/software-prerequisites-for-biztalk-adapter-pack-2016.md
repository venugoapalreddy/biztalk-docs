---
title: "Software prerequisites for BizTalk Adapter Pack 2016 | Microsoft Docs"
ms.custom: ""
ms.date: "06/08/2017"
ms.prod: "biztalk-server"
ms.reviewer: ""

ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 65a063ca-37ae-420b-9d48-e6730caf17e3
caps.latest.revision: 4
author: "MandiOhlinger"
ms.author: "mandia"
manager: "anneta"
---
# Software prerequisites for BizTalk Adapter Pack 2016
Lists the software requirements for the Microsoft [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)] (BAP) included with [!INCLUDE [bts2016_md](../includes/bts2016-md.md)].

The [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)] can be consumed from:  

- A .NET application  

- Microsoft [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]  

- An ADO interface  

- A Microsoft SharePoint portal  

  Based on how you use the adapters, the required software varies.  

## Prerequisites when using a .NET application  
When using a .NET application to consume the adapters, the following software is required on your development computer (the computer where you're creating the .NET application). Install the software in the order listed.


|                                                          BizTalk Adapter Pack 2016                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------|
|                <ul><li>Windows Server 2016</li><li>Windows Server 2012 R2</li><li>Windows 10</li><li>Windows 8.1  </li></ul>                |
|                                                        .NET Framework 4.6.<em>x</em>                                                        |
|                                                             Visual Studio 2015                                                              |
|                                    [!INCLUDE [afproductnameshort](../includes/afproductnameshort-md.md)]                                    |
| The enterprise application clients and associated software. See <strong>Supported enterprise application versions</strong> (in this topic). |

## Prerequisites when using BizTalk Server  
When using a [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)] to consume the adapters, the following software is required on your [!INCLUDE [btsBizTalkServerNoVersion](../includes/btsbiztalkservernoversion-md.md)]. Install the software in the order listed.


|                                                                                                                                                                                                                                                                    BizTalk Adapter Pack 2016                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                                                                                                                                                                                          <ul><li>Windows Server 2016</li><li>Windows Server 2012 R2</li><li>Windows 10</li><li>Windows 8.1  </li></ul>                                                                                                                                                                                                                           |
|                                                                                                                                                                                                                                                                  .NET Framework 4.6.<em>x</em>                                                                                                                                                                                                                                                                   |
|                                                                                                                                                                                                                                                                        Visual Studio 2015                                                                                                                                                                                                                                                                        |
| [!INCLUDE [afproductnameshort](../includes/afproductnameshort-md.md)]<br /><br /> Install the [!INCLUDE [consumeadapterservlong](../includes/consumeadapterservlong-md.md)] for [!INCLUDE [btsVStudioNoVersion](../includes/btsvstudionoversion-md.md)] included with the [!INCLUDE [afproductnameshort](../includes/afproductnameshort-md.md)]. To install, do a <strong>Custom</strong> (select <strong>BizTalk Server Addin</strong>) or <strong>Complete</strong> installation of the [!INCLUDE [afproductnameshort](../includes/afproductnameshort-md.md)]. |
|                                                                                                                                                                                                                                                        [!INCLUDE [bts2016_md](../includes/bts2016-md.md)]                                                                                                                                                                                                                                                        |
|                                                                                                                                                                                                           The enterprise application clients and associated software. See <strong>Supported enterprise application versions</strong> (in this topic).                                                                                                                                                                                                            |

## Prerequisites when using ADO  
 The <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adaptersap](../includes/adaptersap-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adaptersap](../includes/adaptersap-md.md)]<!--END ERROR INCLUDE --></strong> and <strong><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adaptersiebel](../includes/adaptersiebel-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adaptersiebel](../includes/adaptersiebel-md.md)]<!--END ERROR INCLUDE --></strong> include an ADO layer (<em><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adoprovidersapshort](../includes/adoprovidersapshort-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adoprovidersapshort](../includes/adoprovidersapshort-md.md)]<!--END ERROR INCLUDE --></em> and <em><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adoprovidersiebelshort](../includes/adoprovidersiebelshort-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adoprovidersiebelshort](../includes/adoprovidersiebelshort-md.md)]<!--END ERROR INCLUDE --></em>) that can be used to write an ADO.NET client to connect to an SAP system or Siebel system. You can also use the ADO layer with SQL Server Integration Services (SSIS) to import and export data from the LOB application, and SQL Server Reporting Services (SSRS) to generate reports to present data from the LOB systems.  

> [!NOTE]
>  Using the ADO Provider with SSRS is supported only for the [!INCLUDE [adoprovidersapshort](../includes/adoprovidersapshort-md.md)].  

The following software is required on the computer that uses the [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)] with an ADO interface. Install the software in the order listed.  


|                                                          BizTalk Adapter Pack 2016                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------|
|                <ul><li>Windows Server 2016</li><li>Windows Server 2012 R2</li><li>Windows 10</li><li>Windows 8.1  </li></ul>                |
|                                                        .NET Framework 4.6.<em>x</em>                                                        |
|                                                             Visual Studio 2015                                                              |
|                                    [!INCLUDE [afproductnameshort](../includes/afproductnameshort-md.md)]                                    |
|                              <ul><li>Microsoft SQL Server 2016</li><li>Microsoft SQL Server 2014 SP1</li></ul>                              |
| The enterprise application clients and associated software. See <strong>Supported enterprise application versions</strong> (in this topic). |

## Prerequisites when using SharePoint  
The goal of using the adapters with Microsoft SharePoint is to show data from an LOB application on a SharePoint portal.  

A typical setup with the [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)] and SharePoint can use a single computer or use different computers for different tasks. The following table lists the software prerequisites for each computer. If you are using a single computer, all the software must be installed on that computer. Install the software in the order listed.  


|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               Computer where you run the WCF Adapter Service Development Wizard                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Computer where you host the WCF service                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Computer where you can use the SharePoint Designer to define your External Content Types |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <ul><li>Windows Server 2016</li><li>Windows Server 2012 R2</li><li>Windows 10</li><li>Windows 8.1</li><br/><br/><li>.NET Framework 4.6.<em>x</em></li><br/><br/><li>Visual Studio 2015</li><br/><br/><li><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[afproductnameshort](../includes/afproductnameshort-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[afproductnameshort](../includes/afproductnameshort-md.md)]<!--END ERROR INCLUDE --></li><br/><br/><li>Microsoft <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adapterpacknoversion](../includes/adapterpacknoversion-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adapterpacknoversion](../includes/adapterpacknoversion-md.md)]<!--END ERROR INCLUDE --></li><br/><br/><li>The enterprise application clients and associated software. See <strong>Supported enterprise application versions</strong> (in this topic).</li></ul> | <ul><li>Windows Server 2016</li><li>Windows Server 2012 R2</li><li>Windows 10</li><li>Windows 8.1</li><br/><br/><li>.NET Framework 4.6.<em>x</em></li><br/><br/><li>Visual Studio 2015</li><br/><br/><li><!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[afproductnameshort](../includes/afproductnameshort-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[afproductnameshort](../includes/afproductnameshort-md.md)]<!--END ERROR INCLUDE --></li><br/><br/><li>Microsoft <!-- BEGIN ERROR INCLUDE: Unable to resolve [!INCLUDE[adapterpacknoversion](../includes/adapterpacknoversion-md.md)]: Path(D:/a/1/s/target_repo/biztalk/adapters-and-accelerators/software-prerequisites-for-biztalk-adapter-pack-2016.md) contains invalid char.
Parameter name: path -->[!INCLUDE[adapterpacknoversion](../includes/adapterpacknoversion-md.md)]<!--END ERROR INCLUDE --></li><br/><br/><li>The enterprise application clients and associated software. See <strong>Supported enterprise application versions</strong> (in this topic).</li><br /><br /><li>Internet Information Services (IIS) version that comes with the operating system. <a href="https://support.microsoft.com/kb/224609" data-raw-source="[KB 224609](https://support.microsoft.com/kb/224609)">KB 224609</a> lists the versions.</li> </ul> |                   Microsoft SharePoint Software Development Kit (SDK)                    |

<a name="BKMK_SuppLOB"></a>   
## Supported enterprise application versions  
To see the specific LOB system versions that are supported by the BizTalk Adapter Pack, see 
**[Supported Line-of-Business (LOB) systems](http://social.technet.microsoft.com/wiki/contents/articles/17631.biztalk-server-supported-line-of-business-lob-systems.aspx)**.

This section lists any extra info for each adapter, such as any client DLLs required for each adapter.  

### Oracle Database adapter  

-   Optional: If you use distributed transactions with the Oracle database, install **Oracle Services for Microsoft Transaction Server** (part of the Oracle client installation) on the computer running the adapter client.  

-   For your application to work with the most recent version of ODP.NET, install the **policy DLLs** and register the DLLs in the GAC. See [Oracle Data Provider for .NET FAQ](http://www.oracle.com/technetwork/database/windows/faq-093106.html).  

### Oracle E-Business adapter  

-   Optional: To use distributed transactions with the Oracle database, install **Oracle Services for Microsoft Transaction Server** (part of the Oracle client installation) on the computer running the adapter client.  

-   For your application to work with the most recent version of ODP.NET, install the **policy DLLs** and register the DLLs in the GAC. See [Oracle Data Provider for .NET FAQ](http://www.oracle.com/technetwork/database/windows/faq-093106.html).  

### SAP adapter  

- The [!INCLUDE [adaptersap_short](../includes/adaptersap-short-md.md)] requires Unicode version of the RFC SDK irrespective of whether the SAP system is Unicode or non-Unicode.  

- <strong>Required drivers</strong>: The following table lists the DLLs required by the [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)] to interface with the SAP system:  


  | SAP client version |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Required drivers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
  |--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
  |        7.2         | - <strong>SAP RFC SDK 7.10 UNICODE</strong>. This is available as part of SNOTE<sup><em></sup> 27517. The instructions to download the SDK are available at <a href="http://go.microsoft.com/fwlink/?LinkId=94691" data-raw-source="[http://go.microsoft.com/fwlink/?LinkId=94691](http://go.microsoft.com/fwlink/?LinkId=94691)">http://go.microsoft.com/fwlink/?LinkId=94691</a>. After you have downloaded and extracted the SDK, copy all the DLLs from the \rfcsdk\bin and \rfcsdk\lib folders to the relevant location mentioned preceding this table.<br /><br /> - DLLs are available from SAP as part of **R3DLLINST.zip</em><em>. This contains Microsoft run-time DLLs and can be downloaded from the SAP site. See SNOTE<sup></em></sup> 684106 for more information. You can download the .zip file from <a href="http://go.microsoft.com/fwlink/?LinkId=94693" data-raw-source="[http://go.microsoft.com/fwlink/?LinkId=94693](http://go.microsoft.com/fwlink/?LinkId=94693)">http://go.microsoft.com/fwlink/?LinkId=94693</a>. This link has an “Attachments” option from where you can download the package.<br /><br /> - Microsoft Visual C++ run-time DLLs required for SAP 7.1 client are available from the following links:<br /><br /> - <strong>For 32-bit SAP 7.1 client</strong>:  Vcredist_x86.exe from <a href="http://go.microsoft.com/fwlink/?LinkId=107086" data-raw-source="[http://go.microsoft.com/fwlink/?LinkId=107086](http://go.microsoft.com/fwlink/?LinkId=107086)">http://go.microsoft.com/fwlink/?LinkId=107086</a>.<br /><br /> -                                 <strong>For 64-bit SAP 7.1 client</strong>: Vcredist_x64.exe from <a href="http://go.microsoft.com/fwlink/?LinkId=107087" data-raw-source="[http://go.microsoft.com/fwlink/?LinkId=107087](http://go.microsoft.com/fwlink/?LinkId=107087)">http://go.microsoft.com/fwlink/?LinkId=107087</a>.<br /><br /> - If you use SAP Secure Network Communications (SNC) to connect to an SAP system, you must also have the relevant DLLs from SAP. These DLLs are different for 32-bit and 64-bit platforms and are available with SNOTE<sup><em></sup> 352295. You can download the DLLs from <a href="http://go.microsoft.com/fwlink/?LinkId=104032" data-raw-source="[http://go.microsoft.com/fwlink/?LinkId=104032](http://go.microsoft.com/fwlink/?LinkId=104032)">http://go.microsoft.com/fwlink/?LinkId=104032</a>. This link has an “Attachments” option from where you can download the package. The names of the DLLs are:<br /><br /> - **For 32-bit</em><em>: gsskrb5.dll, gssntlm.dll<br /><br /> - **For 64-bit x86</em>*: gx64krb5.dll, gx64ntlm.dll |

   > [!TIP]
   > SNOTEs are release notes that accompany fixes released by SAP.  

  Most of the packages that contain these DLLs must be downloaded from the SAP Service Marketplace. To get downloads from the SAP Service Marketplace: 

  1. Install the Download Manager available from the SAP Service Marketplace.  

  2. Configure the Download Manager by using your credentials for the SAP Service Marketplace.  

  3. Be authorized by the SAP administrator in your organization to download software from the SAP service website. This is required because access to the SAP Software Distribution Center is restricted by a 'Download Software' authorization object. This ensures that software is downloaded only by authorized users.  

  4. Install the SAPCAR program, which is required to extract the files from the packages that you download from the SAP Service Marketplace. SAPCAR is also available from the SAP Service Marketplace.  

     For the 32-bit and 64-bit version of the [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)], you must have the respective 32-bit and 64-bit versions of these DLLs.  

  -   On a 32-bit computer, the 32-bit version of the DLLs must be added to the C:\Windows\System32 folder.  

  -   On a 64-bit computer, the 32-bit version of the DLLs must be added to the C:\Windows\SysWow64 folder. The 64-bit version of the DLLs must be added to the C:\Windows\System32 folder.  


### Siebel adapter  
No extra steps.

### SQL adapter  

**Required drivers** for SQL Server 2014:  

-   If you use the UDTs shipped with the SQL Server versions, for example, Geography, make sure the following DLLs are present on the computer where you use the adapter to perform operations on SQL Server. For example, if you create BizTalk projects to perform operations on SQL Server, these DLLs must be present on the computer where BizTalk Server is running.  

    -   Make sure Microsoft.SqlServer.Types.dll is added to the GAC.  

    -   Make sure SqlServerSpatial.dll is available in the System32 folder.    

    You can install these DLLs on the computer by running the SQL Server setup and selecting **Management Tools – Basic** and **Management Tools – Complete** in the **Feature Selection** page of the wizard.          

-   If you use the adapter to perform operations on columns of FILESTREAM data types, make sure you have SQL Client Connectivity SDK installed. You can install the SQL Client Connectivity SDK by running the SQL Server setup and selecting **SQL Client Connectivity SDK** in the **Feature Selection** page of the wizard. The adapter uses the sqlncli10.dll, installed with the SQL Client Connectivity SDK, to perform FILESTREAM operations.  

-   If you create your own UDTs in SQL Server, make sure the respective assemblies for the UDTs are added to the GAC.

## 64-bit host instance support

The Siebel adapter is supported in a 32-bit host instance. It is not supported to run the Siebel adapter in a 64-bit host instance. 

All the other adapters can run in a 32-bit or 64-bit host instance. 

 For more information about the supported installation scenarios for installing the 32-bit and 64-bit [!INCLUDE [adapterpacknoversion](../includes/adapterpacknoversion-md.md)], see <strong>32-bit and 64-bit install scenarios</strong> at [Installing BAP](../adapters-and-accelerators/installing-the-biztalk-adapter-pack-2016.md).  

## Next step
[Install the BizTalk Adapter Pack](../adapters-and-accelerators/installing-the-biztalk-adapter-pack-2016.md)  
