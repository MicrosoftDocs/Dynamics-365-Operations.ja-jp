---
title: TRANSLATE ER 関数
description: このトピックでは、TRANSLATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040920"
---
# <a name="TRANSLATE">TRANSLATE ER 関数</a>

[!include [banner](../includes/banner.md)]

`TRANSLATE` 関数は、そのすべてまたはその一部が別の文字列に置換した後、*文字列*値として指定されたテキストの文字列を返します。

## <a name="syntax"></a>構文

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>引数

`text`: *文字列*

*文字列*型のデータ ソースの有効なパス。

`pattern`: *文字列*

置換が必要なテキスト。

`replacement`: *文字列*

置換として使用するテキスト。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`TRANSLATE ("abcdef", "cd", "GH")` は、パターン **"cd"** を文字列 **"GH"** に置き換え、**"abGHef"** 返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
