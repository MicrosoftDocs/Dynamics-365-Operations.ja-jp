---
title: MOD_97 ER 関数
description: このトピックでは、MOD_97 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070532"
---
# <span data-ttu-id="a4bcb-103"><a name="MOD_97">MOD_97 ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="a4bcb-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4bcb-104">この `MOD_97` 関数は、指定された請求書番号の桁数に基づいて、MOD97 式として債権者参照を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="a4bcb-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bcb-105">構文</span><span class="sxs-lookup"><span data-stu-id="a4bcb-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="a4bcb-106">引数</span><span class="sxs-lookup"><span data-stu-id="a4bcb-106">Arguments</span></span>

<span data-ttu-id="a4bcb-107">`invoice number digits`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a4bcb-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="a4bcb-108">請求書番号の桁数を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="a4bcb-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="a4bcb-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="a4bcb-109">Return values</span></span>

<span data-ttu-id="a4bcb-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="a4bcb-110">*String*</span></span>

<span data-ttu-id="a4bcb-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="a4bcb-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a4bcb-112">例</span><span class="sxs-lookup"><span data-stu-id="a4bcb-112">Example</span></span>

<span data-ttu-id="a4bcb-113">`MOD_97 ("VEND-200002")` は、**"20000285"** を返します。</span><span class="sxs-lookup"><span data-stu-id="a4bcb-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4bcb-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a4bcb-114">Additional resources</span></span>

[<span data-ttu-id="a4bcb-115">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="a4bcb-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
