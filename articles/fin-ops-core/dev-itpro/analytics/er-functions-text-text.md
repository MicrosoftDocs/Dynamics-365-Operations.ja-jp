---
title: TEXT ER 関数
description: このトピックでは、TEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 38550b8b5181b49bcb8504129932f185ea95e038e38d4581bc3e0fa076f4fb50
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762455"
---
# <a name="text-er-function"></a>TEXT ER 関数

[!include [banner](../includes/banner.md)]

`TEXT` 関数は、現在のアプリケーション インスタンス のサーバー ロケール設定に従って、書式設定されるテキスト文字列に変換した後に、*文字列* 値として指定された数を返します。

## <a name="syntax"></a>構文

```vb
TEXT (number)
```

## <a name="arguments"></a>引数

`number`: *整数* または *実数*

テキスト文字列に変換する必要がある番号。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

*実数* 型の値では、文字列変換が小数点第 2 位に制限されます。

## <a name="example"></a>例

Microsoft Dynamics 365 Finance インスタンスのサーバー ロケールが **EN-US** で定義されている場合、`TEXT (NOW ())` は現在の財務セッション日付、2015 年 12 月 17 日、をテキスト文字列 **"12/17/2015 07:59:23 AM"** として返します。 `TEXT (1/3)` は、**"0.33"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]