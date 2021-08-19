---
title: SPLITLISTBYLIMIT ER 関数
description: このトピックでは、SPLITLISTBYLIMIT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 52351c131480119ce9fb98a75307ebf6026cb12b9977e8b4236d3a24ef6a140e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744437"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER 関数

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT` 関数は、指定されたリストを新しいサブリスト (バッチ) のリストに分割します。 各バッチのレコード数は動的に計算されます。 その後、関数は結果をバッチで構成された新しい *レコード リスト* 値として返します。

## <a name="syntax"></a>構文

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`limit value`: *整数* または *実数*

元のリストをバッチに分割するために使用される制限の最大値。

`limit source`: *フィールド*

指定されたリストの *整数* 型または *実数* 型のフィールドの有効なパス。 このフィールドの値は、合計が増加するステップを定義します。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

返されるバッチのリストには、次の要素が含まれます。

- **値**: *リスト*

    現在のバッチに属するレコードのリスト。

- **Batchnumber**: *整数*

    返されたリスト内の現在のバッチ数。

制限は、制限のソースが定義済み制限を超えると、元のリストの 1 つの項目に適用されません。

## <a name="example"></a>例

次の図は、電子申告 (ER) 形式を示しています。

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

次の図は、形式に対して使用されているデータ ソースを示します。

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

次の図は、形式が実行される際の結果を示します。 この場合、出力は、商品のフラット リストです。

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

次の図では、1 つのバッチに合計重量が 9 を超えない商品を含める必要がある場合、商品アイテムのリストをバッチに表示するために同じフォーマットが調整されています。

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

次の図は、調整された形式が実行される際の結果を示します。

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> 制限は、制限のソース (**重量**) の値 (**11**) が定義済みの制限 (**9**) を超えるため、元のリストの最後の項目に適用されません。 レポートの生成中にサブリストを無視するには、必要に応じて、 `WHERE` 関数または対応するフォーマット要素の **有効** 式のいずれかを使用します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]