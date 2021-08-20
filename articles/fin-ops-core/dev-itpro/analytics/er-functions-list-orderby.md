---
title: ORDERBY ER 関数
description: このトピックでは、ORDERBY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fcacacbf0727fa26350ff23c781c2da54d0ba77262c94dd48d88d01444352947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776149"
---
# <a name="orderby-er-function"></a>ORDERBY ER 関数

[!include [banner](../includes/banner.md)]

`ORDERBY` 関数は、指定されたリストを、指定された引数に基づいて並べ替えられた後に *レコード リスト* 値として返します。 これらの引数は、式として定義することができます。

## <a name="syntax"></a>構文

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`expression 1`: *フィールド*

呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。 参照フィールドは、プリミティブ データ型のフィールドである必要があります。 この引数は必須です。

`expression N`: *フィールド*

呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。 参照フィールドは、プリミティブ データ型のフィールドである必要があります。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="example-1"></a>例 1

*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("C|B|A", "|")` が含まれている場合、式 `FIRST( ORDERBY( DS, DS. Value)).Value` はテキスト値 **"A"** を返します。

## <a name="example-2"></a>例 2

**仕入先** を VendTable テーブルを参照する電子申告 (ER) データ ソースとして構成している場合、式 `ORDERBY (Vendors, Vendors.'name()')` は昇順の名前で並べ替えられた仕入先のリストを返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]