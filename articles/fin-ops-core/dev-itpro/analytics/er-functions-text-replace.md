---
title: REPLACE ER 関数
description: このトピックでは、REPLACE 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916870"
---
# <a name="REPLACE">REPLACE ER 関数</a>

[!include [banner](../includes/banner.md)]

`REPLACE` 関数は、そのすべてまたはその一部が別の文字列に置換した後、*文字列*値として指定されたテキストの文字列を返します。

## <a name="syntax"></a>構文

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*文字列*型のデータ ソースの有効なパス。

`pattern`: *文字列*

`regular expression flag` 引数が **FALSE** の場合、この引数には置換する必要のあるテキストが含まれます。

`regular expression flag` 引数が **TRUE** の場合、この引数には検索パターンと置換後のテキストの両方を定義する正規表現が含まれます。

`replacement`: *文字列*

`regular expression flag` 引数が **FALSE** の場合、この引数には置換として使用するテキストが含まれます。

`regular expression flag` 引数が **TRUE** の場合、この引数は使用されません。

`regular expression flag`: *ブール値*

正規表現を使用して置換を行うかどうかを示す*ブール*値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

`regular expression flag` 引数が **TRUE** の場合、この関数は `pattern` 引数で指定された正規表現を適用することで変更された後、指定された文字列を返します。 正規表現は、置換する必要のある文字を検索するために使用されます。

`regular expression flag` 引数が **FALSE** の場合、この関数は [TRANSLATE](er-functions-text-translate.md) と同様に動作します。 `replacement` 引数で指定された文字は、見つかった文字を置換るために使用されます。 

## <a name="example-1"></a>例 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` は、すべての数値以外の記号を削除する正規表現を適用し、**"19234564971"** を返します。 

## <a name="example-2"></a>例 2

`REPLACE ("abcdef", "cd", "GH", false)` は、パターン **"cd"** を文字列 **"GH"** に置き換え、**"abGHef"** 返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
