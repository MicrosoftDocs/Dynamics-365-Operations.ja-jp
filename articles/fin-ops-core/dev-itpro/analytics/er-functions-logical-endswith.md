---
title: ENDSWITH ER 関数
description: このトピックでは、ENDSWITH 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 1155bb5446f0370d9a5c4b035a767aaeb1d46ee1
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048897"
---
# <a name="endswith-er-function"></a>ENDSWITH ER 関数

[!include [banner](../includes/banner.md)]

`ENDSWITH` 関数は、指定された入力が指定されたテキストで終了するかどうかを決定します。 指定された入力が指定されたテキストで終了する場合、 関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。

## <a name="syntax"></a>構文

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列* 型または文字列定数のデータ ソースの項目の有効なパスで、2 番目の引数で終わる可能性がある値です。

`start text`: *文字列*

*文字列* データ型または文字列定数のデータ ソースの項目の有効なパスで、1 番目の引数で終わる可能性がある値です。

## <a name="return-values"></a>戻り値

*ブール値*

結果 *ブール* 値。

## <a name="usage-notes"></a>使用上の注意

この機能は、[Microsoft Dataverse](/power-platform/admin/data-integrator) にアクセスするための適切なマッピングが [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) で構成されている場合にのみ、[FILTER](er-functions-list-filter.md) 関数の条件式を指定をするのに使用できます。 それ以外の場合は、設計時に例外がスローされます。 受信するメッセージは、効率を向上させるために、`FILTER` 関数の代わりに [WHERE](er-functions-list-where.md) 関数を使用することを推奨しています。

## <a name="example-1"></a>例 1

`ENDSWITH ("abc", "d")` 式は **FALSE** を返し、`ENDSWITH ("abc", "C")` 式は **TRUE** を返します。

## <a name="example-2"></a>例 2

**モデル** データ ソースの **アドレス** フィールドの値が文字列 **USA** で始まる場合、`ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` 式は **TRUE** を返します。 それ以外の場合、**FALSE** を返します。

## <a name="additional-resources"></a>追加リソース

[論理関数](er-functions-category-logical.md)
