---
title: ROUNDDOWN ER 関数
description: このトピックでは、ROUNDDOWN 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915858"
---
# <span data-ttu-id="8096b-103"><a name="ROUNDDOWN">ROUNDDOWN ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="8096b-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8096b-104">`ROUNDDOWN` 関数は、指定された数を指定された小数点以下の桁数に切り下げてから、*実数*値として返します。</span><span class="sxs-lookup"><span data-stu-id="8096b-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="8096b-105">構文</span><span class="sxs-lookup"><span data-stu-id="8096b-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="8096b-106">引数</span><span class="sxs-lookup"><span data-stu-id="8096b-106">Arguments</span></span>

<span data-ttu-id="8096b-107">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="8096b-107">`number`: *Real*</span></span>

<span data-ttu-id="8096b-108">切り下げる必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="8096b-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="8096b-109">`decimals`: *整数*</span><span class="sxs-lookup"><span data-stu-id="8096b-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="8096b-110">小数点以下の桁数を表す数値。</span><span class="sxs-lookup"><span data-stu-id="8096b-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="8096b-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="8096b-111">Return values</span></span>

<span data-ttu-id="8096b-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="8096b-112">*Real*</span></span>

<span data-ttu-id="8096b-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="8096b-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8096b-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="8096b-114">Usage notes</span></span>

<span data-ttu-id="8096b-115">この関数は、[ROUND](er-functions-mathematical-round.md) のように機能しますが、常に指定した数字を (ゼロ方向に) 切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="8096b-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="8096b-116">例 1</span><span class="sxs-lookup"><span data-stu-id="8096b-116">Example 1</span></span>

<span data-ttu-id="8096b-117">`ROUNDDOWN (1200.767, 2)` は、小数点第 2 位で切り下げられ、**1200.76** を返します。</span><span class="sxs-lookup"><span data-stu-id="8096b-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="8096b-118">例 2</span><span class="sxs-lookup"><span data-stu-id="8096b-118">Example 2</span></span>

<span data-ttu-id="8096b-119">`ROUNDDOWN (1700.767, -3)` は、1,000 の最も近い倍数に切り下げられ、**1000** を返します。</span><span class="sxs-lookup"><span data-stu-id="8096b-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8096b-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8096b-120">Additional resources</span></span>

[<span data-ttu-id="8096b-121">算術関数</span><span class="sxs-lookup"><span data-stu-id="8096b-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
