---
title: NOT ER 関数
description: このトピックでは、NOT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041725"
---
# <a name="NOT">NOT ER 関数</a>

[!include [banner](../includes/banner.md)]

`NOT` 関数は、指定された条件の取消論理値を*ブール*値として返します。

## <a name="syntax"></a>構文

```vb
NOT (condition)
```

## <a name="arguments"></a>引数

`condition`: *ブール値*

取り消す必要がある有効な条件式。

## <a name="return-values"></a>戻り値

*ブール型*

結果*ブール*値。

## <a name="example"></a>例

`NOT (TRUE)` は、**FALSE** 返します。

## <a name="additional-resources"></a>追加リソース

[論理機能](er-functions-category-logical.md)
