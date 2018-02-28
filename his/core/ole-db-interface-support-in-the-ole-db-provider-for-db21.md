---
title: "OLE DB Interface Support in the OLE DB Provider for DB21 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c3dac35d-f7c4-4e96-b1db-f105fa5a06fb
caps.latest.revision: 3
author: "gplarsen"
ms.author: "hisdocs; plarsen"
manager: "anneta"
---
# OLE DB Interface Support in the OLE DB Provider for DB2
The following table summarizes the OLE DB version 2.0 interfaces that are supported by the current version of Microsoft OLE DB Provider for DB2.  


|                                          Object                                           |                 Interface                  |         Support         |
|-------------------------------------------------------------------------------------------|--------------------------------------------|-------------------------|
|           [Command Object](../core/command-object-ole-db-provider-for-db2-2.md)           |         <strong>IAccessor</strong>         |           Yes           |
|                                                                                           |       <strong>IColumnsInfo</strong>        |           Yes           |
|                                                                                           |      <strong>IColumnsRowset</strong>       |           Yes           |
|                                                                                           |         <strong>ICommand</strong>          |           Yes           |
|                                                                                           |      <strong>ICommandPersist</strong>      |           No            |
|                                                                                           |      <strong>ICommandPrepare</strong>      |           Yes           |
|                                                                                           |    <strong>ICommandProperties</strong>     |           Yes           |
|                                                                                           |       <strong>ICommandText</strong>        |           Yes           |
|                                                                                           |  <strong>ICommandWithParameters</strong>   |           Yes           |
|                                                                                           |       <strong>IConvertType</strong>        |           Yes           |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           Yes           |
| [CustomErrorObject Object](../core/customerrorobject-object-ole-db-provider-for-db2-1.md) |       <strong>IErrorLookup</strong>        |           Yes           |
|                                                                                           |       <strong>ISQLErrorInfo</strong>       |           Yes           |
|        [DataSource Object](../core/datasource-object-ole-db-provider-for-db2-2.md)        |      <strong>IDBAsynchStatus</strong>      |           Yes           |
|                                                                                           | <strong>IConnectionPointContainer</strong> |           No            |
|                                                                                           |     <strong>IDBCreateSession</strong>      |           Yes           |
|                                                                                           |    <strong>IDBDataSourceAdmin</strong>     |           Yes           |
|                                                                                           |          <strong>IDBInfo</strong>          |           Yes           |
|                                                                                           |       <strong>IDBInitialize</strong>       |           Yes           |
|                                                                                           |       <strong>IDBProperties</strong>       |           Yes           |
|                                                                                           |         <strong>IPersist</strong>          |           Yes           |
|                                                                                           |       <strong>IPersistFile</strong>        |           Yes           |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           Yes           |
|                                <strong>Enumerator</strong>                                |       <strong>IDBInitialize</strong>       |           No            |
|                                                                                           |       <strong>IDBProperties</strong>       |           No            |
|                                                                                           |     <strong>IParseDisplayName</strong>     |           No            |
|                                                                                           |      <strong>ISourcesRowset</strong>       |           No            |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           No            |
|       [ErrorObject Object](../core/errorobject-object-ole-db-provider-for-db2-1.md)       |       <strong>IErrorRecords</strong>       |           Yes           |
|       [ErrorRecord Object](../core/errorrecord-object-ole-db-provider-for-db2-1.md)       |        <strong>IErrorInfo</strong>         |           Yes           |
|                                  <strong>Index</strong>                                   |         <strong>IAccessor</strong>         |           No            |
|                                                                                           |       <strong>IColumnsInfo</strong>        |           No            |
|                                                                                           |       <strong>IConvertType</strong>        |           No            |
|                                                                                           |          <strong>IRowset</strong>          |           No            |
|                                                                                           |       <strong>IRowsetChange</strong>       |           No            |
|                                                                                           |        <strong>IRowsetFind</strong>        |           No            |
|                                                                                           |      <strong>IRowsetIdentity</strong>      |           No            |
|                                                                                           |       <strong>IRowsetIndex</strong>        |           No            |
|                                                                                           |        <strong>IRowsetInfo</strong>        |           No            |
|                                                                                           |       <strong>IRowsetLocate</strong>       |           No            |
|                                                                                           |      <strong>IRowsetRefresh</strong>       |           No            |
|                                                                                           |       <strong>IRowsetScroll</strong>       |           No            |
|                                                                                           |       <strong>IRowsetUpdate</strong>       |           No            |
|                                                                                           |        <strong>IRowsetView</strong>        |           No            |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           No            |
|                             <strong>MultipleResults</strong>                              |     <strong>IMultipleResults</strong>      | Yes (Stored Procedures) |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           No            |
|            [Rowset Object](../core/rowset-object-ole-db-provider-for-db2-1.md)            |         <strong>IAccessor</strong>         |           Yes           |
|                                                                                           |     <strong>IChapteredRowset</strong>      |           No            |
|                                                                                           |       <strong>IColumnsInfo</strong>        |           Yes           |
|                                                                                           |      <strong>IColumnsRowset</strong>       |           Yes           |
|                                                                                           | <strong>IConnectionPointContainer</strong> |           No            |
|                                                                                           |       <strong>IConvertType</strong>        |           Yes           |
|                                                                                           |      <strong>IDBAsynchStatus</strong>      |           No            |
|                                                                                           |          <strong>IRowset</strong>          |           Yes           |
|                                                                                           |       <strong>IRowsetChange</strong>       |           Yes           |
|                                                                                           |   <strong>IRowsetChapterMember</strong>    |           No            |
|                                                                                           |        <strong>IRowsetFind</strong>        |           No            |
|                                                                                           |      <strong>IRowsetIdentity</strong>      |           No            |
|                                                                                           |       <strong>IRowsetIndex</strong>        |           No            |
|                                                                                           |        <strong>IRowsetInfo</strong>        |           Yes           |
|                                                                                           |       <strong>IRowsetLocate</strong>       |           No            |
|                                                                                           |      <strong>IRowsetRefresh</strong>       |           No            |
|                                                                                           |       <strong>IRowsetScroll</strong>       |           No            |
|                                                                                           |       <strong>IRowsetUpdate</strong>       |           Yes           |
|                                                                                           |        <strong>IRowsetView</strong>        |           No            |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           Yes           |
|           [Session Object](../core/session-object-ole-db-provider-for-db2-1.md)           |        <strong>IAlterIndex</strong>        |           No            |
|                                                                                           |        <strong>IAlterTable</strong>        |           No            |
|                                                                                           |     <strong>IDBCreateCommand</strong>      |           Yes           |
|                                                                                           |      <strong>IDBSchemaRowset</strong>      |           Yes           |
|                                                                                           |      <strong>IGetDataSource</strong>       |           Yes           |
|                                                                                           |     <strong>IIndexDefinition</strong>      |           No            |
|                                                                                           |        <strong>IOpenRowset</strong>        |           Yes           |
|                                                                                           |    <strong>ISessionProperties</strong>     |           Yes           |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           Yes           |
|                                                                                           |     <strong>ITableDefinition</strong>      |           No            |
|                                                                                           |       <strong>ITransaction</strong>        |           Yes           |
|                                                                                           |     <strong>ITransactionJoin</strong>      |           No            |
|                                                                                           |     <strong>ITransactionLocal</strong>     |           Yes           |
|                                                                                           |    <strong>ITransactionObject</strong>     |           Yes           |
|       [Transaction Object](../core/transaction-object-ole-db-provider-for-db2-1.md)       | <strong>IConnectionPointContainer</strong> |           No            |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           Yes           |
|                                                                                           |       <strong>ITransaction</strong>        |           Yes           |
|                            <strong>TransactionOptions</strong>                            |     <strong>ISupportErrorInfo</strong>     |           Yes           |
|                                                                                           |    <strong>ITransactionOptions</strong>    |           Yes           |
|                                   <strong>View</strong>                                   |         <strong>IAccessor</strong>         |           No            |
|                                                                                           |       <strong>IColumnsInfo</strong>        |           No            |
|                                                                                           |     <strong>ISupportErrorInfo</strong>     |           No            |
|                                                                                           |       <strong>IViewChapter</strong>        |           No            |
|                                                                                           |        <strong>IViewFilter</strong>        |           No            |
|                                                                                           |        <strong>IViewRowset</strong>        |           No            |
|                                                                                           |         <strong>IViewSort</strong>         |           No            |

