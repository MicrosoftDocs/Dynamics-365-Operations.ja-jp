---
title: IF ER 関数
description: このトピックでは、IF 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687005"
---
# <a name="if-er-function"></a>IF ER 関数

[!include [banner](../includes/banner.md)]

`IF` 関数は、指定された条件が満たされている場合、最初に指定された値を返します。 それ以外の場合、2 つ目に指定された値を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。

## <a name="syntax"></a>構文

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>引数

`condition`: *ブール値*

テストする必要がある有効な条件式。

`first value`: *サポートされているいずれかのデータ型*

条件が満たされた場合に返される結果。

`second value`: *サポートされているいずれかのデータ型*

条件が満たされていない場合に返される結果。

## <a name="return-values"></a>戻り値

*サポートされているいずれかのデータ型*

サポートされているいずれかのデータ型の結果値。

## <a name="usage-notes"></a>使用上の注意

`first value` および `second value` 引数 は、同じデータ型を使用して指定する必要があります。 構成された値のデータ型が一致しない場合は、デザイン時に例外がスローされます。

最初の結果値と 2 番目の結果値が *コンテナー (レコード)* または *レコード リスト* データ型の値である場合、結果には両方の値に存在するフィールドのみが含まれます。

## <a name="example"></a>例

`IF (1=2, "condition is met", "condition is not met")` は、文字列 **"条件を満たしていない"** を返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)
