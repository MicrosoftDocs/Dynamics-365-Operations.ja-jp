---
title: GUIDVALUE ER 関数
description: この記事では、GUIDVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: f3899d983f7c790ff2e3dc74dd91c44fc54e44d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898743"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER 関数

[!include [banner](../includes/banner.md)]

`GUIDVALUE` 関数は、指定された *文字列* 型の入力を *GUID* 型のデータ品目に変換します。

## <a name="syntax"></a>構文

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列* 型のデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*GUID*

結果のグローバル一意識別子 (GUID) 値。

## <a name="usage-notes"></a>使用上の注意

逆方向に変換を行うには (つまり、*GUID* データ型の指定された入力を *文字列* データ型のデータ項目に変換するには)、[TEXT](er-functions-text-text.md) 関数を使用します。

## <a name="example"></a>例

モデル マッピングでは、次のデータ ソースを定義します。

- `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` 式を含む *計算済フィールド* タイプの **myID** データ ソース
- UserInfo テーブルを参照する *テーブル レコード* 型の **ユーザー** データ ソース

その後、`FILTER (Users, Users.objectId = myID)` などの式を使用して、*GUID* データ型の **Objectld** フィールドで UserInfo テーブルをフィルタ処理できます。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]