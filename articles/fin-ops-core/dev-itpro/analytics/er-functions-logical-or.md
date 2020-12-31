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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686981"
---
# <a name="or-er-function"></a><span data-ttu-id="1de96-103">OR ER 関数</span><span class="sxs-lookup"><span data-stu-id="1de96-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1de96-104">`OR` 関数は、指定したすべての条件が false である場合、**FALSE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="1de96-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="1de96-105">指定した任意の条件が true である場合、関数は **TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="1de96-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de96-106">構文</span><span class="sxs-lookup"><span data-stu-id="1de96-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="1de96-107">引数</span><span class="sxs-lookup"><span data-stu-id="1de96-107">Arguments</span></span>

<span data-ttu-id="1de96-108">`condition 1`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="1de96-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="1de96-109">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="1de96-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1de96-110">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="1de96-110">This argument is required.</span></span>

<span data-ttu-id="1de96-111">`condition N`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="1de96-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="1de96-112">テストする必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="1de96-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1de96-113">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="1de96-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1de96-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="1de96-114">Return values</span></span>

<span data-ttu-id="1de96-115">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="1de96-115">*Boolean*</span></span>

<span data-ttu-id="1de96-116">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="1de96-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="1de96-117">例</span><span class="sxs-lookup"><span data-stu-id="1de96-117">Example</span></span>

<span data-ttu-id="1de96-118">`OR (1=2, "a"="a")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="1de96-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1de96-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1de96-119">Additional resources</span></span>

[<span data-ttu-id="1de96-120">論理機能</span><span class="sxs-lookup"><span data-stu-id="1de96-120">Logical functions</span></span>](er-functions-category-logical.md)
