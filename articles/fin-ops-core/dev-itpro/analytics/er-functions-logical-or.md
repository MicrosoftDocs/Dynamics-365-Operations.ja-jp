---
title: OR ER 関数
description: このトピックでは、OR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565859"
---
# <a name="or-er-function"></a><span data-ttu-id="a8b07-103">OR ER 関数</span><span class="sxs-lookup"><span data-stu-id="a8b07-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8b07-104">`OR` 関数は、指定したすべての条件が false である場合、**FALSE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a8b07-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a8b07-105">指定した任意の条件が true である場合、関数は **TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a8b07-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b07-106">構文</span><span class="sxs-lookup"><span data-stu-id="a8b07-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="a8b07-107">引数</span><span class="sxs-lookup"><span data-stu-id="a8b07-107">Arguments</span></span>

<span data-ttu-id="a8b07-108">`condition 1`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="a8b07-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="a8b07-109">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="a8b07-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a8b07-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="a8b07-110">This argument is required.</span></span>

<span data-ttu-id="a8b07-111">`condition N`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="a8b07-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="a8b07-112">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="a8b07-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a8b07-113">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="a8b07-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a8b07-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="a8b07-114">Return values</span></span>

<span data-ttu-id="a8b07-115">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="a8b07-115">*Boolean*</span></span>

<span data-ttu-id="a8b07-116">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="a8b07-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="a8b07-117">例</span><span class="sxs-lookup"><span data-stu-id="a8b07-117">Example</span></span>

<span data-ttu-id="a8b07-118">`OR (1=2, "a"="a")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="a8b07-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8b07-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a8b07-119">Additional resources</span></span>

[<span data-ttu-id="a8b07-120">論理機能</span><span class="sxs-lookup"><span data-stu-id="a8b07-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]