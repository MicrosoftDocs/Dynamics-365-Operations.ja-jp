---
title: DataImportSessionInfo クラス
description: このトピックでは、DataImportSessionInfo クラスについて説明します。
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
ms.openlocfilehash: 58c63825f075ffe4ea1aa5218bdf4a5ff805b3b0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502737"
---
# <a name="class-dataimportsessioninfo"></a>クラス DataImportSessionInfo

[!include [banner](../../includes/banner.md)]

```xpp
class DataImportSessionInfo extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                     |
|--------------------------------------------------------------------------------|-------------------------------------------------|
| public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate) |                                                 |
| public int getCurrentProgress()                                                |                                                 |
| public str getCurrentTable()                                                   |                                                 |
| public int setSourceGUID(Guid szSourceGUID)                                    |                                                 |
| public int setSysDataImpLogId(int sysDataImpLogId)                             |                                                 |
| public void new(str szInpFileName, boolean fUpdateExistingData)                | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-addimporttable"></a>メソッド addImportTable

```xpp
public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate)
```

### <a name="parameters---addimporttable"></a>パラメーター - addImportTable

szTabName  

<!-- -->

ulTableId  

<!-- -->

fAlwaysUpdate  

### <a name="return-value---addimporttable"></a>戻り値 - addImportTable

## <a name="method-getcurrentprogress"></a>メソッド getCurrentProgress

```xpp
public int getCurrentProgress()
```

### <a name="return-value---getcurrentprogress"></a>戻り値 - getCurrentProgress

## <a name="method-getcurrenttable"></a>メソッド getCurrentTable

```xpp
public str getCurrentTable()
```

### <a name="return-value---getcurrenttable"></a>戻り値 - getCurrentTable

## <a name="method-setsourceguid"></a>メソッド setSourceGUID

```xpp
public int setSourceGUID(Guid szSourceGUID)
```

### <a name="parameters---setsourceguid"></a>パラメーター - setSourceGUID

szSourceGUID  

### <a name="return-value---setsourceguid"></a>戻り値 - setSourceGUID

## <a name="method-setsysdataimplogid"></a>メソッド setSysDataImpLogId

```xpp
public int setSysDataImpLogId(int sysDataImpLogId)
```

### <a name="parameters---setsysdataimplogid"></a>パラメーター - setSysDataImpLogId

sysDataImpLogId  

### <a name="return-value---setsysdataimplogid"></a>戻り値 - setSysDataImpLogId

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(str szInpFileName, boolean fUpdateExistingData)
```

### <a name="parameters---new"></a>パラメーター - new

szInpFileName  

<!-- -->

fUpdateExistingData  

