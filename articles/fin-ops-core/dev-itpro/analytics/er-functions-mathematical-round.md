---
title: ROUND ER 関数
description: このトピックでは、ROUND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570401"
---
# <a name="round-er-function"></a><span data-ttu-id="f54ee-103">ROUND ER 関数</span><span class="sxs-lookup"><span data-stu-id="f54ee-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f54ee-104">`ROUND` 関数は、指定された数を指定された小数点以下の桁数に丸めてから、*実数* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="f54ee-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54ee-105">構文</span><span class="sxs-lookup"><span data-stu-id="f54ee-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="f54ee-106">引数</span><span class="sxs-lookup"><span data-stu-id="f54ee-106">Arguments</span></span>

<span data-ttu-id="f54ee-107">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="f54ee-107">`number`: *Real*</span></span>

<span data-ttu-id="f54ee-108">丸める必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="f54ee-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="f54ee-109">`decimals`: *整数*</span><span class="sxs-lookup"><span data-stu-id="f54ee-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="f54ee-110">小数点以下の桁数を表す数値。</span><span class="sxs-lookup"><span data-stu-id="f54ee-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="f54ee-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="f54ee-111">Return values</span></span>

<span data-ttu-id="f54ee-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="f54ee-112">*Real*</span></span>

<span data-ttu-id="f54ee-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="f54ee-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f54ee-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="f54ee-114">Usage notes</span></span>

<span data-ttu-id="f54ee-115">`decimals` 引数の値が 0 (ゼロ) より大きい場合、指定された数字は小数点以下の桁数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="f54ee-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="f54ee-116">`decimals` 引数の値が **0** (ゼロ) の場合、指定された数字は最も近い偶数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="f54ee-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="f54ee-117">`decimals` 引数の値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で丸められます。</span><span class="sxs-lookup"><span data-stu-id="f54ee-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="f54ee-118">例 1</span><span class="sxs-lookup"><span data-stu-id="f54ee-118">Example 1</span></span>

<span data-ttu-id="f54ee-119">`ROUND (1200.767, 2)` は、小数点第 2 位で四捨五入され、**1200.77** を返します。</span><span class="sxs-lookup"><span data-stu-id="f54ee-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f54ee-120">例 2</span><span class="sxs-lookup"><span data-stu-id="f54ee-120">Example 2</span></span>

<span data-ttu-id="f54ee-121">`ROUND (1200.767, -3)` は、1,000 の最も近い倍数に四捨五入され、**1000** を返します。</span><span class="sxs-lookup"><span data-stu-id="f54ee-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="f54ee-122">例 3</span><span class="sxs-lookup"><span data-stu-id="f54ee-122">Example 3</span></span>

<span data-ttu-id="f54ee-123">`ROUND (1200.5, 0)` は、最も近い偶数に丸めて **1200** を返しますが、`ROUND (1201.5, 0)` は同じ処理を行って **1202** を返します。</span><span class="sxs-lookup"><span data-stu-id="f54ee-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f54ee-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f54ee-124">Additional resources</span></span>

[<span data-ttu-id="f54ee-125">算術関数</span><span class="sxs-lookup"><span data-stu-id="f54ee-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]