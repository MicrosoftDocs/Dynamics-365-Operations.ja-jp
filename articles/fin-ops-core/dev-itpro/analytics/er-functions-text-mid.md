---
title: MID ER 関数
description: このトピックでは、MID 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915605"
---
# <a name="MID">MID ER 関数</a>

[!include [banner](../includes/banner.md)]

`MID` 関数は、指定された位置から始まる指定された文字列から、指定された数の文字を表す*文字列*値を返します。

## <a name="syntax"></a>構文

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>引数

`text`: *文字列*

文字を返すテキストを指定する*文字列*値。

`starting position`: *整数*

指定されたテキストから返す必要がある最初の文字の位置を指定する*整数*値。

`number of characters`: *整数*

指定された開始位置から始め、返す必要がある文字の数を指定する*整数*値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

`starting position` 引数の値が 0 (ゼロ) よりも小さい場合は、指定された文字列の最初の位置から返される文字がカウントされます。

`starting position` 引数の値が指定した文字列の長さを超える場合は、空の文字列が返されます。

## <a name="example"></a>例

`MID ("Sample", 2, 3)` は、**"amp"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)
