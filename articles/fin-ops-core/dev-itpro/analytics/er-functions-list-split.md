---
title: SPLIT ER 関数
description: このトピックでは、SPLIT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686395"
---
# <a name="split-er-function"></a>SPLIT ER 関数

[!include [banner](../includes/banner.md)]

`SPLIT` 関数は、指定された入力文字列をサブ文字列に分割し、結果を新しい *レコード リスト* 値として返します。

## <a name="syntax-1"></a>構文 1

```vb
SPLIT (input, length)
```

この構文は、指定された入力文字列を指定された長さのサブ文字列に分割するために使用します。

## <a name="syntax-2"></a>構文 2

```vb
SPLIT (input, delimiter)
```

この構文は、指定された入力文字列を指定された区切り記号に基づいてサブ文字列に分割するために使用します。

## <a name="arguments"></a>引数

`input`: *文字列*

分割するテキスト。

`length`: *整数*

単一のサブ文字列の最大の長さ。

`delimiter`: *文字列*

サブ文字列を区切るために使用される区切り記号。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

返されるリストのレコード構造は、*文字列* 型の **値** フィールドで構成されます。 返されるリストのすべてのレコードには、このフィールドで生成されたサブ文字列が含まれます。

`delimiter` 引数が空の場合、返される新しいリストは、*文字列* 型の **値** フィールドを持つ 1 つのレコードで構成されます。 このフィールドには、入力テキストが含まれています。

`input` 引数が空の場合は、新しい空のリストが返されます。 `input` または `delimiter` 引数のいずれかを指定しない場合 (null)、アプリケーション例外がスローされます。

## <a name="example-1"></a>例 1

`SPLIT ("abcd", 3)` は、*文字列* 型の **値** フィールドのある 2 つのレコードで構成される新しいリストを返します。 最初のレコードの **値** フィールドには、テキスト **"abc"** が、2 つ目のレコードの **値** フィールドには、テキスト **"d"** が含まれます。

## <a name="example-2"></a>例 2

`SPLIT ("XAb aBy", "aB")` は、*文字列* 型の **値** フィールドのある 3 つのレコードで構成される新しいリストを返します。 最初のレコードの **値** フィールドには、テキスト **"X"** が、2 つ目のレコードの **値** フィールドには、テキスト **"&nbsp;"** が、3 つ目のレコードの **値** フィールドにはテキスト **"y"** が含まれます。 

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)
