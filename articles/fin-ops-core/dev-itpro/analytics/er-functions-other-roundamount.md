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
ms.openlocfilehash: 5903f562b5f266572f999756539fa7b9ef145023
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041334"
---
# <span data-ttu-id="0b1f7-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="0b1f7-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b1f7-104">`ROUNDAMOUNT` 関数は、指定された丸めルールに従って、指定された数値を最も近い別の数値の倍数に丸めた結果の*実際*値を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1f7-105">構文</span><span class="sxs-lookup"><span data-stu-id="0b1f7-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="0b1f7-106">引数</span><span class="sxs-lookup"><span data-stu-id="0b1f7-106">Arguments</span></span>

<span data-ttu-id="0b1f7-107">`number`: *Int* または *Real*</span><span class="sxs-lookup"><span data-stu-id="0b1f7-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="0b1f7-108">丸める必要のある数値。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="0b1f7-109">`decimals`: *Int* または *Real*</span><span class="sxs-lookup"><span data-stu-id="0b1f7-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="0b1f7-110">`number` パラメーターの値を倍数に丸める必要がある数。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="0b1f7-111">`round rule`: *列挙値*</span><span class="sxs-lookup"><span data-stu-id="0b1f7-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="0b1f7-112">丸めルールを定義する **RoundOffType** 列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="0b1f7-113">この列挙型は、次の値を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="0b1f7-114">標準 (通常)</span><span class="sxs-lookup"><span data-stu-id="0b1f7-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="0b1f7-115">下方向 (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="0b1f7-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="0b1f7-116">切り上げ (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="0b1f7-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="0b1f7-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b1f7-117">Return values</span></span>

<span data-ttu-id="0b1f7-118">*実績*</span><span class="sxs-lookup"><span data-stu-id="0b1f7-118">*Real*</span></span>

<span data-ttu-id="0b1f7-119">結果数値は、`decimals` パラメーターで指定された値の倍数で、`number` パラメーターで指定された値に近いです。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0b1f7-120">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0b1f7-120">Usage notes</span></span>

<span data-ttu-id="0b1f7-121">`number` パラメーターがゼロの場合、この関数は常にゼロを返します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="0b1f7-122">`decimals` パラメーターがゼロのとき、この関数が既定の丸め値に丸めます</span><span class="sxs-lookup"><span data-stu-id="0b1f7-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="0b1f7-123">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、既定の丸め値は **0.01** です。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="0b1f7-124">それ以外の場合、既定の丸め値 **1.0** です。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="0b1f7-125">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この関数は最も近い丸め金額を丸めます。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="0b1f7-126">`round rule` パラメーターが **RoundOffType.RoundDown** に設定されると、この関数は最も近い丸め金額をゼロに向かって丸めます。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="0b1f7-127">`round rule` パラメーターが **RoundOffType.RoundUp** に設定されると、この関数はゼロから最も近い丸め金額に丸めます。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="0b1f7-128">`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この機能は [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel 機能および [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ 機能のように動作します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1f7-129">備考</span><span class="sxs-lookup"><span data-stu-id="0b1f7-129">Remarks</span></span>

<span data-ttu-id="0b1f7-130">指定した小数点以下の桁数に数値を丸めるには、[ROUND](er-functions-mathematical-round.md) 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="0b1f7-131">例</span><span class="sxs-lookup"><span data-stu-id="0b1f7-131">Example</span></span>

<span data-ttu-id="0b1f7-132">**model.RoundOff** パラメーターが **RoundOffType.Ordinary** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="0b1f7-133">**model.RoundOff** パラメーターが **RoundOffType.RoundDown** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="0b1f7-134">**model.RoundOff** パラメーターが **RoundOffType.RoundUp** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 8.4 を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1f7-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b1f7-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0b1f7-135">Additional resources</span></span>

[<span data-ttu-id="0b1f7-136">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="0b1f7-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="0b1f7-137">算術関数</span><span class="sxs-lookup"><span data-stu-id="0b1f7-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
