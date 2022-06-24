---
title: MOD_97 ER 関数
description: この記事では、MOD_97 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: f57b55a9c4182b411e098ebce2f36b78ef03b6f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898436"
---
# <a name="mod_97-er-function"></a>MOD_97 ER 関数

[!include [banner](../includes/banner.md)]

この `MOD_97` 関数は、指定された請求書番号の桁数に基づいて、MOD97 式として債権者参照を表す *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>引数

`invoice number digits`: *文字列*

請求書番号の桁数を表すテキスト値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`MOD_97 ("VEND-200002")` は、**"20000285"** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]