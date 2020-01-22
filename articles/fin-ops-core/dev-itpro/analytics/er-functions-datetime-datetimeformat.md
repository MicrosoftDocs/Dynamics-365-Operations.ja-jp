---
title: DATETIMEFORMAT ER 関数
description: このトピックでは、DATETIMEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916410"
---
# <a name="DATETIMEFORMAT">DATETIMEFORMAT ER 関数</a>

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` 関数は、特定の日時値を指定された形式のテキストして、およびオプションで指定された[カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す*文字列*の値を返します。 サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。

## <a name="syntax-1"></a>構文 1

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>構文 2

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>引数

`datetime`: *日時*

書式設定する日時を表す日時値。

`format`: *文字列*

出力文字列の形式。

`culture`: *文字列*

書式設定に使用するカルチャ。

## <a name="return-values"></a>戻り値

*文字列*

結果文字列値。

## <a name="usage-notes"></a>使用上の注意

呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。 たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATETIMEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。 既定の `culture` の値は **EN-US** です。

`DATETIMEFORMAT` 関数は、特定の日時値を変換するときに、関数がコンテキストで呼び出される ER 形式を実行しているアプリケーションユーザーのタイムゾーン設定を考慮します。

## <a name="example-1"></a>例 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日時値 2015 年 12 月 24 日を **"24-12-2015"** として返します。

## <a name="example-2"></a>例 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日時値 2015 年 12 月 24 日を **"24.12.2015"** として返します。

## <a name="example-3"></a>例 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` は、**言語と国/地域の基本設定**セクションにタイムゾーン値 **(GMT-08:00) 太平洋標準時 (米国およびカナダ)** を持つアプリケーション ユーザーによって開始されたプロセス中に呼び出されると、文字列値 **2019-11-12T08:00:00.0000000-08:00** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)
