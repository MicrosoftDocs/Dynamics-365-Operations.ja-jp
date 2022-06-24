---
title: NULLDATE ER 関数
description: この記事では、NULLDATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 7d1f0535796da096253dbd3ed55e9407cc9150f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870409"
---
# <a name="nulldate-er-function"></a>NULLDATE ER 関数

[!include [banner](../includes/banner.md)]

`NULLDATE` 関数は、**null** の日付 (1900 年 1 月 1 日) を表す *日付* 値を返します。

## <a name="syntax"></a>構文

```vb
NULLDATE () as 
```

## <a name="return-values"></a>戻り値

*日付*

結果日付値。

## <a name="example-1"></a>例 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` は、指定されたカスタム形式に基づいて、**null** の日付 1900 年 1 月 1 日を **"1900-01-01"** として返します。

## <a name="example-2"></a>例 2

式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` は、**DocumentDate** フィールドの値が **null** の日付と同じである場合に **True** を返します。 この例では、**請求書** は、**Finance/Table records** タイプの電子申告 (ER) データ ソースで、CustInvoiceJour テーブルを参照します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]