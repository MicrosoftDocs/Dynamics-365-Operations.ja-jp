---
title: GUIDVALUE ER 関数
description: このトピックでは、GUIDVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915697"
---
# <a name="GUIDVALUE">GUIDVALUE ER 関数</a>

[!include [banner](../includes/banner.md)]

`GUIDVALUE` 関数は、指定された*文字列*型の入力を *GUID* 型のデータ品目に変換します。

## <a name="syntax"></a>構文

```
GUIDVALUE (input)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列*型のデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*GUID*

結果のグローバル一意識別子 (GUID) 値。

## <a name="usage-notes"></a>使用上の注意

逆方向に変換を行うには (つまり、*GUID* データ型の指定された入力を*文字列*データ型のデータ項目に変換するには)、[TEXT](er-functions-text-text.md) 関数を使用します。

## <a name="example"></a>例

モデル マッピングでは、次のデータ ソースを定義します。

- `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` 式を含む*計算済フィールド* タイプの **myID** データ ソース
- UserInfo テーブルを参照する*テーブル レコード*型の**ユーザー**データ ソース

その後、`FILTER (Users, Users.objectId = myID)` などの式を使用して、*GUID* データ型の **Objectld** フィールドで UserInfo テーブルをフィルタ処理できます。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
