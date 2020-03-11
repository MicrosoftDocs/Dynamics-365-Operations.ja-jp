---
title: ROUND ER 関数
description: このトピックでは、ROUND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041610"
---
# <span data-ttu-id="fec34-103"><a name="ROUND">ROUND ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="fec34-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fec34-104">`ROUND` 関数は、指定された数を指定された小数点以下の桁数に丸めてから、*実数*値として返します。</span><span class="sxs-lookup"><span data-stu-id="fec34-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec34-105">構文</span><span class="sxs-lookup"><span data-stu-id="fec34-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="fec34-106">引数</span><span class="sxs-lookup"><span data-stu-id="fec34-106">Arguments</span></span>

<span data-ttu-id="fec34-107">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="fec34-107">`number`: *Real*</span></span>

<span data-ttu-id="fec34-108">丸める必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="fec34-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="fec34-109">`decimals`: *整数*</span><span class="sxs-lookup"><span data-stu-id="fec34-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="fec34-110">小数点以下の桁数を表す数値。</span><span class="sxs-lookup"><span data-stu-id="fec34-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="fec34-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="fec34-111">Return values</span></span>

<span data-ttu-id="fec34-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="fec34-112">*Real*</span></span>

<span data-ttu-id="fec34-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="fec34-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fec34-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="fec34-114">Usage notes</span></span>

<span data-ttu-id="fec34-115">`decimals` 引数の値が 0 (ゼロ) より大きい場合、指定された数字は小数点以下の桁数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="fec34-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="fec34-116">`decimals` 引数の値が **0** (ゼロ) の場合、指定された数字は最も近い整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="fec34-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="fec34-117">`decimals` 引数の値が 0 (ゼロ) より小さい場合、指定された数字は小数点より左で丸められます。</span><span class="sxs-lookup"><span data-stu-id="fec34-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="fec34-118">例 1</span><span class="sxs-lookup"><span data-stu-id="fec34-118">Example 1</span></span>

<span data-ttu-id="fec34-119">`ROUND (1200.767, 2)` は、小数点第 2 位で四捨五入され、**1200.77** を返します。</span><span class="sxs-lookup"><span data-stu-id="fec34-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fec34-120">例 2</span><span class="sxs-lookup"><span data-stu-id="fec34-120">Example 2</span></span>

<span data-ttu-id="fec34-121">`ROUND (1200.767, -3)` は、1,000 の最も近い倍数に四捨五入され、**1000** を返します。</span><span class="sxs-lookup"><span data-stu-id="fec34-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fec34-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fec34-122">Additional resources</span></span>

[<span data-ttu-id="fec34-123">算術関数</span><span class="sxs-lookup"><span data-stu-id="fec34-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
