---
title: POWER ER 関数
description: このトピックでは、POWER 電子申告 (ER) 関数使用方法についての情報を提供します。
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750159"
---
# <a name="power-er-function"></a><span data-ttu-id="292ac-103">POWER ER 関数</span><span class="sxs-lookup"><span data-stu-id="292ac-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="292ac-104">`POWER` 関数は、指定された正の数に指定された累乗をした結果を表す *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="292ac-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="292ac-105">構文</span><span class="sxs-lookup"><span data-stu-id="292ac-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="292ac-106">引数</span><span class="sxs-lookup"><span data-stu-id="292ac-106">Arguments</span></span>

<span data-ttu-id="292ac-107">`number`: *実数* または *整数*</span><span class="sxs-lookup"><span data-stu-id="292ac-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="292ac-108">指定された累乗をする必要がある数値。</span><span class="sxs-lookup"><span data-stu-id="292ac-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="292ac-109">`power`: *実数* または *整数*</span><span class="sxs-lookup"><span data-stu-id="292ac-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="292ac-110">指定され累乗を表す数値。</span><span class="sxs-lookup"><span data-stu-id="292ac-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="292ac-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="292ac-111">Return values</span></span>

<span data-ttu-id="292ac-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="292ac-112">*Real*</span></span>

<span data-ttu-id="292ac-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="292ac-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="292ac-114">例 1</span><span class="sxs-lookup"><span data-stu-id="292ac-114">Example 1</span></span>

<span data-ttu-id="292ac-115">`POWER (10, 2)` は、**100** を返します。</span><span class="sxs-lookup"><span data-stu-id="292ac-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="292ac-116">例 2</span><span class="sxs-lookup"><span data-stu-id="292ac-116">Example 2</span></span>

<span data-ttu-id="292ac-117">`POWER (4, 0.5)` は、**2** を返します。</span><span class="sxs-lookup"><span data-stu-id="292ac-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="292ac-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="292ac-118">Additional resources</span></span>

[<span data-ttu-id="292ac-119">算術関数</span><span class="sxs-lookup"><span data-stu-id="292ac-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]