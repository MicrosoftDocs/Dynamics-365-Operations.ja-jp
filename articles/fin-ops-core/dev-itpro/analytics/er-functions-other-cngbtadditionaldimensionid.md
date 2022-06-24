---
title: CN_GBT_ADDITIONALDIMENSIONID ER 関数
description: この記事では、CN_GBT_ADDITIONALDIMENSIONID 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 80ce6846cd4687c2a12815ef0da1e1684c57d1f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898772"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER 関数

[!include [banner](../includes/banner.md)]

`CN_GBT_ADDITIONALDIMENSIONID` 関数は、指定された文字列から取得された単一の財務分析コード ID を表す *文字列* 値を返します。 指定された文字列は、ID のコンマ区切りのリストとしてすべての分析コードを示します。

## <a name="syntax"></a>構文

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>引数

`text`: *文字列*

ID のコンマ区切りのリストとしてすべての分析コードを示す *文字列* 値。

`number`: 整数

指定された文字列で要求された分析コードの順序コードを定義する *整数* 値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` は、**"CC"** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]