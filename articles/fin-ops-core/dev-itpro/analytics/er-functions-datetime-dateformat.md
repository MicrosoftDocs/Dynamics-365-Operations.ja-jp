---
title: DATEFORMAT ER 関数
description: このトピックでは、DATEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684935"
---
# <a name="dateformat-er-function"></a>DATEFORMAT ER 関数

[!include [banner](../includes/banner.md)]

`DATEFORMAT` 関数は、特定の日付の値を指定された形式のテキストして、およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す *文字列* の値を返します。 サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>引数

`date`: *日付*

書式設定する日付を表す日付値。

`format`: *文字列*

出力文字列の形式。

`culture`: *文字列*

書式設定に使用するカルチャ。

## <a name="return-values"></a>戻り値

*文字列*

結果文字列値。

## <a name="usage-notes"></a>使用上の注意

呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。 たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。 既定の `culture` の値は **EN-US** です。

## <a name="example-1"></a>例 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。

## <a name="example-2"></a>例 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を文字列 **"24-12-2015"** として返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)
