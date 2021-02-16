---
title: リスト カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるリスト関数について説明します。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
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
ms.openlocfilehash: e2e708c59bceebf845ee78c98057133bb2892cf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686183"
---
# <a name="list-of-er-functions-in-the-list-category"></a>リスト カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子申告 (ER) リスト関数を使用して、*レコード リスト* および *コンテナー (レコード)* データ タイプのデータ ソースから情報を抽出し、操作を実行できます。 このトピックでは、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | この機能は、メモリ内の選択範囲として実行されます。 これは、指定したパスに一致するすべての品目を表すレコードの一覧を構成する、新しいフラット化された *レコード リスト* の値を返します。 |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | この機能は、結合された SQL クエリとして実行されます。 これは、指定したパスに一致するすべての品目を表すレコードの一覧を構成する、新しいフラット化された *レコード リスト* の値を返します。 |
| [数](er-functions-list-count.md)                       | この関数は、リストが空でない場合に、指定されたリストのレコード数を表す *整数* 値を返します。 リストが空の場合は、この関数は **0** (ゼロ) を返します。 |
| [EmptyList](er-functions-list-emptylist.md)               | この関数は、指定されたリストをリスト構造のソースとして使用し、空の *レコード リスト* 値を返します。|
| [列挙](er-functions-list-enumerate.md)               | この関数は、指定されたリストの列挙されたレコードで構成される新しい *レコード リスト* 値を返します。 |
| [フィルター](er-functions-list-filter.md)                     | この関数は、クエリが変更された後、指定されたリストを *レコード リスト* 値として返し、指定された条件でフィルタリングします。 |
| [先頭](er-functions-list-first.md)                       | この関数は、リストが空でない場合に、指定されたリストの最初のレコードを *コンテナー (レコード)* 値として返します。 リストが空の場合、この関数は例外をスローします。 |
| [FirstOrNull](er-functions-list-firstornull.md)           | この関数は、レコードが空でない場合に、指定されたリストの最初のレコードを *コンテナー (レコード)* 値として返します。 レコードが空の場合、この関数は null *コンテナー (レコード)* 値を返します。 |
| [指数](er-functions-list-index.md)                       | この関数は、指定されたリストの指定された数値インデックスを使用して選択された *コンテナー (レコード)* 値を返します。 インデックスが指定されたリスト内のレコードの範囲外である場合は、この関数は例外をスローします。 |
| [IsEmpty](er-functions-list-isempty.md)                   | この関数は、指定したリストにレコードが含まれていない場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [リスト](er-functions-list-list.md)                         | この関数は、指定された引数から作成された新しいリストで構成される *レコード リスト* 値を返します。|
| [ListDistinct](er-functions-list-listdistinct.md)         | この関数は、指定されたリストのすべてのレコードに対して、指定された式をセレクターとして計算します。 固有のセレクター値ごとに 1 つのレコードを含む、新しい *レコード リスト* 値を返します。|
| [ListJoin](er-functions-list-listjoin.md)                 | この関数は、指定された引数から作成された新しい結合リストを表す *レコード リスト* 値を返します。|
| [ListOfFields](er-functions-list-listoffields.md)         | この関数は、*列挙* または *コンテナー (レコード)* 型の指定された引数の構造に基づいて作成された *レコード リスト* 値を返します。 |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | この関数は、指定されたリストの最初のレコードのみで構成される *レコード リスト* 値を返します。|
| [OrderBy](er-functions-list-orderby.md)                   | この関数は、指定されたリストを、指定された引数に基づいて並べ替えられた後に *レコード リスト* 値として返します。 これらの引数は、式として定義することができます。 |
| [取消](er-functions-list-reverse.md)                   | この関数は、指定されたリストを、逆の並べ替え順で *レコード リスト* 値として返します。 |
| [分割](er-functions-list-split.md)                       | この関数は、指定された入力文字列をサブ文字列に分割し、新しい *レコード リスト* 値として結果を返します。 |
| [SplitList](er-functions-list-splitlist.md)               | この関数は、指定されたリストをサブリスト (またはバッチ) に分割します。各サブリストには指定されたレコード数が含まれます。 その後、結果をバッチで構成された新しい *レコード リスト* 値として返します。 |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | この関数は、指定されたリストを新しいサブリスト (バッチ) のリストに分割します。 各バッチのレコード数は動的に計算されます。 その後、関数は結果をバッチで構成された新しい *レコード リスト* 値として返します。 |
| [StringJoin](er-functions-list-stringjoin.md)             | この関数は、指定されたリストから指定したフィールドの連結された値で構成される *文字列* 値を返します。 値は、指定した区切り記号で区切ることができます。 |
| [場所](er-functions-list-where.md)                       | この関数は、指定されたリストを、指定された条件に基づいてフィルタリングされた後に *レコード リスト* 値として返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)
