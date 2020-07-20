---
title: DataImportManager クラス
description: このトピックでは、DataImportManager クラスについて説明します。
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
ms.openlocfilehash: e670942d98490cea0e8a505ff32a960eb9ccf284
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502738"
---
# <a name="class-dataimportmanager"></a>クラス DataImportManager

[!include [banner](../../includes/banner.md)]

```xpp
class DataImportManager extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                        | 説明                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| ::public static int commitImportSessionInfo(DataImportSessionInfo impInfo)                    |                                                            |
| ::public static int endTableDataCopy(ImportTableDataInfo dataInfo)                            |                                                            |
| ::public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)                         |                                                            |
| ::public static int finishMergeTableData()                                                    |                                                            |
| ::public static int getImportSessionProgress(DataImportSessionInfo impInfo)                   |                                                            |
| ::public static int mergeAllData()                                                            |                                                            |
| ::public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)   |                                                            |
| ::public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume) |                                                            |
| public void new()                                                                             | DataImportManager クラスの新しいインスタンスを初期化します。 |

## <a name="method-commitimportsessioninfo"></a>メソッド commitImportSessionInfo

```xpp
public static int commitImportSessionInfo(DataImportSessionInfo impInfo)
```

### <a name="parameters---commitimportsessioninfo"></a>パラメーター - commitImportSessionInfo

impInfo  

### <a name="return-value---commitimportsessioninfo"></a>戻り値 - commitImportSessionInfo

## <a name="method-endtabledatacopy"></a>メソッド endTableDataCopy

```xpp
public static int endTableDataCopy(ImportTableDataInfo dataInfo)
```

### <a name="parameters---endtabledatacopy"></a>パラメーター - endTableDataCopy

dataInfo  

### <a name="return-value---endtabledatacopy"></a>戻り値 - endTableDataCopy

## <a name="method-endtableschemacopy"></a>メソッド endTableSchemaCopy

```xpp
public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)
```

### <a name="parameters---endtableschemacopy"></a>パラメーター - endTableSchemaCopy

schInfo  

### <a name="return-value---endtableschemacopy"></a>戻り値 - endTableSchemaCopy

## <a name="method-finishmergetabledata"></a>メソッド finishMergeTableData

```xpp
public static int finishMergeTableData()
```

### <a name="return-value---finishmergetabledata"></a>戻り値 - finishMergeTableData

## <a name="method-getimportsessionprogress"></a>メソッド getImportSessionProgress

```xpp
public static int getImportSessionProgress(DataImportSessionInfo impInfo)
```

### <a name="parameters---getimportsessionprogress"></a>パラメーター - getImportSessionProgress

impInfo  

### <a name="return-value---getimportsessionprogress"></a>戻り値 - getImportSessionProgress

## <a name="method-mergealldata"></a>メソッド mergeAllData

```xpp
public static int mergeAllData()
```

### <a name="return-value---mergealldata"></a>戻り値 - mergeAllData

## <a name="method-mergetabledata"></a>メソッド mergeTableData

```xpp
public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)
```

### <a name="parameters---mergetabledata"></a>パラメーター - mergeTableData

mergeStep  

<!-- -->

tableId  

<!-- -->

updateHeartbeat  

### <a name="return-value---mergetabledata"></a>戻り値 - mergeTableData

## <a name="method-recoverimportsession"></a>メソッド recoverImportSession

```xpp
public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume)
```

### <a name="parameters---recoverimportsession"></a>パラメーター - recoverImportSession

impInfo  

<!-- -->

fTryToResume  

### <a name="return-value---recoverimportsession"></a>戻り値 - recoverImportSession

## <a name="method-new"></a>メソッド new

DataImportManager クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

