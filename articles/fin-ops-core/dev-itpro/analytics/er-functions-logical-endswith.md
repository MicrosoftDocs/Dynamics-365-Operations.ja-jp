---
title: ENDSWITH ER 関数
description: この記事では、ENDSWITH 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 2608593238e5b2f738b452fb042837238f17e44e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271616"
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
