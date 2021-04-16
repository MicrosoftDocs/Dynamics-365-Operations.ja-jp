---
title: COLLECTEDLIST ER 関数
description: このトピックでは、COLLECTEDLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 494fb0fa1000abe8d0234d512e41926103c56f05
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755327"
---
# <a name="collectedlist-er-function"></a>COLLECTEDLIST ER 関数

[!include [banner](../includes/banner.md)]

`COLLECTEDLIST` 関数は、形式要素の **収集されたデータ キー値** プロパティによって返され、フォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値のリストを含む *レコード リスト* 値を返します。これは指定された条件を満たすものです。 各条件は、キー範囲とキー値で構成されます。

## <a name="syntax"></a>構文

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>引数

`condition 1 range`: *文字列*

電子申告 (ER) 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。 この引数は必須です。

`condition 1 value`: *文字列*

ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。 この引数は必須です。

`condition N range`: *文字列*

ER 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。 これらの追加引数はオプションです。

`condition N value`: *文字列*

ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

**収集したデータ キー名** および **収集したデータ キー値** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

この関数は、現在の **共通\\ファイル** コンポーネントの **出力の詳細を収集** オプションを無効にすると、空のリストを返します。

`condition range` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。

`condition value` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。

## <a name="example"></a>例

この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。

## <a name="additional-resources"></a>追加リソース

[データ収集機能](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]