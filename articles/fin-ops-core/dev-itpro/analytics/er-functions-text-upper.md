---
title: UPPER ER 関数
description: このトピックでは、UPPER 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749144"
---
# <a name="upper-er-function"></a>UPPER ER 関数

[!include [banner](../includes/banner.md)]

`UPPER` 関数は、大文字に変換した後の *文字列* 値として指定されたテキスト返します。

## <a name="syntax"></a>構文

```vb
UPPER (text )
```

## <a name="arguments"></a>引数

`text`: *文字列*

*文字列* 型のデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

`UPPER ("Sample")` は、**"SAMPLE"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]