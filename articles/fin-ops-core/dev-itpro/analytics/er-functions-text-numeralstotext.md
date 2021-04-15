---
title: NUMERALSTOTEXT ER 機能
description: このトピックでは、NUMERALSTOTEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746150"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="95a36-103">NUMERALSTOTEXT ER 機能</span><span class="sxs-lookup"><span data-stu-id="95a36-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95a36-104">`NUMERALSTOTEXT` 関数は、指定された言語で綴らた後 (つまりテキスト文字列に変換された)、*文字列* 値として指定された数を返します。</span><span class="sxs-lookup"><span data-stu-id="95a36-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a36-105">構文</span><span class="sxs-lookup"><span data-stu-id="95a36-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="95a36-106">引数</span><span class="sxs-lookup"><span data-stu-id="95a36-106">Arguments</span></span>

<span data-ttu-id="95a36-107">`number`: *整数* または *実数*</span><span class="sxs-lookup"><span data-stu-id="95a36-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="95a36-108">綴りが必要な数を指定する数値。</span><span class="sxs-lookup"><span data-stu-id="95a36-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="95a36-109">`language`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="95a36-109">`language`: *String*</span></span>

<span data-ttu-id="95a36-110">言語コードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="95a36-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="95a36-111">`currency`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="95a36-111">`currency`: *String*</span></span>

<span data-ttu-id="95a36-112">通貨コードを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="95a36-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="95a36-113">`print currency name flag`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="95a36-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="95a36-114">綴られたテキストに通貨名を追加する必要があるかどうかを示す *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="95a36-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="95a36-115">`decimal points`: *整数*</span><span class="sxs-lookup"><span data-stu-id="95a36-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="95a36-116">綴られたテキストを持つべき小数点以下の桁数を示す *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="95a36-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="95a36-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="95a36-117">Return values</span></span>

<span data-ttu-id="95a36-118">*文字列*</span><span class="sxs-lookup"><span data-stu-id="95a36-118">*String*</span></span>

<span data-ttu-id="95a36-119">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="95a36-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="95a36-120">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="95a36-120">Usage notes</span></span>

<span data-ttu-id="95a36-121">言語コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="95a36-121">The language code is optional.</span></span> <span data-ttu-id="95a36-122">空の文字列として定義されている場合、実行中のコンテキストの言語コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="95a36-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="95a36-123">既定の言語コードは **EN-US** です。</span><span class="sxs-lookup"><span data-stu-id="95a36-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="95a36-124">実行中のコンテキストの言語コードは、実行されている電子申告 (ER) の **フォルダー** または **ファイル** 要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="95a36-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="95a36-125">通貨コードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="95a36-125">The currency code is optional.</span></span> <span data-ttu-id="95a36-126">空の文字列として定義されている場合、実行中のコンテキストの会社通貨が使用されます。</span><span class="sxs-lookup"><span data-stu-id="95a36-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="95a36-127">`print currency name flag` と `decimal points` 引数は、以下の言語コードについてのみ分析されます: **CS**、**ET**、**HU**、**LT**、**LV**、**PL**、および **RU**。</span><span class="sxs-lookup"><span data-stu-id="95a36-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="95a36-128">また、`print currency name flag` 引数は、通貨名の語形変化をサポートする国または地域のコンテキストを持つ会社に対してのみ分析されることにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="95a36-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="95a36-129">例 1</span><span class="sxs-lookup"><span data-stu-id="95a36-129">Example 1</span></span>

<span data-ttu-id="95a36-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` は、**"One Thousand Two Hundred Thirty Four and 56"** を返します。</span><span class="sxs-lookup"><span data-stu-id="95a36-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="95a36-131">例 2</span><span class="sxs-lookup"><span data-stu-id="95a36-131">Example 2</span></span>

<span data-ttu-id="95a36-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` は、**"Sto dwadzieścia"** を返します。</span><span class="sxs-lookup"><span data-stu-id="95a36-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="95a36-133">例 3</span><span class="sxs-lookup"><span data-stu-id="95a36-133">Example 3</span></span>

<span data-ttu-id="95a36-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` は、**"Сто двадцать евро 21 евроцент"** を返します。</span><span class="sxs-lookup"><span data-stu-id="95a36-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95a36-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="95a36-135">Additional resources</span></span>

[<span data-ttu-id="95a36-136">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="95a36-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]