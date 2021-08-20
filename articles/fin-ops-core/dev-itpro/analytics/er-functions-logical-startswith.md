---
title: STARTSWITH ER 関数
description: このトピックでは、STARTSWITH 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: b378f501ccf812cfa0ae09e7cfbfdcf4c8a24ab8747b8ffe6044769df14a3057
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762227"
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
