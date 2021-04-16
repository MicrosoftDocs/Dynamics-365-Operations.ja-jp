---
title: NOT ER 関数
description: このトピックでは、NOT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751719"
---
# <a name="not-er-function"></a><span data-ttu-id="bca60-103">NOT ER 関数</span><span class="sxs-lookup"><span data-stu-id="bca60-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bca60-104">`NOT` 関数は、指定された条件の取消論理値を *ブール* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="bca60-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca60-105">構文</span><span class="sxs-lookup"><span data-stu-id="bca60-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="bca60-106">引数</span><span class="sxs-lookup"><span data-stu-id="bca60-106">Arguments</span></span>

<span data-ttu-id="bca60-107">`condition`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="bca60-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="bca60-108">取り消す必要がある有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="bca60-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="bca60-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="bca60-109">Return values</span></span>

<span data-ttu-id="bca60-110">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="bca60-110">*Boolean*</span></span>

<span data-ttu-id="bca60-111">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="bca60-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="bca60-112">例</span><span class="sxs-lookup"><span data-stu-id="bca60-112">Example</span></span>

<span data-ttu-id="bca60-113">`NOT (TRUE)` は、**FALSE** 返します。</span><span class="sxs-lookup"><span data-stu-id="bca60-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bca60-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bca60-114">Additional resources</span></span>

[<span data-ttu-id="bca60-115">論理機能</span><span class="sxs-lookup"><span data-stu-id="bca60-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]