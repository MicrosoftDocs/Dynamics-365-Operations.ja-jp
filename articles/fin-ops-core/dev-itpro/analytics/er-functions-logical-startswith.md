---
title: STARTSWITH ER 関数
description: この記事では、STARTSWITH 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287221"
---
# <a name="startswith-er-function"></a>STARTSWITH ER 関数

[!include [banner](../includes/banner.md)]

`STARTSWITH` 関数は、指定された入力が指定されたテキストで始まるかどうかを決定します。 指定された入力が指定されたテキストで始まる場合、 関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。

## <a name="syntax"></a>構文

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>引数

`input`: *文字列*

*文字列* 型または文字列定数のデータ ソースの項目の有効なパスで、2 番目の引数で始まる可能性がある値です。

`start text`: *文字列*

*文字列* データ型または文字列定数のデータ ソースの項目の有効なパスで、1 番目の引数で始まる可能性がある値です。

## <a name="return-values"></a>戻り値

*ブール値*

結果 *ブール* 値。

## <a name="usage-notes"></a>使用上の注意

この機能は、[Microsoft Dataverse](/power-platform/admin/data-integrator) にアクセスするための適切なマッピングが [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) で構成されている場合にのみ、[FILTER](er-functions-list-filter.md) 関数の条件式を指定をするのに使用できます。 それ以外の場合は、設計時に例外がスローされます。 受信するメッセージは、効率を向上させるために、`FILTER` 関数の代わりに [WHERE](er-functions-list-where.md) 関数を使用することを推奨しています。

## <a name="example-1"></a>例 1

`STARTSWITH ("abc", "d")` 式は **FALSE** を返し、`STARTSWITH ("abc", "A")` 式は **TRUE** を返します。

## <a name="example-2"></a>例 2

**モデル** データ ソースの **アドレス** フィールドの値が文字列 **123 Coffee Street** で始まる場合、`STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` 式は **TRUE** を返します。 それ以外の場合、**FALSE** を返します。

## <a name="additional-resources"></a>追加リソース

[論理関数](er-functions-category-logical.md)
