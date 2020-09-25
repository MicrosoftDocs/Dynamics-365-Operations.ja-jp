---
title: ROUNDAMOUNT ER 機能
description: このトピックでは、ROUNDAMOUNT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 31a28279037ee6bfecd69b9d1e816afbd0de7894
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743978"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="774c6-103">ROUNDAMOUNT ER 機能</span><span class="sxs-lookup"><span data-stu-id="774c6-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="774c6-104">`ROUNDAMOUNT` 関数は、指定された丸めルールに従って、指定された数値を最も近い別の数値の倍数に丸めた結果の*実際*値を返します。</span><span class="sxs-lookup"><span data-stu-id="774c6-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="774c6-105">構文</span><span class="sxs-lookup"><span data-stu-id="774c6-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="774c6-106">引数</span><span class="sxs-lookup"><span data-stu-id="774c6-106">Arguments</span></span>

<span data-ttu-id="774c6-107">`number`: *Int* または *Real*</span><span class="sxs-lookup"><span data-stu-id="774c6-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="774c6-108">丸める必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="774c6-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="774c6-109">`decimals`: *Int* または *Real*</span><span class="sxs-lookup"><span data-stu-id="774c6-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="774c6-110">`number` パラメーターの値を倍数に丸める必要がある数。</span><span class="sxs-lookup"><span data-stu-id="774c6-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="774c6-111">`round rule`: *列挙値*</span><span class="sxs-lookup"><span data-stu-id="774c6-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="774c6-112">丸めルールを定義する **RoundOffType** 列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="774c6-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="774c6-113">この列挙型は、次の値を提供します。</span><span class="sxs-lookup"><span data-stu-id="774c6-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="774c6-114">標準 (通常)</span><span class="sxs-lookup"><span data-stu-id="774c6-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="774c6-115">下方向 (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="774c6-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="774c6-116">切り上げ (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="774c6-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="774c6-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="774c6-117">Return values</span></span>

<span data-ttu-id="774c6-118">*実績*</span><span class="sxs-lookup"><span data-stu-id="774c6-118">*Real*</span></span>

<span data-ttu-id="774c6-119">結果数値は、`decimals` パラメーターで指定された値の倍数で、`number` パラメーターで指定された値に近いです。</span><span class="sxs-lookup"><span data-stu-id="774c6-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="774c6-120">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="774c6-120">Usage notes</span></span>

<span data-ttu-id="774c6-121">`number` パラメーターがゼロの場合、この関数は常にゼロを返します。</span><span class="sxs-lookup"><span data-stu-id="774c6-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="774c6-122">`decimals` パラメーターがゼロのとき、この関数が既定の丸め値に丸めます</span><span class="sxs-lookup"><span data-stu-id="774c6-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="774c6-123">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、既定の丸め値は **0.01** です。</span><span class="sxs-lookup"><span data-stu-id="774c6-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="774c6-124">それ以外の場合、既定の丸め値 **1.0** です。</span><span class="sxs-lookup"><span data-stu-id="774c6-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="774c6-125">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この関数は最も近い丸め金額を丸めます。</span><span class="sxs-lookup"><span data-stu-id="774c6-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="774c6-126">`round rule` パラメーターが **RoundOffType.RoundDown** に設定されると、この関数は最も近い丸め金額をゼロに向かって丸めます。</span><span class="sxs-lookup"><span data-stu-id="774c6-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="774c6-127">`round rule` パラメーターが **RoundOffType.RoundUp** に設定されると、この関数はゼロから最も近い丸め金額に丸めます。</span><span class="sxs-lookup"><span data-stu-id="774c6-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="774c6-128">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この機能は [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel 機能および [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ 機能のように動作します。</span><span class="sxs-lookup"><span data-stu-id="774c6-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="774c6-129">備考</span><span class="sxs-lookup"><span data-stu-id="774c6-129">Remarks</span></span>

<span data-ttu-id="774c6-130">指定した小数点以下の桁数に数値を丸めるには、[ROUND](er-functions-mathematical-round.md) 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="774c6-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="774c6-131">例</span><span class="sxs-lookup"><span data-stu-id="774c6-131">Example</span></span>

<span data-ttu-id="774c6-132">**model.RoundOff** パラメーターが **RoundOffType.Ordinary** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。</span><span class="sxs-lookup"><span data-stu-id="774c6-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="774c6-133">**model.RoundOff** パラメーターが **RoundOffType.RoundDown** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。</span><span class="sxs-lookup"><span data-stu-id="774c6-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="774c6-134">**model.RoundOff** パラメーターが **RoundOffType.RoundUp** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 8.4 を返します。</span><span class="sxs-lookup"><span data-stu-id="774c6-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="774c6-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="774c6-135">Additional resources</span></span>

[<span data-ttu-id="774c6-136">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="774c6-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="774c6-137">算術関数</span><span class="sxs-lookup"><span data-stu-id="774c6-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
