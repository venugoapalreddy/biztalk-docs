---
title: "Support for ODBC 2 Level 2 Functions | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b09a32b3-4af8-435b-888a-787c93b50c83
caps.latest.revision: 3
author: "gplarsen"
ms.author: "hisdocs; plarsen"
manager: "anneta"
---
# Support for ODBC 2 Level 2 Functions
The following table lists the ODBC 2.*x* level 2 functions that are supported by the Microsoft ODBC Driver for DB2.  


| ODBC 2.<em>x</em> level 2 functions supported |                       Functions supported by the Microsoft ODBC Driver for DB2                        |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------|
|       <strong>SQLBrowseConnect</strong>       |                                                  No                                                   |
|     <strong>SQLColumnPrivileges</strong>      |                                                  No                                                   |
|        <strong>SQLDataSources</strong>        |                  Yes. This function is actually supported by the ODBC Driver Manager                  |
|       <strong>SQLDescribeParam</strong>       |                                                  No                                                   |
|          <strong>SQLDrivers</strong>          |                  Yes. This function is actually supported by the ODBC Driver Manager                  |
|       <strong>SQLExtendedFetch</strong>       |                               Yes, but supports forward scrolling only                                |
|        <strong>SQLForeignKeys</strong>        |                                                  No                                                   |
|        <strong>SQLMoreResults</strong>        |                                                  Yes                                                  |
|         <strong>SQLNativeSQL</strong>         |                                                  Yes                                                  |
|         <strong>SQLNumParams</strong>         |                                                  Yes                                                  |
|       <strong>SQLParamOptions</strong>        |                                                  Yes                                                  |
|        <strong>SQLPrimaryKeys</strong>        | Yes, but SQL grammar conformance varies depending on the version of the DB2 database that is accessed |
|     <strong>SQLProcedureColumns</strong>      |                                                  Yes                                                  |
|        <strong>SQLProcedures</strong>         |                                                  Yes                                                  |
|            <strong>SetPos</strong>            |                                                  Yes                                                  |
|     <strong>SQLSetScrollOptions</strong>      |                                                  Yes                                                  |
|      <strong>SQLTablePrivileges</strong>      |                                                  No                                                   |

