---
title: INDEX ER 関数
description: このトピックでは、INDEX 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087754"
---
# <a name="index-er-function"></a>INDEX ER 関数

[!include [banner](../includes/banner.md)]

`INDEX` 関数は、指定されたリストの指定された数値インデックスを使用して選択された *コンテナー (レコード)* 値を返します。 インデックスが指定されたリスト内のレコードの範囲外である場合は、例外がスローされます。

## <a name="syntax"></a>構文

```vb
INDEX (list, index)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`index`: *整数*

指定したリスト内の目的のレコードの位置を示す数値インデックス。

> [!NOTE]
> この関数では 1 ベースの番号付けを使用しているため、指定したリストの最初のレコードを返すには値 **1** を指定します。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="example-1"></a>例 1

*計算済フィールド* タイプのデータ ソース **DS** を入力していて、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `DS.Value` は、このレコード リストの 2 番目のレコードのテキスト値 **"B"** を返します。 式 `INDEX (SPLIT ("A|B|C", "|"), 2).Value` もテキスト値 **"B"** を返します。

## <a name="example-2"></a>例 2

*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `INDEX (SPLIT ("A|B|C", "|"), 4).Value` は実行時に例外をスローします。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
