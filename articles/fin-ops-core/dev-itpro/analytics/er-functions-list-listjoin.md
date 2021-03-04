---
title: LISTJOIN ER 関数
description: このトピックでは、LISTJOIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682246"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER 関数

[!include [banner](../includes/banner.md)]

この `LISTJOIN` 関数は、指定された引数から作成された新しい結合リストを表す *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>引数

`list 1`: *レコード リスト*

*レコード リスト* データ タイプのデータ ソースの参照。 この引数は必須です。

`list N`: *レコード リスト*

*レコード リスト* データ タイプのデータ ソースの参照。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成されたリストの構造には、引数で参照されるすべてのレコード リストの構造に存在するフィールドのみが含まれます。

## <a name="example"></a>例

`Container` タイプのデータ ソース **レコード 1** を入力します。 このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:

- **コード**: このフィールドには、`String` タイプの値を返す式が含まれています。
- **量**: このフィールドには、`Real` タイプの値を返す式が含まれています。

次に、`Container` タイプのデータ ソース **レコード 2** を入力します。 このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:

- **量**: このフィールドには、`Real` タイプの値を返す式が含まれています。
- **IsValid**: このフィールドには、`Boolean` タイプの値を返す式が含まれています。

![ER モデル マッピング デザイナーのページ](./media/er-functions-list-listjoin-image1.gif)

この場合、式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` は 2 つのレコードを含む新しいリストを返します。

![2 つのレコードを持つ ER モデル マッピング デザイナー ページ](./media/er-functions-list-listjoin-image2.gif)

このフィールドは、呼び出された関数のすべての引数に表示される唯一のフィールドであるため、`Real` タイプの 1 つの **量** フィールドで構成されます。

![ER モデル マッピング デザイナー ページの量フィールド](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>追加リソース

[リスト関数](er-functions-category-list.md)

[実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]