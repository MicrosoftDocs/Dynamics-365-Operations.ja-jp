---
title: CONCATENATE ER 機能
description: この記事では、CONCATENATE 電子申告 (ER) 関数の使用方法についての情報を提供します
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267287"
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
