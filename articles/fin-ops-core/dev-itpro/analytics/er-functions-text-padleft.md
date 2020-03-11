---
title: PADLEFT ER 関数
description: このトピックでは、PADLEFT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040966"
---
# <a name="PADLEFT">PADLEFT ER 関数</a>

[!include [banner](../includes/banner.md)]

`PADLEFT` 関数は、指定の文字列から始まる指定の文字でパディングされた指定の長さの*文字列*値を返します。

## <a name="syntax"></a>構文

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>引数

`text`: *文字列*

オリジナルのテキストを表す*文字列*値。

`length`: *整数*

パディングされた文字列の最終文字数を表す*整数*値。

`padding chars`: *文字列*

パディングに使用する文字。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`PADLEFT ("1234", 10, "`&nbsp;`")` は、テキスト文字列の **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
