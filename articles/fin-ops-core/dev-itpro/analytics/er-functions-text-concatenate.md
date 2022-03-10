---
title: CONCATENATE ER 機能
description: このトピックでは、CONCATENATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 1507e1b8a31ed45e7c540e4e2ff31b79e8de3b866ffbace9de17d7b3e169e877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762503"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER 機能

[!include [banner](../includes/banner.md)]

`CONCATENATE` 関数は、一つの文字列に結合された後、*文字列* 値として指定されたすべてのテキスト文字列を返します。

## <a name="syntax"></a>構文

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>引数

`text 1`: *文字列*

*文字列* データ タイプのデータ ソースの参照。 この引数は必須です。

`text N`: *文字列*

*文字列* データ タイプのデータ ソースの参照。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`CONCATENATE ("abc", "def")`" は、**abcdef" を返します**。

## <a name="usage-notes"></a>使用上の注意

式 `"abc" & "def"` も、**"abcdef"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]