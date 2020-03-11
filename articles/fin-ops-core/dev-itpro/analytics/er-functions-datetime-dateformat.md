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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042438"
---
# <span data-ttu-id="bcbdb-103"><a name="DATEFORMAT">DATEFORMAT ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="bcbdb-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcbdb-104">`DATEFORMAT` 関数は、特定の日付の値を指定された形式のテキストして、およびオプションで指定された[カルチャ](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) で表す*文字列*の値を返します。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="bcbdb-105">サポートされている形式の詳細については、[標準](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) と [カスタム](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="bcbdb-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="bcbdb-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="bcbdb-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="bcbdb-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="bcbdb-108">引数</span><span class="sxs-lookup"><span data-stu-id="bcbdb-108">Arguments</span></span>

<span data-ttu-id="bcbdb-109">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="bcbdb-109">`date`: *Date*</span></span>

<span data-ttu-id="bcbdb-110">書式設定する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="bcbdb-111">`format`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="bcbdb-111">`format`: *String*</span></span>

<span data-ttu-id="bcbdb-112">出力文字列の形式。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-112">The format of the output string.</span></span>

<span data-ttu-id="bcbdb-113">`culture`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="bcbdb-113">`culture`: *String*</span></span>

<span data-ttu-id="bcbdb-114">書式設定に使用するカルチャ。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="bcbdb-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="bcbdb-115">Return values</span></span>

<span data-ttu-id="bcbdb-116">*文字列*</span><span class="sxs-lookup"><span data-stu-id="bcbdb-116">*String*</span></span>

<span data-ttu-id="bcbdb-117">結果文字列値。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bcbdb-118">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="bcbdb-118">Usage notes</span></span>

<span data-ttu-id="bcbdb-119">呼び出された関数の引数としてカルチャが定義されていない場合、`culture` の値は、呼び出し元のコンテキストによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="bcbdb-120">たとえば、ドイツのカルチャを使用するように構成された **FILE** 要素に対して、電子申告 (ER) 形式の構文 1 を使用して `DATEFORMAT` 関数が呼び出された場合、変換はドイツのカルチャを使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="bcbdb-121">既定の `culture` の値は **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="bcbdb-122">例 1</span><span class="sxs-lookup"><span data-stu-id="bcbdb-122">Example 1</span></span>

<span data-ttu-id="bcbdb-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` は、指定されたカスタム形式に基づいて、現在のアプリケーション サーバーの日付 2015 年 12 月 24 日を、文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="bcbdb-124">例 2</span><span class="sxs-lookup"><span data-stu-id="bcbdb-124">Example 2</span></span>

<span data-ttu-id="bcbdb-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` は、選択されたドイツのカルチャおよび指定された形式に基づいて、現在のアプリケーション セッションの日付 2015 年 12 月 24 日を文字列 **"24-12-2015"** として返します。</span><span class="sxs-lookup"><span data-stu-id="bcbdb-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bcbdb-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bcbdb-126">Additional resources</span></span>

[<span data-ttu-id="bcbdb-127">日時の関数</span><span class="sxs-lookup"><span data-stu-id="bcbdb-127">Date and time functions</span></span>](er-functions-category-datetime.md)
