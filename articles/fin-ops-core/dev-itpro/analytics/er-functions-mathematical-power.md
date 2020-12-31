---
title: POWER ER 関数
description: このトピックでは、POWER 電子申告 (ER) 関数使用方法についての情報を提供します。
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
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683332"
---
# <a name="power-er-function"></a><span data-ttu-id="d7160-103">POWER ER 関数</span><span class="sxs-lookup"><span data-stu-id="d7160-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7160-104">`POWER` 関数は、指定された正の数に指定された累乗をした結果を表す *実数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d7160-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7160-105">構文</span><span class="sxs-lookup"><span data-stu-id="d7160-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="d7160-106">引数</span><span class="sxs-lookup"><span data-stu-id="d7160-106">Arguments</span></span>

<span data-ttu-id="d7160-107">`number`: *実数* または *整数*</span><span class="sxs-lookup"><span data-stu-id="d7160-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="d7160-108">指定された累乗をする必要がある数値。</span><span class="sxs-lookup"><span data-stu-id="d7160-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="d7160-109">`power`: *実数* または *整数*</span><span class="sxs-lookup"><span data-stu-id="d7160-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="d7160-110">指定され累乗を表す数値。</span><span class="sxs-lookup"><span data-stu-id="d7160-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7160-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="d7160-111">Return values</span></span>

<span data-ttu-id="d7160-112">*実績*</span><span class="sxs-lookup"><span data-stu-id="d7160-112">*Real*</span></span>

<span data-ttu-id="d7160-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="d7160-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d7160-114">例 1</span><span class="sxs-lookup"><span data-stu-id="d7160-114">Example 1</span></span>

<span data-ttu-id="d7160-115">`POWER (10, 2)` は、**100** を返します。</span><span class="sxs-lookup"><span data-stu-id="d7160-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d7160-116">例 2</span><span class="sxs-lookup"><span data-stu-id="d7160-116">Example 2</span></span>

<span data-ttu-id="d7160-117">`POWER (4, 0.5)` は、**2** を返します。</span><span class="sxs-lookup"><span data-stu-id="d7160-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7160-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d7160-118">Additional resources</span></span>

[<span data-ttu-id="d7160-119">算術関数</span><span class="sxs-lookup"><span data-stu-id="d7160-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
