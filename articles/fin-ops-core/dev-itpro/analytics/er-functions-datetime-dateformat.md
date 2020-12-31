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
# <a name="dateformat-er-function"></a><span data-ttu-id="1236c-103">DATEFORMAT ER 関数</span><span class="sxs-lookup"><span data-stu-id="1236c-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1236c-104">`DATEFORMAT` 関数は、特定の日付の値を指定された形式のテキストして、およびオプションで指定された [カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="1236c-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="1236c-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1236c-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1236c-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="1236c-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="1236c-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="1236c-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="1236c-108">引数</span><span class="sxs-lookup"><span data-stu-id="1236c-108">Arguments</span></span>

<span data-ttu-id="1236c-109">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="1236c-109">`date`: *Date*</span></span>

<span data-ttu-id="1236c-110">書式設定する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="1236c-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="1236c-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1236c-111">`format`: *String*</span></span>

<span data-ttu-id="1236c-112">出力文字列の形式。</span><span class="sxs-lookup"><span data-stu-id="1236c-112">The format of the output string.</span></span>

<span data-ttu-id="1236c-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1236c-113">`culture`: *String*</span></span>

<span data-ttu-id="1236c-114">書式設定に使用するカルチャ。</span><span class="sxs-lookup"><span data-stu-id="1236c-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="1236c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="1236c-115">Return values</span></span>

<span data-ttu-id="1236c-116">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1236c-116">*String*</span></span>

<span data-ttu-id="1236c-117">結果文字列値。</span><span class="sxs-lookup"><span data-stu-id="1236c-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1236c-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="1236c-118">Usage notes</span></span>

<span data-ttu-id="1236c-119">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="1236c-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="1236c-120">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="1236c-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="1236c-121">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="1236c-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="1236c-122">例 1</span><span class="sxs-lookup"><span data-stu-id="1236c-122">Example 1</span></span>

<span data-ttu-id="1236c-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="1236c-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="1236c-124">例 2</span><span class="sxs-lookup"><span data-stu-id="1236c-124">Example 2</span></span>

<span data-ttu-id="1236c-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="1236c-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1236c-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1236c-126">Additional resources</span></span>

[<span data-ttu-id="1236c-127">日時の関数</span><span class="sxs-lookup"><span data-stu-id="1236c-127">Date and time functions</span></span>](er-functions-category-datetime.md)
