---
title: WHERE ER 関数
description: この記事では、WHERE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273161"
---
# <a name="where-er-function"></a>WHERE ER 関数

[!include [banner](../includes/banner.md)]

`WHERE` 関数は、指定されたリストを、指定された条件に基づいてフィルタリングされた後に *レコード リスト* 値として返します。

## <a name="syntax"></a>構文

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`condition`: *ブール値*

指定されたリストのレコードをフィルター処理するために使用される有効な条件式。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

この関数は [FILTER](er-functions-list-filter.md) 関数とは異なります。指定された条件がメモリに存在する *レコード リスト* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。

この関数に対して構成されている引数 (`list` および `condition`) がこの要求を SQL の直接呼び出しに変換できる場合、デザイン時に警告メッセージがスローされます。 このメッセージは、`WHERE` 関数の代わりに [FILTER](er-functions-list-filter.md) 関数が使用された場合にパフォーマンスが向上する可能性があることをユーザーに通知します。

## <a name="example-1"></a>例 1

**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `WHERE (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。

## <a name="example-2"></a>例 2

*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `WHERE( DS, DS.Value = "B")` は、**値** フィールドにテキスト **"B"** を含む 1 つのレコードのみのリストを返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
