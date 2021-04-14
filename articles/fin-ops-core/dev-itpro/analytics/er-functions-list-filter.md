---
title: FILTER ER 関数
description: このトピックでは、FILTER 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746606"
---
# <a name="filter-er-function"></a>FILTER ER 関数

[!include [banner](../includes/banner.md)]

`FILTER` 関数は、クエリが変更された後、指定されたリストを *レコード リスト* 値として返し、指定された条件でフィルタリングします。

## <a name="syntax"></a>構文

```vb
FILTER (list, condition)
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

この関数は [WHERE](er-functions-list-where.md) 関数とは異なります。指定された条件がデータベース レベルで *テーブル レコード* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。 テーブルおよび関係を使用して、リストと条件を定義することができます。

この関数に対して構成されている引数 (`list` および `condition`) のいずれかまたは両方がこの要求を SQL の直接呼び出しに変換できない場合、デザイン時に例外がスローされます。 この例外は、`list` または `condition` のいずれもデータベースのクエリに使用できないことをユーザーに通知します。

## <a name="example-1"></a>例 1

**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `FILTER (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。

## <a name="example-2"></a>例 2

**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成され、**parmVendorBankGroup** が *文字列* データ型の値を返す ER データ ソースとして構成されている場合、式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` が特定の銀行グループに属する仕入先のみの一覧を返します。

## <a name="example-3"></a>例 3

`SPLIT ("A,B,C", ",")` 式を含む *計算済フィールド* タイプの **DS** データ ソースを入力します。 次に、別の式 `FILTER( DS, DS.Value = "B")` を入力します。 この式を ER フォーミュラ デザイナーに保存しようとすると、次の例外がスローされます。「検証エラー : FILTER 関数のリスト式はクエリ可能ではありません。」

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]