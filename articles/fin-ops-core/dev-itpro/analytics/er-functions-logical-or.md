---
title: OR ER 関数
description: このトピックでは、OR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917123"
---
# <span data-ttu-id="fe408-103"><a name="OR">OR ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="fe408-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe408-104">`OR` 関数は、指定したすべての条件が false である場合、**FALSE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="fe408-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="fe408-105">指定した任意の条件が true である場合、関数は **TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="fe408-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe408-106">構文</span><span class="sxs-lookup"><span data-stu-id="fe408-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="fe408-107">引数</span><span class="sxs-lookup"><span data-stu-id="fe408-107">Arguments</span></span>

<span data-ttu-id="fe408-108">`condition 1`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="fe408-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="fe408-109">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="fe408-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="fe408-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="fe408-110">This argument is required.</span></span>

<span data-ttu-id="fe408-111">`condition N`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="fe408-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="fe408-112">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="fe408-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="fe408-113">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="fe408-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe408-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="fe408-114">Return values</span></span>

<span data-ttu-id="fe408-115">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="fe408-115">*Boolean*</span></span>

<span data-ttu-id="fe408-116">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="fe408-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="fe408-117">例</span><span class="sxs-lookup"><span data-stu-id="fe408-117">Example</span></span>

<span data-ttu-id="fe408-118">`OR (1=2, "a"="a")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="fe408-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe408-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fe408-119">Additional resources</span></span>

[<span data-ttu-id="fe408-120">論理機能</span><span class="sxs-lookup"><span data-stu-id="fe408-120">Logical functions</span></span>](er-functions-category-logical.md)
