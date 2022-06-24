---
title: ISVALIDCHARACTERISO7064 ER 関数
description: この記事では、ISVALIDCHARACTERISO7064 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 43da66e79bd8fbeecf5a04283574077600552a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908477"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER 関数

[!include [banner](../includes/banner.md)]

`ISVALIDCHARACTERISO7064` 機能は、指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。

## <a name="syntax"></a>構文

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>引数

`text`: *文字列*

IBAN を表すテキスト値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` は、**TRUE** を返します。 

`ISVALIDCHARACTERISO7064 ("AT61")` は、**FALSE** 返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]