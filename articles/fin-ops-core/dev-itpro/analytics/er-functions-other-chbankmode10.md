---
title: CH_BANK_MOD_10 ER 関数
description: この記事では、CH_BANK_MOD_10 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 494aa335ef170db0cd2f61a1d33391de474cd4bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885030"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER 関数

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10` 関数は、指定された請求書番号の桁数に基づいて、MOD10 式として債権者参照を表す *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>引数

`invoice number digits`: *文字列*

請求書番号の桁数を表すテキスト値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`CH_BANK_MOD_10 ("VEND-200002")` は、**3** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]