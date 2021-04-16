---
title: NOT ER 関数
description: このトピックでは、NOT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751719"
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