---
title: ISEMPTY ER 関数
description: この記事では、ISEMPTY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 1d8c9a2195afbc76bc00f31778d087268b98279f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845528"
---
# <a name="isempty-er-function"></a>ISEMPTY ER 関数

[!include [banner](../includes/banner.md)]

`ISEMPTY` 関数は、指定したリストにレコードが含まれていない場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。

## <a name="syntax"></a>構文

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*ブール型*

結果 *ブール* 値。

## <a name="example-1"></a>例 1

*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `ISEMPTY(DS)` は **FALSE** を返します。

## <a name="example-2"></a>例 2

式 `ISEMPTY (SPLIT ("",1))` は **TRUE** を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]