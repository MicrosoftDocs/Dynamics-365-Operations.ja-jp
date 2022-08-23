---
title: NULLDATE ER 関数
description: この記事では、NULLDATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272655"
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
