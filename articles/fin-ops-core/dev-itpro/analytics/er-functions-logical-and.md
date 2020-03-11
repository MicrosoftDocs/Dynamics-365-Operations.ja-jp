---
title: AND ER 関数
description: このトピックでは、AND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041817"
---
# <span data-ttu-id="b6faf-103"><a name="AND">AND ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="b6faf-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6faf-104">`AND` 関数は、指定したすべての条件が true である場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="b6faf-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="b6faf-105">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="b6faf-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6faf-106">構文</span><span class="sxs-lookup"><span data-stu-id="b6faf-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="b6faf-107">引数</span><span class="sxs-lookup"><span data-stu-id="b6faf-107">Arguments</span></span>

<span data-ttu-id="b6faf-108">`condition 1`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="b6faf-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="b6faf-109">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="b6faf-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="b6faf-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="b6faf-110">This argument is required.</span></span>

<span data-ttu-id="b6faf-111">`condition N`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="b6faf-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="b6faf-112">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="b6faf-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="b6faf-113">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="b6faf-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6faf-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="b6faf-114">Return values</span></span>

<span data-ttu-id="b6faf-115">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="b6faf-115">*Boolean*</span></span>

<span data-ttu-id="b6faf-116">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="b6faf-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6faf-117">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="b6faf-117">Usage notes</span></span>

<span data-ttu-id="b6faf-118">論理関数の引数では、データ ソース参照、数値とテキストの値、ブール値、比較演算子、およびその他の電子申告 (ER) 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6faf-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="b6faf-119">ただし、すべての引数は **TRUE** または **FALSE** の*ブール*値に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6faf-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="b6faf-120">例</span><span class="sxs-lookup"><span data-stu-id="b6faf-120">Example</span></span>

<span data-ttu-id="b6faf-121">`AND (1=1, "a"="a")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="b6faf-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="b6faf-122">`AND (1=2, "a"="a")` は、**FALSE** 返します。</span><span class="sxs-lookup"><span data-stu-id="b6faf-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6faf-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b6faf-123">Additional resources</span></span>

[<span data-ttu-id="b6faf-124">論理機能</span><span class="sxs-lookup"><span data-stu-id="b6faf-124">Logical functions</span></span>](er-functions-category-logical.md)
