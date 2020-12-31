---
title: ABS ER 関数
description: このトピックでは、ABS 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683284"
---
# <a name="abs-er-function"></a><span data-ttu-id="e61f8-103">ABS ER 関数</span><span class="sxs-lookup"><span data-stu-id="e61f8-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e61f8-104">`ABS` 関数は、指定された数の絶対値 (係数) を *実数* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="e61f8-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="e61f8-105">つまり、符号のない数値を返します。</span><span class="sxs-lookup"><span data-stu-id="e61f8-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61f8-106">構文</span><span class="sxs-lookup"><span data-stu-id="e61f8-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="e61f8-107">引数</span><span class="sxs-lookup"><span data-stu-id="e61f8-107">Arguments</span></span>

<span data-ttu-id="e61f8-108">`number`: *実数*</span><span class="sxs-lookup"><span data-stu-id="e61f8-108">`number`: *Real*</span></span>

<span data-ttu-id="e61f8-109">係数を求める数値。</span><span class="sxs-lookup"><span data-stu-id="e61f8-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="e61f8-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e61f8-110">Return values</span></span>

<span data-ttu-id="e61f8-111">*実績*</span><span class="sxs-lookup"><span data-stu-id="e61f8-111">*Real*</span></span>

<span data-ttu-id="e61f8-112">結果数値。</span><span class="sxs-lookup"><span data-stu-id="e61f8-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e61f8-113">例</span><span class="sxs-lookup"><span data-stu-id="e61f8-113">Example</span></span>

<span data-ttu-id="e61f8-114">`ABS (-1)` は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="e61f8-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e61f8-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e61f8-115">Additional resources</span></span>

[<span data-ttu-id="e61f8-116">算術関数</span><span class="sxs-lookup"><span data-stu-id="e61f8-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
