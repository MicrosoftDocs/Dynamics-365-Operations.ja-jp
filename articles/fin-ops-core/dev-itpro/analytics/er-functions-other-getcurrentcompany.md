---
title: GETCURRENTCOMPANY ER 機能
description: この記事では、GETCURRENTCOMPANY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 06d552a0e8241d416fc49c4377b02f90fdf63d29
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872745"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER 機能

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY` 機能は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`GETCURRENTCOMPANY ()` は、**Contoso エンターテインメント システム USA** 会社にサイン インしているユーザーに対して **USMF** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]