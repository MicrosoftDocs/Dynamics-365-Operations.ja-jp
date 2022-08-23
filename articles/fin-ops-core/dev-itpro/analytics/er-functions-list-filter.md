---
title: FILTER ER 関数
description: この記事では、FILTER 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/14/2021
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
ms.openlocfilehash: cfaf76daa8118942c3650e6b39c853434a20ee30
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272591"
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

## <a name="usage-notes"></a><a name="usage-notes"></a>使用上の注意

この関数は [WHERE](er-functions-list-where.md) 関数とは異なります。指定された条件がデータベース レベルで *テーブル レコード* タイプの任意の電子申告 (ER) データ ソースに適用されるためです。 テーブルおよび関係を使用して、リストと条件を定義することができます。

この関数に対して構成されている引数 (`list` および `condition`) のいずれかまたは両方がこの要求を SQL の直接呼び出しに変換できない場合、デザイン時に例外がスローされます。 この例外は、`list` または `condition` のいずれもデータベースのクエリに使用できないことをユーザーに通知します。

> [!NOTE]
> `FILTER` 関数は、[`VALUEIN`](er-functions-logical-valuein.md)  関数で選択条件を指定した場合、`WHERE` 関数とは異なる動作をします。
> 
> - `VALUEIN` 関数が `WHERE` 関数のスコープ内で使用されており、`VALUEIN` の 2 番目の引数がレコードを返さないデータソースを参照している場合、`VALUEIN` が返すブール値の *[False](er-formula-supported-data-types-primitive.md#boolean)* 値が考慮されます。 そのため、**VendGroups** データソースがベンダーグループのレコードを返さない場合、式 `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` は仕入先のレコードを返しません。
> - `VALUEIN` 関数が `FILTER` 関数のスコープ内で使用されており、`VALUEIN` の 2 番目の引数がレコードを返さないデータソースを参照している場合、`VALUEIN` が返すブール値の *[False](er-formula-supported-data-types-primitive.md#boolean)* 値が無視されます。 したがって、**VendGroups** データソースが仕入先グループのレコードを返さない場合でも、式 `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` は **Vendors** データソースのすべての仕入先レコードを返します。

## <a name="example-1"></a>例 1

**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成されている場合、式 `FILTER (Vendors, Vendors.VendGroup = "40")` は仕入先グループ 40 に属している仕入先のみのリストを返します。

## <a name="example-2"></a>例 2

**仕入先** が VendTable テーブルを参照する ER データ ソースとして構成され、**parmVendorBankGroup** が *文字列* データ型の値を返す ER データ ソースとして構成されている場合、式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` が特定の銀行グループに属する仕入先のみの一覧を返します。

## <a name="example-3"></a>例 3

`SPLIT ("A,B,C", ",")` 式を含む *計算済フィールド* タイプの **DS** データ ソースを入力します。 次に、別の式 `FILTER( DS, DS.Value = "B")` を入力します。 この式を ER フォーミュラ デザイナーに保存しようとすると、次の例外がスローされます。「検証エラー : FILTER 関数のリスト式はクエリ可能ではありません。」

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
