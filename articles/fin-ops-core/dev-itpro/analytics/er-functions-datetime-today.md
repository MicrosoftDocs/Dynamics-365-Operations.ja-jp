---
title: TODAY ER 関数
description: このトピックでは、TODAY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 12c4489751e9e0c06d4b628e7c297eee472054369f7cfacee048622cbc39d074
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755829"
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