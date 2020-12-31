---
title: データ収集カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるデータ収集関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686296"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>データ収集カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子申告 (ER) データ収集関数は、**テキスト** または **Xml** 形式で生成された出力のデータに基づいて、実行中の ER 形式で棚卸および集計を行うために使用されます。 この方法は、実行される ER 形式のパフォーマンスを向上させたり、生成されたドキュメントに実行中の合計値を入力したり、その他の目的でも使用されます。 このトピックでは、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | この関数は、形式要素の **収集されたデータ キー値** プロパティによって返され、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値のリストを含む *レコード リスト* 値を返します。これは指定された条件を満たすものです。 各条件は、キー範囲とキー値で構成されます。 |
| [CountIF](er-functions-datacollection-countif.md) | この関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。 条件は、キー範囲とキー値で構成されます。 |
| [CountIFs](er-functions-datacollection-countifs.md) | この関数は、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された、形式要素の数を表す *整数* 値を返します。これは指定された条件を満たすものです。 各条件は、キー範囲とキー値で構成されます。 |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | この関数は、現在の ER 形式要素の名前を表す *文字列* の値を返します。 |
| [SumIF](er-functions-datacollection-sumif.md) | この関数は、形式要素のバインディングにより返された、およびフォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値の合計を表す *実数* 値を返します。これは指定された条件を満たすものです。 条件は、キー範囲とキー値で構成されます。 |
| [SumIFs](er-functions-datacollection-sumifs.md) | この関数は、形式要素のバインディングにより返された、およびフォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値の合計を表す *実数* 値を返します。これは指定された条件を満たすものです。 各条件は、キー範囲とキー値で構成されます。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)
