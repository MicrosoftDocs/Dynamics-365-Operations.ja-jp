---
title: FORMATELEMENTNAME ER 関数
description: このトピックでは、FORMATELEMENTNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ef59bb44a7096f4c095ce37a89558a717748f02e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685330"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER 関数

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` 関数は、現在の電子申告 (ER) 形式要素の名前を表す *文字列* 値を返します。

## <a name="syntax"></a>構文

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

この関数は、**テキスト** グループからの ER 形式のコンポーネントの **収集したデータ キー名** および **収集したデータ キー値** プロパティに対してコンフィギュレーションされた ER 式で呼び出すことができます。それは **出力の詳細を収集** オプションがオンになっている **共通\\ファイル** コンポーネントの下に存在します。

## <a name="example"></a>例

この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発** 業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。

## <a name="additional-resources"></a>追加リソース

[データ収集機能](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]