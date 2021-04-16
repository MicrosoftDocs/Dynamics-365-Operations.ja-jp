---
title: ROUNDUP ER 関数
description: このトピックでは、ROUNDUP 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744442"
---
# <a name="roundup-er-function"></a><span data-ttu-id="b188f-103">ROUNDUP ER 関数</span><span class="sxs-lookup"><span data-stu-id="b188f-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b188f-104">`ROUNDUP` 関数は、指定された数を指定された小数点以下の桁数に切り上げてから、*実数* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="b188f-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b188f-105">構文</span><span class="sxs-lookup"><span data-stu-id="b188f-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b188f-106">引数</span><span class="sxs-lookup"><span data-stu-id="b188f-106">Arguments</span></span>

<span data-ttu-id="b188f-107">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="b188f-107">`number`: *Real*</span></span>

<span data-ttu-id="b188f-108">切り上げる必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="b188f-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="b188f-109">`decimals`: *整数*</span><span class="sxs-lookup"><span data-stu-id="b188f-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b188f-110">小数点以下の桁数を表す数値。</span><span class="sxs-lookup"><span data-stu-id="b188f-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b188f-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="b188f-111">Return values</span></span>

<span data-ttu-id="b188f-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="b188f-112">*Real*</span></span>

<span data-ttu-id="b188f-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="b188f-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b188f-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="b188f-114">Usage notes</span></span>

<span data-ttu-id="b188f-115">この関数は、[ROUND](er-functions-mathematical-round.md) のように機能しますが、常に指定した数字を (ゼロとは逆方向に) 切り上げます。</span><span class="sxs-lookup"><span data-stu-id="b188f-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="b188f-116">例 1</span><span class="sxs-lookup"><span data-stu-id="b188f-116">Example 1</span></span>

<span data-ttu-id="b188f-117">`ROUNDUP (1200.763, 2)` は、小数点第 2 位で切り上げられ、**1200.77** を返します。</span><span class="sxs-lookup"><span data-stu-id="b188f-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b188f-118">例 2</span><span class="sxs-lookup"><span data-stu-id="b188f-118">Example 2</span></span>

<span data-ttu-id="b188f-119">`ROUNDUP (1200.767, -3)` は、1,000 の最も近い倍数に切り上げられ、**2000** を返します。</span><span class="sxs-lookup"><span data-stu-id="b188f-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b188f-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b188f-120">Additional resources</span></span>

[<span data-ttu-id="b188f-121">算術関数</span><span class="sxs-lookup"><span data-stu-id="b188f-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]