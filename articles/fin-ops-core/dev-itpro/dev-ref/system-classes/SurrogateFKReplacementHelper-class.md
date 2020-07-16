---
title: SurrogateFKReplacementHelper クラス
description: このトピックでは、SurrogateFKReplacementHelper クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6c3536299786bdc55177ed68e2ccd92332eb13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502794"
---
# <a name="class-surrogatefkreplacementhelper"></a>クラス SurrogateFKReplacementHelper

[!include [banner](../../includes/banner.md)]

```xpp
class SurrogateFKReplacementHelper extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                             | 説明                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)                                                                                             |                                                 |
| public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)                                                              |                                                 |
| public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])                                                                                                                       |                                                 |
| public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])                   |                                                 |
| public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])                                                               |                                                 |
| public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\]) |                                                 |
| public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])                                                                                        |                                                 |
| public str extendedDataType()                                                                                                                                                                                      |                                                 |
| public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)                                                                                               |                                                 |
| public boolean isResolvedReferenceAmbiguous(Query query)                                                                                                                                                           |                                                 |
| public str primaryKeyTableName()                                                                                                                                                                                   |                                                 |
| public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])                                                                                |                                                 |
| public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)                                                     |                                                 |
| public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])                                                                                                                                  |                                                 |
| public FieldBinding surrogateForeignKeyFieldBinding()                                                                                                                                                              |                                                 |
| ::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)                                                                                                                    |                                                 |
| ::public static SurrogateFKReplacementHelper constructForEDT(str edtName)                                                                                                                                          |                                                 |
| ::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)                                                                                                                                  |                                                 |
| ::public static str defaultPrimaryKeyQueryDataSourceName()                                                                                                                                                         |                                                 |
| ::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)                                                                                                                    |                                                 |
| ::public static str implicitReplacementFieldGroupName()                                                                                                                                                            |                                                 |
| private void new(FieldBinding surrogateForeignKeyBinding)                                                                                                                                                          | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-adddefaultrequiredjoins"></a>メソッド addDefaultRequiredJoins

```xpp
public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)
```

### <a name="parameters---adddefaultrequiredjoins"></a>パラメーター - addDefaultRequiredJoins

foreignKeyQueryBuildDataSource  

<!-- -->

replacementFieldGroupName  

### <a name="return-value---adddefaultrequiredjoins"></a>戻り値 - addDefaultRequiredJoins

## <a name="method-addrequiredjoins"></a>メソッド addRequiredJoins

```xpp
public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)
```

### <a name="parameters---addrequiredjoins"></a>パラメーター - addRequiredJoins

requiredJoinsAsRelationPathList  

<!-- -->

foreignKeyQueryBuildDataSource  

<!-- -->

replacementFieldGroupName  

### <a name="return-value---addrequiredjoins"></a>戻り値 - addRequiredJoins

## <a name="method-displaybindings"></a>メソッド displayBindings

```xpp
public List displayBindings(str replacementFieldGroupName, [boolean distinctBindingsOnly])
```

### <a name="parameters---displaybindings"></a>パラメーター - displayBindings

replacementFieldGroupName  

<!-- -->

distinctBindingsOnly  

### <a name="return-value---displaybindings"></a>戻り値 - displayBindings

## <a name="method-displayvaluesfromqueryrun"></a>メソッド displayValuesFromQueryRun

```xpp
public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource], [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromqueryrun"></a>パラメーター - displayValuesFromQueryRun

queryRun  

<!-- -->

replacementFieldGroupName  

<!-- -->

isRootPrimaryKeyDataSource  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

### <a name="return-value---displayvaluesfromqueryrun"></a>戻り値 - displayValuesFromQueryRun

## <a name="method-displayvaluesfromrecid"></a>メソッド displayValuesFromRecID

```xpp
public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromrecid"></a>パラメーター - displayValuesFromRecID

recIDValue  

<!-- -->

replacementFieldGroupName  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

### <a name="return-value---displayvaluesfromrecid"></a>戻り値 - displayValuesFromRecID

## <a name="method-displayvaluesfromrootds"></a>メソッド displayValuesFromRootDS

```xpp
public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])
```

### <a name="parameters---displayvaluesfromrootds"></a>パラメーター - displayValuesFromRootDS

rootQueryBuildDataSource  

<!-- -->

isPrimaryKeyDataSource  

<!-- -->

replacementFieldGroupName  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

### <a name="return-value---displayvaluesfromrootds"></a>戻り値 - displayValuesFromRootDS

## <a name="method-displayvalue"></a>メソッド displayValue

```xpp
public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, [boolean isRootPrimaryKeyDataSource])
```

### <a name="parameters---displayvalue"></a>パラメーター - displayValue

resolvedCursor  

<!-- -->

displayBinding  

<!-- -->

isRootPrimaryKeyDataSource  

### <a name="return-value---displayvalue"></a>戻り値 - displayValue

## <a name="method-extendeddatatype"></a>メソッド extendedDataType

```xpp
public str extendedDataType()
```

### <a name="return-value---extendeddatatype"></a>戻り値 - extendedDataType

## <a name="method-generateresolvereferencequery"></a>メソッド generateResolveReferenceQuery

```xpp
public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)
```

### <a name="parameters---generateresolvereferencequery"></a>パラメーター - generateResolveReferenceQuery

requiredJoinsAsRelationPathList  

<!-- -->

filterValuesAsFilterValueList  

### <a name="return-value---generateresolvereferencequery"></a>戻り値 - generateResolveReferenceQuery

## <a name="method-isresolvedreferenceambiguous"></a>メソッド isResolvedReferenceAmbiguous

```xpp
public boolean isResolvedReferenceAmbiguous(Query query)
```

### <a name="parameters---isresolvedreferenceambiguous"></a>パラメーター - isResolvedReferenceAmbiguous

クエリ  

### <a name="return-value---isresolvedreferenceambiguous"></a>戻り値 - isResolvedReferenceAmbiguous

## <a name="method-primarykeytablename"></a>メソッド primaryKeyTableName

```xpp
public str primaryKeyTableName()
```

### <a name="return-value---primarykeytablename"></a>戻り値 - primaryKeyTableName

## <a name="method-querybuilddatasourcebindingsforquery"></a>メソッド queryBuildDataSourceBindingsForQuery

```xpp
public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource])
```

### <a name="parameters---querybuilddatasourcebindingsforquery"></a>パラメーター - queryBuildDataSourceBindingsForQuery

クエリ  

<!-- -->

replacementFieldGroupName  

<!-- -->

isRootPrimaryKeyDataSource  

### <a name="return-value---querybuilddatasourcebindingsforquery"></a>戻り値 - queryBuildDataSourceBindingsForQuery

## <a name="method-querybuilddatasourcebindingsforrootds"></a>メソッド queryBuildDataSourceBindingsForRootDS

```xpp
public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)
```

### <a name="parameters---querybuilddatasourcebindingsforrootds"></a>パラメーター - queryBuildDataSourceBindingsForRootDS

rootQueryBuildDataSource  

<!-- -->

isPrimaryKeyDataSource  

<!-- -->

replacementFieldGroupName  

### <a name="return-value---querybuilddatasourcebindingsforrootds"></a>戻り値 - queryBuildDataSourceBindingsForRootDS

## <a name="method-resolvereference"></a>メソッド resolveReference

```xpp
public Common resolveReference(Query query, [boolean ignoreAmbiguousReference])
```

### <a name="parameters---resolvereference"></a>パラメーター - resolveReference

クエリ  

<!-- -->

ignoreAmbiguousReference  

### <a name="return-value---resolvereference"></a>戻り値 - resolveReference

## <a name="method-surrogateforeignkeyfieldbinding"></a>メソッド surrogateForeignKeyFieldBinding

```xpp
public FieldBinding surrogateForeignKeyFieldBinding()
```

### <a name="return-value---surrogateforeignkeyfieldbinding"></a>戻り値 - surrogateForeignKeyFieldBinding

## <a name="method-construct"></a>メソッド construct

```xpp
public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)
```

### <a name="parameters---construct"></a>パラメーター - construct

surrogateForeignKeyBinding  

### <a name="return-value---construct"></a>戻り値 - construct

## <a name="method-constructforedt"></a>メソッド constructForEDT

```xpp
public static SurrogateFKReplacementHelper constructForEDT(str edtName)
```

### <a name="parameters---constructforedt"></a>パラメーター - constructForEDT

edtName  

### <a name="return-value---constructforedt"></a>戻り値 - constructForEDT

## <a name="method-constructforpktable"></a>メソッド constructForPKTable

```xpp
public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)
```

### <a name="parameters---constructforpktable"></a>パラメーター - constructForPKTable

pkTableName  

### <a name="return-value---constructforpktable"></a>戻り値 - constructForPKTable

## <a name="method-defaultprimarykeyquerydatasourcename"></a>メソッド defaultPrimaryKeyQueryDataSourceName

```xpp
public static str defaultPrimaryKeyQueryDataSourceName()
```

### <a name="return-value---defaultprimarykeyquerydatasourcename"></a>戻り値 - defaultPrimaryKeyQueryDataSourceName

## <a name="method-deprecated_workflowcaption"></a>メソッド DEPRECATED\_WorkflowCaption

```xpp
public static str DEPRECATED_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)
```

### <a name="parameters---deprecated_workflowcaption"></a>パラメーター - DEPRECATED\_WorkflowCaption

tableName  

<!-- -->

fieldName  

<!-- -->

recIDValue  

### <a name="return-value---deprecated_workflowcaption"></a>戻り値 - DEPRECATED\_WorkflowCaption

## <a name="method-implicitreplacementfieldgroupname"></a>メソッド implicitReplacementFieldGroupName

```xpp
public static str implicitReplacementFieldGroupName()
```

### <a name="return-value---implicitreplacementfieldgroupname"></a>戻り値 - implicitReplacementFieldGroupName

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
private void new(FieldBinding surrogateForeignKeyBinding)
```

### <a name="parameters---new"></a>パラメーター - new

surrogateForeignKeyBinding  

