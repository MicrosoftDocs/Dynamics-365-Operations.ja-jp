---
title: JSONVALUE ER 関数
description: このトピックでは、JSONVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746366"
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

JSON データのスカラー値の識別子。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

**JsonField** データ ソースは、JSON 形式の次のデータを含みます: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。 この場合、`JSONVALUE (JsonField, "BuildNumber")` 式は *文字列* データ型の次の値を返します: **"7.3.1234.1"**。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]