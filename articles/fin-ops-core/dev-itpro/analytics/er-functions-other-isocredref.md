---
title: ISOCREDREF ER 関数
description: このトピックでは、ISOCREDREF 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916962"
---
# <a name="ISOCREDREF">ISOCREDREF ER 関数</a>

[!include [banner](../includes/banner.md)]

`ISOCREDREF` 機能は、指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を表す*文字列*値を返します。

## <a name="syntax"></a>構文

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>引数

`invoice number digits`: *文字列*

請求書番号の桁数を表すテキスト値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

> [!NOTE] 
> ISO 準拠ではないアルファベットの記号を削除するには、`invoice number digits` 引数はこの関数へ渡す前に移動する必要があります。

## <a name="example"></a>例

`ISOCredRef ("VEND-200002")` は、**"RF23VEND-200002"** を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)
