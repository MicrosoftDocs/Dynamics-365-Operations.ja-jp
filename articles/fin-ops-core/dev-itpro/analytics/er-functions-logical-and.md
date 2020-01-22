---
title: AND ER 関数
description: このトピックでは、AND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917169"
---
# <a name="AND">AND ER 関数</a>

[!include [banner](../includes/banner.md)]

`AND` 関数は、指定したすべての条件が true である場合、**TRUE** の*ブール*値を返します。 それ以外の場合は、**FALSE** の*ブール*値が返されます。

## <a name="syntax"></a>構文

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>引数

`condition 1`: *ブール値*

テストする必要がある有効な条件式。 この引数は必須です。

`condition N`: *ブール値*

テストする必要がある有効な条件式。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*ブール型*

結果*ブール*値。

## <a name="usage-notes"></a>使用上の注意

論理関数の引数では、データ ソース参照、数値とテキストの値、ブール値、比較演算子、およびその他の電子申告 (ER) 関数を使用できます。 ただし、すべての引数は **TRUE** または **FALSE** の*ブール*値に評価する必要があります。

## <a name="example"></a>例

`AND (1=1, "a"="a")` は、**TRUE** を返します。

`AND (1=2, "a"="a")` は、**FALSE** 返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)
