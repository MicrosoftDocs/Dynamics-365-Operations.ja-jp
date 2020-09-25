---
title: DAYOFYEAR ER 関数
description: このトピックでは、DAYOFYEAR 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745492"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="c6104-103">DAYOFYEAR ER 関数</span><span class="sxs-lookup"><span data-stu-id="c6104-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6104-104">`DAYOFYEAR` 関数は、1 月 1 日から指定された日までの日数を表す*整数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="c6104-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6104-105">構文</span><span class="sxs-lookup"><span data-stu-id="c6104-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="c6104-106">引数</span><span class="sxs-lookup"><span data-stu-id="c6104-106">Arguments</span></span>

<span data-ttu-id="c6104-107">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="c6104-107">`date`: *Date*</span></span>

<span data-ttu-id="c6104-108">日数の計算に使用する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="c6104-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6104-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="c6104-109">Return values</span></span>

<span data-ttu-id="c6104-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="c6104-110">*Integer*</span></span>

<span data-ttu-id="c6104-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="c6104-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c6104-112">例 1</span><span class="sxs-lookup"><span data-stu-id="c6104-112">Example 1</span></span>

<span data-ttu-id="c6104-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` は、**61** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6104-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c6104-114">例 2</span><span class="sxs-lookup"><span data-stu-id="c6104-114">Example 2</span></span>

<span data-ttu-id="c6104-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6104-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6104-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6104-116">Additional resources</span></span>

[<span data-ttu-id="c6104-117">日時の関数</span><span class="sxs-lookup"><span data-stu-id="c6104-117">Date and time functions</span></span>](er-functions-category-datetime.md)
