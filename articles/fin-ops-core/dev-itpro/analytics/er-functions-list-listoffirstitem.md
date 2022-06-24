---
title: LISTOFFIRSTITEM ER 関数
description: この記事では、LISTOFFIRSTITEM 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881162"
---
# <a name="listoffirstitem-er-function"></a>LISTOFFIRSTITEM ER 関数

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` 関数は、指定されたリストの最初のレコードのみで構成される *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="example"></a>例

式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` はテキスト値 **"A"** を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]