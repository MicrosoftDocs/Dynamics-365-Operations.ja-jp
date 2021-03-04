---
title: TRANSLATE ER 関数
description: このトピックでは、TRANSLATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685306"
---
# <a name="translate-er-function"></a>TRANSLATE ER 関数

[!include [banner](../includes/banner.md)]

`TRANSLATE` 関数は、指定されたテキストを別の提供されたセットの文字に置換した結果を含む *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*文字列* 型のデータ ソースの有効なパス。

`pattern`: *文字列*

置換が必要なテキスト。

`replacement`: *文字列*

置換として使用するテキスト。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

`TRANSLATE` 関数は一度に 1 文字ずつ置き換えます。 この関数は、`text` 引数の最初の文字を `pattern` 引数の最初の文字に、次に 2 番目の文字に置き換え、完了するまで同じフローに従います。 引数 `text` と `pattern` の文字が一致すると、`pattern` 引数の文字と同じ位置にある `replacement` 引数の文字に置き換えられます。 文字が `pattern` 引数に複数回出現する場合は、この文字の最初の出現に対応する `replacement` 引数マッピングが使用されます。

## <a name="example-1"></a>例 1

`TRANSLATE ("abcdef", "cd", "GH")` は、次の理由により、指定された **"abcdef"** テキストの **"c"** 文字を `replacement` テキストの **"G"** 文字に置き換えます:
-   **"c"** 文字は、最初の位置の `pattern` テキストに表示されます。
-   `replacement` テキストの最初の位置には **"G"** 文字が含まれます。

## <a name="example-2"></a>例 2

`TRANSLATE ("abcdef", "ccd", "GH")` は、**"abGdef"** を返します。

## <a name="example-3"></a>例 3

`TRANSLATE ("abccba", "abc", "123")` は、**"123321"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]