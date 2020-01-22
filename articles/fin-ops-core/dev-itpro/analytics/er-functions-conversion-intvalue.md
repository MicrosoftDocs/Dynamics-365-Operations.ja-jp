---
title: INTVALUE ER 関数
description: このトピックでは、INTVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917721"
---
# <span data-ttu-id="1a9c4-103"><a name="INTVALUE">INTVALUE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="1a9c4-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a9c4-104">`INTVALUE` 関数は、指定された文字列を表す *Int* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1a9c4-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="1a9c4-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1a9c4-106">構文 2</span><span class="sxs-lookup"><span data-stu-id="1a9c4-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1a9c4-107">引数</span><span class="sxs-lookup"><span data-stu-id="1a9c4-107">Arguments</span></span>

<span data-ttu-id="1a9c4-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1a9c4-108">`text`: *String*</span></span>

<span data-ttu-id="1a9c4-109">*Int* 数に変換する必要があるテキスト値。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="1a9c4-110">`number`: *実数*または*整数*</span><span class="sxs-lookup"><span data-stu-id="1a9c4-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1a9c4-111">*Int* 数に変換する必要がある数値の*実数*または*整数*値。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a9c4-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="1a9c4-112">Return values</span></span>

<span data-ttu-id="1a9c4-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="1a9c4-113">*Int*</span></span>

<span data-ttu-id="1a9c4-114">結果数値。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1a9c4-115">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="1a9c4-115">Usage notes</span></span>

<span data-ttu-id="1a9c4-116">任意の小数点以下の桁数が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1a9c4-117">例 1</span><span class="sxs-lookup"><span data-stu-id="1a9c4-117">Example 1</span></span>

<span data-ttu-id="1a9c4-118">`INTVALUE ("100.77")` は、*Int* の値 **100** を返します。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1a9c4-119">例 2</span><span class="sxs-lookup"><span data-stu-id="1a9c4-119">Example 2</span></span>

<span data-ttu-id="1a9c4-120">`INTVALUE (-100.77)` は、*Int* の値 **-100** を返します。</span><span class="sxs-lookup"><span data-stu-id="1a9c4-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a9c4-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1a9c4-121">Additional resources</span></span>

[<span data-ttu-id="1a9c4-122">型変換関数</span><span class="sxs-lookup"><span data-stu-id="1a9c4-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
