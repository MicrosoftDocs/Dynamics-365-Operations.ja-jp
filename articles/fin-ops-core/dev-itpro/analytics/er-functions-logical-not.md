---
title: NOT ER 関数
description: このトピックでは、NOT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565883"
---
# <a name="not-er-function"></a>NOT ER 関数

[!include [banner](../includes/banner.md)]

`NOT` 関数は、指定された条件の取消論理値を *ブール* 値として返します。

## <a name="syntax"></a>構文

```vb
NOT (condition)
```

## <a name="arguments"></a>引数

`condition`: *ブール値*

取り消す必要がある有効な条件式。

## <a name="return-values"></a>戻り値

*ブール型*

結果 *ブール* 値。

## <a name="example"></a>例

`NOT (TRUE)` は、**FALSE** 返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]