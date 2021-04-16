---
title: COUNT ER 関数
description: このトピックでは、COUNT 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746630"
---
# <a name="count-er-function"></a>COUNT ER 関数

[!include [banner](../includes/banner.md)]

`COUNT` 関数は、リストが空でない場合に、指定されたリストのレコード数を表す *整数* 値を返します。 リストが空の場合は、この関数は **0** (ゼロ) を返します。

## <a name="syntax"></a>構文

```vb
COUNT (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*整数*

結果数値。

## <a name="example"></a>例

この例で使用される `SPLIT` 関数は 2 つのレコードで構成されるリストを作成するため、`COUNT (SPLIT("abcd" , 3))` は、**2** を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]