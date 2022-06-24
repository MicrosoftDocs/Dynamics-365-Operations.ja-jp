---
title: SUMIFS ER 関数
description: この記事では、SUMIFS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 097c62f5b0f0b929e13354cd46417a194c9f2e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858802"
---
# <a name="sumifs-er-function"></a>SUMIFS ER 関数

[!include [banner](../includes/banner.md)]

`SUMIFS` 関数は、形式要素のバインディングにより返された、およびフォーマット中に送信ドキュメントを生成するのに形式要素が使用された際に収集された値の合計を表す *実数* 値を返します。これは指定された条件を満たすものです。 各条件は、キー範囲とキー値で構成されます。

## <a name="syntax"></a>構文

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>引数

`key name for summing`: *文字列*

バインディングの値を集計目的で使用する必要がある、 電子申告 (ER) 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。

**収集したデータ キー名** プロパティは、ER 形式の **数値** コンポーネントまたは **文字列** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

`condition 1 range`: *文字列*

ER 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。 この引数は必須です。

**収集したデータ キー名** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

`condition 1 value`: *文字列*

ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。 この引数は必須です。

**収集したデータ キー値** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

`condition N range`: *文字列*

ER 形式コンポーネントの **収集したデータ キー名** プロパティでコンフィギュレーションされた式によって返される値。 これらの追加引数はオプションです。

**収集したデータ キー名** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

`condition N value`: *文字列*

ER 形式コンポーネントの **収集したデータ キー値** プロパティでコンフィギュレーションされた式によって返される値。 これらの追加引数はオプションです。

**収集したデータ キー値** プロパティは、ER 形式の **シーケンス** コンポーネントまたは **XML 要素** コンポーネントのいずれかに対してコンフィギュレーションできます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

## <a name="return-values"></a>戻り値

*実績*

結果数値。

## <a name="usage-notes"></a>使用上の注意

この関数は、現在の **共通\\ファイル** コンポーネントの **出力の詳細を収集** オプションを無効にすると、**0** (ゼロ) 値を返します。

`condition range` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。

`condition value` 引数では、ワイルドカード文字 **"\*"** を使用して任意の複数の文字を表すことができます。

## <a name="example"></a>例

この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。

## <a name="additional-resources"></a>追加リソース

[データ収集機能](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]