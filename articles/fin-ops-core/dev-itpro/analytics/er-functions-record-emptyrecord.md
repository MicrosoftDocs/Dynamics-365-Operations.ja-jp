---
title: EMPTYRECORD ER 機能
description: この記事では、EMPTYRECORD 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280158"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER 機能

[!include [banner](../includes/banner.md)]

`EMPTYRECORD`関数は、指定されたリストまたはレコードと同じ構造を持つ *コンテナー (記録)* 値を返します。

## <a name="syntax"></a>構文

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト* または *コンテナー (レコード)*

*レコード リスト* または *コンテナー (レコード)* タイプのデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="usage-notes"></a>使用上の注意

> [!NOTE] 
> null レコードは、すべてのフィールドが空の値があるレコードです。 空の値が数字の場合は **0** (ゼロ)、文字列の場合、空の文字列などです。

## <a name="example"></a>例

`EMPTYRECORD (SPLIT ("abc", 1))` は、`SPLIT` 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。 詳細については、[SPLIT](er-functions-list-split.md) をご覧ください。

## <a name="additional-resources"></a>追加リソース

[レコード機能](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
