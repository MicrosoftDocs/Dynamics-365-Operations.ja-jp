---
title: NUMBERVALUE ER 機能
description: このトピックでは、NUMBERVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743402"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="c3893-103">NUMBERVALUE ER 機能</span><span class="sxs-lookup"><span data-stu-id="c3893-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3893-104">`NUMBERVALUE` 関数は、指定された*文字列*値から変換された*実数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="c3893-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="c3893-105">変換時に、指定された 10 進と桁区切り記号が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="c3893-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3893-106">構文</span><span class="sxs-lookup"><span data-stu-id="c3893-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="c3893-107">引数</span><span class="sxs-lookup"><span data-stu-id="c3893-107">Arguments</span></span>

<span data-ttu-id="c3893-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="c3893-108">`text`: *String*</span></span>

<span data-ttu-id="c3893-109">*実数*の数に変換する必要があるテキスト値。</span><span class="sxs-lookup"><span data-stu-id="c3893-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="c3893-110">`decimal separator`: 文字列</span><span class="sxs-lookup"><span data-stu-id="c3893-110">`decimal separator`: String</span></span>

<span data-ttu-id="c3893-111">少数桁の区切り文字。</span><span class="sxs-lookup"><span data-stu-id="c3893-111">A decimal separator.</span></span> <span data-ttu-id="c3893-112">10 進数の整数部と小数点以下を区切るのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3893-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="c3893-113">`digit grouping separator`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="c3893-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="c3893-114">桁区切り記号。</span><span class="sxs-lookup"><span data-stu-id="c3893-114">A digit grouping separator.</span></span> <span data-ttu-id="c3893-115">千の位の区切り記号として使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3893-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3893-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="c3893-116">Return values</span></span>

<span data-ttu-id="c3893-117">*実績*</span><span class="sxs-lookup"><span data-stu-id="c3893-117">*Real*</span></span>

<span data-ttu-id="c3893-118">結果数値。</span><span class="sxs-lookup"><span data-stu-id="c3893-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c3893-119">例</span><span class="sxs-lookup"><span data-stu-id="c3893-119">Example</span></span>

<span data-ttu-id="c3893-120">`NUMBERVALUE( "1 234,56", ",", " ")` は、**1234.56** を返します。</span><span class="sxs-lookup"><span data-stu-id="c3893-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3893-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c3893-121">Additional resources</span></span>

[<span data-ttu-id="c3893-122">型変換関数</span><span class="sxs-lookup"><span data-stu-id="c3893-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
