---
title: DATETIMEFORMAT ER 関数
description: このトピックでは、DATETIMEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825376"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="ff44d-103">DATETIMEFORMAT ER 関数</span><span class="sxs-lookup"><span data-stu-id="ff44d-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff44d-104">`DATETIMEFORMAT` 関数は、特定の日時値を指定された形式のテキストして、およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ff44d-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff44d-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ff44d-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="ff44d-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ff44d-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="ff44d-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ff44d-108">引数</span><span class="sxs-lookup"><span data-stu-id="ff44d-108">Arguments</span></span>

<span data-ttu-id="ff44d-109">`datetime`: *日時*</span><span class="sxs-lookup"><span data-stu-id="ff44d-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="ff44d-110">書式設定する日時を表す日時値。</span><span class="sxs-lookup"><span data-stu-id="ff44d-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="ff44d-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="ff44d-111">`format`: *String*</span></span>

<span data-ttu-id="ff44d-112">出力文字列の形式。</span><span class="sxs-lookup"><span data-stu-id="ff44d-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="ff44d-113">書式文字列では、標準形式またはカスタム形式を使用する場合、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="ff44d-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="ff44d-114">たとえば、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" 書式指定子は短い日付パターンを使用して日付を返し、標準 "D" 書式指定子は長い日付パターンを使用して日付を返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="ff44d-115">また、[カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" 書式指定子は月を 1 から 12 の値で返しますが、カスタム "m" 書式指定子は 0 から 59 の分を返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="ff44d-116">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="ff44d-116">`culture`: *String*</span></span>

<span data-ttu-id="ff44d-117">書式設定に使用するカルチャ。</span><span class="sxs-lookup"><span data-stu-id="ff44d-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff44d-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="ff44d-118">Return values</span></span>

<span data-ttu-id="ff44d-119">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ff44d-119">*String*</span></span>

<span data-ttu-id="ff44d-120">結果文字列値。</span><span class="sxs-lookup"><span data-stu-id="ff44d-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ff44d-121">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="ff44d-121">Usage notes</span></span>

<span data-ttu-id="ff44d-122">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="ff44d-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ff44d-123">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATETIMEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="ff44d-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ff44d-124">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="ff44d-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="ff44d-125">`DATETIMEFORMAT` 関数は、特定の日時値を変換するときに、関数がコンテキストで呼び出される ER 形式を実行しているアプリケーションユーザーのタイムゾーン設定を考慮します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="ff44d-126">例 1</span><span class="sxs-lookup"><span data-stu-id="ff44d-126">Example 1</span></span>

<span data-ttu-id="ff44d-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日時値 2015 年 12 月 24 日を **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ff44d-128">例 2</span><span class="sxs-lookup"><span data-stu-id="ff44d-128">Example 2</span></span>

<span data-ttu-id="ff44d-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日時値 2015 年 12 月 24 日を **"24.12.2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="ff44d-130">例 3</span><span class="sxs-lookup"><span data-stu-id="ff44d-130">Example 3</span></span>

<span data-ttu-id="ff44d-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` は、**言語と国/地域の基本設定** セクションでタイム ゾーン値 **(GMT-08:00) 太平洋標準時 (米国およびカナダ)** を持つアプリケーション ユーザーが開始したプロセス中に関数が呼び出されると、文字列値 **2019-11-12T08:00:00.0000000-08:00** を返します。</span><span class="sxs-lookup"><span data-stu-id="ff44d-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff44d-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ff44d-132">Additional resources</span></span>

[<span data-ttu-id="ff44d-133">日時の関数</span><span class="sxs-lookup"><span data-stu-id="ff44d-133">Date and time functions</span></span>](er-functions-category-datetime.md)
