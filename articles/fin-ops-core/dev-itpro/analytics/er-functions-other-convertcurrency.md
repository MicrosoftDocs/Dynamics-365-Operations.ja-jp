---
title: CONVERTCURRENCY ER 関数
description: このトピックでは、CONVERTCURRENCY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: bf972c6c2cc798811a9fb3bd3a355ac6ffca5a60
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915950"
---
# <a name="CONVERTCURRENCY">CONVERTCURRENCY ER 関数</a>

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY` 関数は、特定の日付で指定された会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換した結果を表す、*実数*値を返します。

## <a name="syntax"></a>構文

```
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>引数

`amount`: *整数*または*実数*

変換が必要な金額を表す数値。

`source currency`: *文字列*

換算元の通貨のコード

`target currency`: *文字列*

換算先の通貨のコード

`date`: *日付*

変換の為替レートを決定するために使用される日付を表す*日付*値。

`company`: *文字列*

変換に使用される設定を提供する会社のコードを表す*文字列*値。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="example"></a>例

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` は、**DEMF** 会社の設定に基づいて現在のセッションの日付の 1 ユーロに相当する額を米ドルで返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)
