---
title: WHERE ER 関数
description: このトピックでは、WHERE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745500"
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