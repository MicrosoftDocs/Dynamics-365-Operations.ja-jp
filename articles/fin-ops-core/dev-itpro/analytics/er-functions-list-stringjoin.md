---
title: STRINGJOIN ER 関数
description: このトピックでは、STRINGJOIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041794"
---
# <a name="STRINGJOIN">STRINGJOIN ER 関数</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` 関数は、指定されたリストから指定したフィールドの連結された値で構成される*文字列*値を返します。 値は、指定した区切り記号で区切ることができます。

## <a name="syntax"></a>構文

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`field`: *フィールド*

指定されたリストの*文字列*データ型のフィールドの有効なパス。

`delimiter`: *文字列*

サブ文字列を区切るために使用される区切り記号。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example"></a>例

データソース **DS** として `SPLIT("abc" , 1)` を入力すると、式 `STRINGJOIN (DS, DS.Value, "-")` は **"a-b-c"** を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)
