---
title: CHAR ER 関数
description: このトピックでは、CHAR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: e422ccc406e919b2191f4bccb1ac8198bba84b09e9f01f6971876e2c6507d6d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754369"
---
# <a name="char-er-function"></a>CHAR ER 関数

[!include [banner](../includes/banner.md)]

`CHAR` 関数は、指定された Unicode 番号で参照される単一の文字を表す *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
CHAR (number)
```

## <a name="arguments"></a>引数

`number`: *整数*

予想される単一文字に対応する番号。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

この機能を返す文字列は、親 **FILE** 形式の要素で選択したエンコードによって異なります。 サポートされているエンコードの一覧については、[エンコーディング クラス](/dotnet/api/system.text.encoding) で参照できます。

## <a name="example"></a>例

`CHAR (255)` は、**"ÿ"** を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]