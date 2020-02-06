---
title: NUMERALSTOTEXT ER 機能
description: このトピックでは、NUMERALSTOTEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915628"
---
# <span data-ttu-id="e22b2-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="e22b2-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e22b2-104">`NUMERALSTOTEXT` 関数は、指定された言語で綴らた後 (つまりテキスト文字列に変換された)、*文字列*値として指定された数を返します。</span><span class="sxs-lookup"><span data-stu-id="e22b2-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22b2-105">構文</span><span class="sxs-lookup"><span data-stu-id="e22b2-105">Syntax</span></span>

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="e22b2-106">引数</span><span class="sxs-lookup"><span data-stu-id="e22b2-106">Arguments</span></span>

<span data-ttu-id="e22b2-107">`number`: *整数*または*実数*</span><span class="sxs-lookup"><span data-stu-id="e22b2-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="e22b2-108">綴りが必要な数を指定する数値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="e22b2-109">`language`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="e22b2-109">`language`: *String*</span></span>

<span data-ttu-id="e22b2-110">言語コードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="e22b2-111">`currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="e22b2-111">`currency`: *String*</span></span>

<span data-ttu-id="e22b2-112">通貨コードを表す*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="e22b2-113">`print currency name flag`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="e22b2-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="e22b2-114">綴られたテキストに通貨名を追加する必要があるかどうかを示す*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="e22b2-115">`decimal points`: *整数*</span><span class="sxs-lookup"><span data-stu-id="e22b2-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="e22b2-116">綴られたテキストを持つべき小数点以下の桁数を示す*整数*値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="e22b2-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="e22b2-117">Return values</span></span>

<span data-ttu-id="e22b2-118">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e22b2-118">*String*</span></span>

<span data-ttu-id="e22b2-119">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="e22b2-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e22b2-120">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="e22b2-120">Usage notes</span></span>

<span data-ttu-id="e22b2-121">言語コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="e22b2-121">The language code is optional.</span></span> <span data-ttu-id="e22b2-122">空の文字列として定義されている場合、実行中のコンテキストの言語コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e22b2-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="e22b2-123">既定の言語コードは **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="e22b2-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="e22b2-124">実行中のコンテキストの言語コードは、実行されている電子申告 (ER) の**フォルダー**または**ファイル**要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e22b2-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="e22b2-125">通貨コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="e22b2-125">The currency code is optional.</span></span> <span data-ttu-id="e22b2-126">空の文字列として定義されている場合、実行中のコンテキストの会社通貨が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e22b2-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="e22b2-127">`print currency name flag` と `decimal points` 引数は、以下の言語コードについてのみ分析されます: **CS**、**ET**、**HU**、**LT**、**LV**、**PL**、および **RU**。</span><span class="sxs-lookup"><span data-stu-id="e22b2-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="e22b2-128">また、`print currency name flag` 引数は、通貨名の語形変化をサポートする国または地域のコンテキストを持つ会社に対してのみ分析されることにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="e22b2-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="e22b2-129">例 1</span><span class="sxs-lookup"><span data-stu-id="e22b2-129">Example 1</span></span>

<span data-ttu-id="e22b2-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` は、**"One Thousand Two Hundred Thirty Four and 56"** を返します。</span><span class="sxs-lookup"><span data-stu-id="e22b2-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e22b2-131">例 2</span><span class="sxs-lookup"><span data-stu-id="e22b2-131">Example 2</span></span>

<span data-ttu-id="e22b2-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` は、**"Sto dwadzieścia"** を返します。</span><span class="sxs-lookup"><span data-stu-id="e22b2-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="e22b2-133">例 3</span><span class="sxs-lookup"><span data-stu-id="e22b2-133">Example 3</span></span>

<span data-ttu-id="e22b2-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` は、**"Сто двадцать евро 21 евроцент"** を返します。</span><span class="sxs-lookup"><span data-stu-id="e22b2-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e22b2-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e22b2-135">Additional resources</span></span>

[<span data-ttu-id="e22b2-136">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="e22b2-136">Text functions</span></span>](er-functions-category-text.md)