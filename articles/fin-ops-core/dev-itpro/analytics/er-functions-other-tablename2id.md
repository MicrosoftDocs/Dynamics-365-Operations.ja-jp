---
title: TABLENAME2ID ER 関数
description: この記事では、TABLENAME2ID 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886852"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER 関数

[!include [banner](../includes/banner.md)]

`TABLENAME2ID` 関数は、*整数* 値として指定されたテーブル名に対応するテーブル ID の数値表現を返します。

## <a name="syntax"></a>構文

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>引数

`text`: *文字列*

有効なテーブル名を表すテキスト値。

## <a name="return-values"></a>戻り値

*整数*

結果数値。

## <a name="usage-notes"></a>使用上の注意

この関数を実行すると、同じ会社名が使用されている場合でも、Microsoft Dynamics 365 Finance の異なるインスタンスに結果を得ることができます。

## <a name="example"></a>例

`TABLENAME2ID ("Intrastat")` は、**1510** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]