---
title: DATEFORMAT ER 関数
description: このトピックでは、DATEFORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563657"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="12607-103">DATEFORMAT ER 関数</span><span class="sxs-lookup"><span data-stu-id="12607-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12607-104">`DATEFORMAT` 関数は、特定の日付の値を指定された形式のテキストして、およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="12607-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="12607-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12607-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="12607-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="12607-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="12607-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="12607-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="12607-108">引数</span><span class="sxs-lookup"><span data-stu-id="12607-108">Arguments</span></span>

<span data-ttu-id="12607-109">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="12607-109">`date`: *Date*</span></span>

<span data-ttu-id="12607-110">書式設定する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="12607-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="12607-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="12607-111">`format`: *String*</span></span>

<span data-ttu-id="12607-112">出力文字列の形式。</span><span class="sxs-lookup"><span data-stu-id="12607-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="12607-113">書式文字列では、標準形式またはカスタム形式を使用する場合、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="12607-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="12607-114">たとえば、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" 書式指定子は短い日付パターンを使用して日付を返し、標準 "D" 書式指定子は長い日付パターンを使用して日付を返します。</span><span class="sxs-lookup"><span data-stu-id="12607-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="12607-115">また、[カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" 書式指定子は月を 1 から 12 の値で返しますが、カスタム "m" 書式指定子は 0 から 59 の分を返します。</span><span class="sxs-lookup"><span data-stu-id="12607-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="12607-116">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="12607-116">`culture`: *String*</span></span>

<span data-ttu-id="12607-117">書式設定に使用するカルチャ。</span><span class="sxs-lookup"><span data-stu-id="12607-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="12607-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="12607-118">Return values</span></span>

<span data-ttu-id="12607-119">*文字列*</span><span class="sxs-lookup"><span data-stu-id="12607-119">*String*</span></span>

<span data-ttu-id="12607-120">結果文字列値。</span><span class="sxs-lookup"><span data-stu-id="12607-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="12607-121">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="12607-121">Usage notes</span></span>

<span data-ttu-id="12607-122">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="12607-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="12607-123">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="12607-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="12607-124">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="12607-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="12607-125">例 1</span><span class="sxs-lookup"><span data-stu-id="12607-125">Example 1</span></span>

<span data-ttu-id="12607-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="12607-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="12607-127">例 2</span><span class="sxs-lookup"><span data-stu-id="12607-127">Example 2</span></span>

<span data-ttu-id="12607-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="12607-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12607-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="12607-129">Additional resources</span></span>

[<span data-ttu-id="12607-130">日時の関数</span><span class="sxs-lookup"><span data-stu-id="12607-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]