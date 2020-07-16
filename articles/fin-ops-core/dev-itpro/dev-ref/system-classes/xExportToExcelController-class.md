---
title: xExportToExcelController クラス
description: このトピックでは、xExportToExcelControlle クラスについて説明します。
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
ms.openlocfilehash: 531082acb9efccbfa5b799e1286129a828cee8a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502681"
---
# <a name="class-xexporttoexcelcontroller"></a>クラス xExportToExcelController

[!include [banner](../../includes/banner.md)]

```xpp
class xExportToExcelController extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                             | 説明 |
|------------------------------------------------------------------------------------------------------------------------------------|-------------|
| public boolean export()                                                                                                            |             |
| public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)                                                     |             |
| public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows) |             |
| public void new()                                                                                                                  |             |

## <a name="method-export"></a>メソッド export

```xpp
public boolean export()
```

### <a name="return-value---export"></a>戻り値 - export

## <a name="method-exportgrid"></a>メソッド exportGrid

```xpp
public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)
```

### <a name="parameters---exportgrid"></a>パラメーター - exportGrid

gridControl  

<!-- -->

onlyMarkedRows  

### <a name="return-value---exportgrid"></a>戻り値 - exportGrid

## <a name="method-performstaticexport"></a>メソッド performStaticExport

```xpp
public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows)
```

### <a name="parameters---performstaticexport"></a>パラメーター - performStaticExport

formRun  

<!-- -->

gridControl  

<!-- -->

stream  

<!-- -->

onlyMarkedRows  

### <a name="return-value---performstaticexport"></a>戻り値 - performStaticExport

## <a name="method-new"></a>メソッド new

```xpp
public void new()
```

