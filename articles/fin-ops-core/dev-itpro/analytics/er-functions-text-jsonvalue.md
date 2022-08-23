---
title: JSONVALUE ER 関数
description: この記事では、JSONVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 10/25/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267966"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER 関数

[!include [banner](../includes/banner.md)]

`JSONVALUE` 関数は指定した ID を持つスカラー値を抽出し、指定したパスでアクセスする JavaScript Object Notation (JSON) 形式で、データを解析します。 次に、抽出したスカラー値を *文字列* 値として返します。

## <a name="syntax"></a>構文

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>引数

`input`: *文字列*

JSON データを含む *文字列* 型のデータ ソースの有効なパス。

`path`: *文字列*

JSON データのスカラー値の識別子。 フォワード スラッシュ (/) を使用して、関連する JSON ノードの名前を切り離します。 角カッコ (\[\]) の表記を使用して、JSON 配列内の特定の値のインデックスを指定します。 このインデックスにはゼロ ベースの番号付けが使用されます。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example-1"></a>例 1

**JsonField** データ ソースは、JSON 形式の次のデータを含みます: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。 この場合、`JSONVALUE (JsonField, "BuildNumber")` 式は *文字列* データ型の次の値を返します: **"7.3.1234.1"**。

## <a name="example-2"></a>例 2

*計算済フィールド* タイプの **JsonField** データソースには、次の式が含まれています: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

以下のデータを JSON 形式で表現した [*文字列*](er-formula-supported-data-types-primitive.md#string) の値を返すように構成した式です。

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

この場合、式 `JSONVALUE(json, "workers/[1]/emails/[0]")` は次の *文字列* データ型の値を返します: `JohnS@Contoso.com`。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
