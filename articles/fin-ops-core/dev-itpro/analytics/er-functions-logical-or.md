---
title: OR ER 関数
description: この記事では、OR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 99b5ee37af1ea1a69985fb79b762b31561334fd6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268089"
---
# <a name="or-er-function"></a>OR ER 関数

[!include [banner](../includes/banner.md)]

`OR` 関数は、指定したすべての条件が false である場合、**FALSE** の *ブール* 値を返します。 指定した任意の条件が true である場合、関数は **TRUE** の *ブール* 値を返します。

## <a name="syntax"></a>構文

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>引数

`condition 1`: *ブール値*

テストする必要がある有効な条件式。 この引数は必須です。

`condition N`: *ブール値*

テストする必要がある有効な条件式。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*ブール型*

結果 *ブール* 値。

## <a name="example"></a>例

`OR (1=2, "a"="a")` は、**TRUE** を返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
