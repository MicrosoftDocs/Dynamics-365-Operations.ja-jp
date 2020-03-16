---
title: VALUEIN ER 関数
description: このトピックでは、VALUEIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041702"
---
# <a name="VALUEIN">VALUEIN ER 関数</a>

[!include [banner](../includes/banner.md)]

`VALUEIN` 関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。 指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の*ブール*値を返します。 それ以外の場合は、**FALSE** の*ブール*値が返されます。

## <a name="syntax"></a>構文

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>引数

`input`: *フィールド*

*レコード リスト* タイプのデータ ソースの項目の有効なパス。 この項目の値は一致します。

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`list item expression`: *ブール値*

照合に使用される指定されたリストの単一のフィールドを指し示すか、そのフィールドを含む有効な条件式。

## <a name="return-values"></a>戻り値

*ブール型*

結果*ブール*値。

## <a name="usage-notes"></a>使用上の注意

一般に、`VALUEIN` 関数は一連の **OR** 条件に変換されます。

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

場合によっては、`EXISTS JOIN` オペレーターを使用してデータベース SQL ステートメントに変換されます。

## <a name="example-1"></a>例 1

モデル マッピングで、*計算済フィールド* タイプの**リスト** データ ソースを定義します。 このデータ ソースには、式 `SPLIT ("a,b,c", ",")` が含まれています。

データ ソースが呼び出されると、`VALUEIN ("B", List, List.Value)` 式として構成されている場合は、**TRUE** を返します。 この場合、`VALUEIN` 関数は次の一連の条件に変換されます。`("B" = "b")` が **TRUE** と等しい場合、`(("B" = "a") or ("B" = "b") or ("B" = "c"))`。

データ ソースが呼び出されると、`VALUEIN ("B", List, LEFT(List.Value, 0))` 式として構成されている場合は、**FALSE** を返します。 この場合、`VALUEIN` 関数は次の一連の条件に変換されます。 **TRUE** と等しくない `("B" = "")`。

このような条件のテキストの文字数の上限は 32,768 文字です。 したがって、実行時に制限を超える可能性があるデータ ソースを作成しないでください。 制限を超過した場合は、アプリケーションは実行を停止し、例外がスローされます。 たとえば、この状況は、データ ソースが `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` として構成され、**List1** および **List2** リストに大量のレコードが含まれているときに生じます。

場合によっては、`VALUEIN` 関数は `EXISTS JOIN` オペレーターを使用することでデータベース ステートメントに変換されます。 この動作は、[FILTER](er-functions-list-filter.md) 関数が使用され、次の条件が満たされているときに発生します。

- **ASK FOR QUERY** オプションは、レコードのリストを参照する `VALUEIN` 関数のデータ ソースに対してオフになっています。 このデータ ソースには実行時に適用される追加の条件はありません。
- 入れ子になった式は、レコードのリストを参照する `VALUEIN` 関数のデータ ソース用に構成されません。
- `VALUEIN` 関数のリスト項目は、指定されたデータ ソースの式またメソッドではなく、指定されたデータ ソースのフィールドを参照します。

この例の前半で説明した [WHERE](er-functions-list-where.md) 関数の代わりにこのオプションを使用することを検討してください。

## <a name="example-2"></a>例 2

モデル マッピングでは、次のデータ ソースを定義します。

- *テーブル レコード* タイプの **In** データ ソース。 このデータ ソースは、イントラスタット テーブルを参照します。
- *テーブル レコード* タイプの**ポート** データ ソース。 このデータ ソースは、IntrastatPort テーブルを参照します。

`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` 式として構成されたデータ ソースが呼び出されると、次の SQL ステートメントが生成され、イントラスタット テーブルのフィルターされたレコードを返します。

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId** フィールドの場合、`IN` 演算子を使用して最終的な SQL ステートメントが生成されます。

## <a name="example-3"></a>例 3

モデル マッピングでは、次のデータ ソースを定義します。

- *計算済フィールド* タイプの **Le** データ ソース。 このデータ ソースには、式 `SPLIT ("DEMF,GBSI,USMF", ",")` が含まれています。
- *テーブル レコード* タイプの **In** データ ソース。 このデータ ソースはイントラスタット テーブルを参照し、**会社間**オプションが有効になっています。

`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` 式として構成されたデータ ソースが呼び出されると、最終的な SQL ステートメントには次の条件が含まれています。

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)
