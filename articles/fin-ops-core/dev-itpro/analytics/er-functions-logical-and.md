---
title: AND ER 関数
description: このトピックでは、AND 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745476"
---
# <a name="and-er-function"></a><span data-ttu-id="d0eb8-103">AND ER 関数</span><span class="sxs-lookup"><span data-stu-id="d0eb8-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0eb8-104">`AND` 関数は、指定したすべての条件が true である場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="d0eb8-105">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0eb8-106">構文</span><span class="sxs-lookup"><span data-stu-id="d0eb8-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="d0eb8-107">引数</span><span class="sxs-lookup"><span data-stu-id="d0eb8-107">Arguments</span></span>

<span data-ttu-id="d0eb8-108">`condition 1`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="d0eb8-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="d0eb8-109">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="d0eb8-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-110">This argument is required.</span></span>

<span data-ttu-id="d0eb8-111">`condition N`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="d0eb8-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="d0eb8-112">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="d0eb8-113">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0eb8-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="d0eb8-114">Return values</span></span>

<span data-ttu-id="d0eb8-115">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="d0eb8-115">*Boolean*</span></span>

<span data-ttu-id="d0eb8-116">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d0eb8-117">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="d0eb8-117">Usage notes</span></span>

<span data-ttu-id="d0eb8-118">論理関数の引数では、データ ソース参照、数値とテキストの値、ブール値、比較演算子、およびその他の電子申告 (ER) 関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="d0eb8-119">ただし、すべての引数は **TRUE** または **FALSE** の *ブール* 値に評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="d0eb8-120">例</span><span class="sxs-lookup"><span data-stu-id="d0eb8-120">Example</span></span>

<span data-ttu-id="d0eb8-121">`AND (1=1, "a"="a")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="d0eb8-122">`AND (1=2, "a"="a")` は、**FALSE** 返します。</span><span class="sxs-lookup"><span data-stu-id="d0eb8-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0eb8-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d0eb8-123">Additional resources</span></span>

[<span data-ttu-id="d0eb8-124">論理機能</span><span class="sxs-lookup"><span data-stu-id="d0eb8-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]