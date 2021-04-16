---
title: GUIDVALUE ER 関数
description: このトピックでは、GUIDVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746390"
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