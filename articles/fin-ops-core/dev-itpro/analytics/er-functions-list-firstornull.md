---
title: FIRSTORNULL ER 関数
description: このトピックでは、FIRSTORNULL 電子申告 (ER) 関数の使用方法について説明します
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753219"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER 関数

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` 関数は、レコードが空でない場合に、指定されたリストの最初のレコードを *コンテナー (レコード)* 値として返します。 レコードが空の場合、この関数は null *コンテナー (レコード)* 値を返します。

## <a name="syntax"></a>構文

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="example"></a>例

式 `FIRSTORNULL(SPLIT("",1)).Value` は空の文字列 (**""**) を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]