---
title: DATETIMEFORMAT ER 関数
description: このトピックでは、DATETIMEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563633"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER 関数

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` 関数は、特定の日時値を指定された形式のテキストして、およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す *文字列* の値を返します。 サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。

## <a name="syntax-1"></a>構文 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>構文 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>引数

`datetime`: *日時*

書式設定する日時を表す日時値。

`format`: *文字列*

出力文字列の形式。

> [!NOTE]
> 書式文字列では、標準形式またはカスタム形式を使用する場合、大文字と小文字が区別されます。 たとえば、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" 書式指定子は短い日付パターンを使用して日付を返し、標準 "D" 書式指定子は長い日付パターンを使用して日付を返します。 また、[カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" 書式指定子は月を 1 から 12 の値で返しますが、カスタム "m" 書式指定子は 0 から 59 の分を返します。

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

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` は、**言語と国/地域の基本設定** セクションでタイム ゾーン値 **(GMT-08:00) 太平洋標準時 (米国およびカナダ)** を持つアプリケーション ユーザーが開始したプロセス中に関数が呼び出されると、文字列値 **2019-11-12T08:00:00.0000000-08:00** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]