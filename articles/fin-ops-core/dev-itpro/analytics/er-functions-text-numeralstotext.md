---
title: NUMERALSTOTEXT ER 機能
description: このトピックでは、NUMERALSTOTEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041013"
---
# <a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER 機能</a>

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT` 関数は、指定された言語で綴らた後 (つまりテキスト文字列に変換された)、*文字列*値として指定された数を返します。

## <a name="syntax"></a>構文

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>引数

`number`: *整数*または*実数*

綴りが必要な数を指定する数値。

`language`: *文字列*

言語コードを表す*文字列*値。

`currency`: *文字列*

通貨コードを表す*文字列*値。

`print currency name flag`: *ブール値*

綴られたテキストに通貨名を追加する必要があるかどうかを示す*ブール*値。

`decimal points`: *整数*

綴られたテキストを持つべき小数点以下の桁数を示す*整数*値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

言語コードはオプションです。 空の文字列として定義されている場合、実行中のコンテキストの言語コードが使用されます。 既定の言語コードは **EN-US** です。 実行中のコンテキストの言語コードは、実行されている電子申告 (ER) の**フォルダー**または**ファイル**要素で定義されます。

通貨コードはオプションです。 空の文字列として定義されている場合、実行中のコンテキストの会社通貨が使用されます。

> [!NOTE] 
> `print currency name flag` と `decimal points` 引数は、以下の言語コードについてのみ分析されます: **CS**、**ET**、**HU**、**LT**、**LV**、**PL**、および **RU**。 また、`print currency name flag` 引数は、通貨名の語形変化をサポートする国または地域のコンテキストを持つ会社に対してのみ分析されることにご注意ください。

## <a name="example-1"></a>例 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` は、**"One Thousand Two Hundred Thirty Four and 56"** を返します。

## <a name="example-2"></a>例 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` は、**"Sto dwadzieścia"** を返します。 

## <a name="example-3"></a>例 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` は、**"Сто двадцать евро 21 евроцент"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
