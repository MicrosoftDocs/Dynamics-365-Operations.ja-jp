---
title: NOW ER 関数
description: このトピックでは、NOW 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0c3cfefd36db44608f05225746704aa3fbe4fc2c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682368"
---
# <a name="now-er-function"></a>NOW ER 関数

[!include [banner](../includes/banner.md)]

`NOW` 関数は、現在のアプリケーション サーバーの日付と時刻を表す *DateTime* 値を返します。

## <a name="syntax"></a>構文

```vb
NOW ()
```

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="example"></a>例

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日時値 2015 年 12 月 24 日を **"24-12-2015"** として返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]