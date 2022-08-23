---
title: REPEAT ER 関数
description: この記事では、REPEAT 電子申告 (ER) 関数の使用方法について説明します。
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220692"
---
# <a name="repeat-er-function"></a>REPEAT ER 関数

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`REPEAT` 関数は、指定された入力に一致する値を持つフィールドを含むレコードを作成します。 次に、指定された回数だけ繰り返されるレコードの新しい *レコード リスト* を返します。

## <a name="syntax"></a>構文

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>引数

`item`: サポートされている [プリミティブ](er-formula-supported-data-types-primitive.md) データ型または [複合](er-formula-supported-data-types-composite.md) データ型

繰り返す値。

`number`: *整数*

繰り返しの回数。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

返される繰り返しレコードのリストには、以下のフィールドが表示されます:

- 指定値 (`Item` フィールド)
- 現在のレコード インデックス (`Number` フィールド)

> [!NOTE]
> この関数では 1 から始まる番号付けが使用されるため、結果リストの最初のレコードの `Number` フィールドの値は **1** になります。

この関数を使用して既存のデータを乗算すると、[Regression suite automation tool (RSAT)](../perf-test/rsat/rsat-overview.md) による [電子申告 (ER)](general-electronic-reporting.md) ソリューションのパフォーマンスやボリューム テストを実行することができます。

## <a name="example"></a>例

ER 形式の実行が開始される前に、実行時にダイアログ ボックスのデータ 入力フィールドで指定した数だけ `Party` XML 要素を含む XML 形式のドキュメントを生成します。

以下の図は、ER [形式](er-overview-components.md#format-component) を示します。 この形式では、ただ一つの `Party` XML 要素が追加され、ただ一つの関係者のプロパティが公開されます。

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

次の図は、以下の構成済データ ソースを示しています:

- ただ一つの関係者を表す `Party` データ ソース。 `Party.Value` フィールドは、ただ一つのテキスト値を公開するために使用されます。
- `NumberOfRepeats` [データ ソース](er-user-input-parameter-data-sources.md) は、実行時にダイアログ ボックスでデータ入力フィールドを提供するために使用され、生成されるドキュメントに入力する関係者の数を指定できます。
- `NumberOfRepeats` データ ソースで指定した回数だけ `Party` レコードを繰り返す `Party2` データ ソース。

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

次の図は、XML 形式の出力を生成するために作成される編集可能な ER 形式のデータ バインドを示しています。 この出力では、個々の関係者が列挙型ノードとして表示されます。

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

次の図は、設計された形式が実行され、`NumberOfRepeats` データ ソースの値が **5** と指定された場合の結果を示しています。

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>追加リソース

[リスト関数](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
