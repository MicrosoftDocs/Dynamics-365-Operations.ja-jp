---
title: NOT ER 関数
description: このトピックでは、NOT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041725"
---
# <span data-ttu-id="6595e-103"><a name="NOT">NOT ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="6595e-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6595e-104">`NOT` 関数は、指定された条件の取消論理値を*ブール*値として返します。</span><span class="sxs-lookup"><span data-stu-id="6595e-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6595e-105">構文</span><span class="sxs-lookup"><span data-stu-id="6595e-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="6595e-106">引数</span><span class="sxs-lookup"><span data-stu-id="6595e-106">Arguments</span></span>

<span data-ttu-id="6595e-107">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="6595e-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="6595e-108">取り消す必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="6595e-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="6595e-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6595e-109">Return values</span></span>

<span data-ttu-id="6595e-110">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="6595e-110">*Boolean*</span></span>

<span data-ttu-id="6595e-111">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="6595e-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="6595e-112">例</span><span class="sxs-lookup"><span data-stu-id="6595e-112">Example</span></span>

<span data-ttu-id="6595e-113">`NOT (TRUE)` は、**FALSE** 返します。</span><span class="sxs-lookup"><span data-stu-id="6595e-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6595e-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6595e-114">Additional resources</span></span>

[<span data-ttu-id="6595e-115">論理機能</span><span class="sxs-lookup"><span data-stu-id="6595e-115">Logical functions</span></span>](er-functions-category-logical.md)
