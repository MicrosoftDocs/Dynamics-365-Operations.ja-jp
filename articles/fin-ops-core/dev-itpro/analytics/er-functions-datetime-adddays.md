---
title: ADDDAYS ER 関数
description: このトピックでは、ADDDAYS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688446"
---
# <a name="adddays-er-function"></a>ADDDAYS ER 関数

[!include [banner](../includes/banner.md)]

`ADDDAYS` 関数は、指定された開始日前後の指定された日数の *日時* 値を計算します。

## <a name="syntax"></a>構文

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>引数

`datetime`: *日時*

開始日を表す日付/時刻値。

`days`: *整数*

`datetime` の前後の日数。

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="usage-notes"></a>使用上の注意

`days` の正の値は、未来の日付になります。 負の値は、過去の日付になります。

## <a name="example-1"></a>例 1

`ADDDAYS (NOW(), 7)` は、7 日後の日付と時刻を返します。

## <a name="example-2"></a>例 2

`ADDDAYS (NOW(), -3)` は、3 日前の日付と時刻を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]