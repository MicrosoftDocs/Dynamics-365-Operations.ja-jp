---
title: OR ER 関数
description: このトピックでは、OR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565859"
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