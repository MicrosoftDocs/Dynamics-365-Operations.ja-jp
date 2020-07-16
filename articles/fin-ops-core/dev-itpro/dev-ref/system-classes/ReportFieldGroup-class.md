---
title: ReportFieldGroup クラス
description: このトピックでは、ReportFieldGroup クラスについて説明します。
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
ms.openlocfilehash: fc6cb020861ff94f9f599570f4e8531ecff87812
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502840"
---
# <a name="class-reportfieldgroup"></a>クラス ReportFieldGroup

[!include [banner](../../includes/banner.md)]

```xpp
class ReportFieldGroup extends TreeNode
```

ReportFieldGroup クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                        | 説明                                                   |
|-----------------------------------------------|---------------------------------------------------------------|
| public int autoFieldGroupOrder(\[int value\]) |                                                               |
| public str dataGroup(\[str value\])           |                                                               |
| public int fieldCount()                       |                                                               |
| public ReportControl fieldNumber(int number)  |                                                               |
| public TableId table(\[TableId value\])       | オブジェクトに関連付けられているテーブル ID を取得または設定します。 |

## <a name="method-autofieldgrouporder"></a>メソッド autoFieldGroupOrder

```xpp
public int autoFieldGroupOrder([int value])
```

### <a name="parameters---autofieldgrouporder"></a>パラメーター - autoFieldGroupOrder

値  

### <a name="return-value---autofieldgrouporder"></a>戻り値 - autoFieldGroupOrder

## <a name="method-datagroup"></a>メソッド dataGroup

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a>パラメーター - dataGroup

値  

### <a name="return-value---datagroup"></a>戻り値 - dataGroup

## <a name="method-fieldcount"></a>メソッド fieldCount

```xpp
public int fieldCount()
```

### <a name="return-value---fieldcount"></a>戻り値 - fieldCount

## <a name="method-fieldnumber"></a>メソッド fieldNumber

```xpp
public ReportControl fieldNumber(int number)
```

### <a name="parameters---fieldnumber"></a>パラメーター - fieldNumber

番号  

### <a name="return-value---fieldnumber"></a>戻り値 - fieldNumber

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

