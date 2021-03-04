---
title: TODAY ER 関数
description: このトピックでは、TODAY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: a93a9171456fb69e16c8104b0afb9ad485311b1a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683798"
---
# <a name="today-er-function"></a>TODAY ER 関数

[!include [banner](../includes/banner.md)]

`TODAY` 関数は、現在のアプリケーション サーバーの日付を表す *日付* 値を返します。

## <a name="syntax"></a>構文

```xpp
TODAY ()
```

## <a name="return-values"></a>戻り値

*日付*

結果日付値。

## <a name="example"></a>例

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]