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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9b937e7fae3e90d1a87196fab653dfac8e94179
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682392"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="fa9a3-103">DAYOFYEAR ER 関数</span><span class="sxs-lookup"><span data-stu-id="fa9a3-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa9a3-104">`DAYOFYEAR` 関数は、1 月 1 日から指定された日までの日数を表す *整数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="fa9a3-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9a3-105">構文</span><span class="sxs-lookup"><span data-stu-id="fa9a3-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="fa9a3-106">引数</span><span class="sxs-lookup"><span data-stu-id="fa9a3-106">Arguments</span></span>

<span data-ttu-id="fa9a3-107">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="fa9a3-107">`date`: *Date*</span></span>

<span data-ttu-id="fa9a3-108">日数の計算に使用する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="fa9a3-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="fa9a3-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa9a3-109">Return values</span></span>

<span data-ttu-id="fa9a3-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="fa9a3-110">*Integer*</span></span>

<span data-ttu-id="fa9a3-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="fa9a3-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="fa9a3-112">例 1</span><span class="sxs-lookup"><span data-stu-id="fa9a3-112">Example 1</span></span>

<span data-ttu-id="fa9a3-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` は、**61** を返します。</span><span class="sxs-lookup"><span data-stu-id="fa9a3-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fa9a3-114">例 2</span><span class="sxs-lookup"><span data-stu-id="fa9a3-114">Example 2</span></span>

<span data-ttu-id="fa9a3-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="fa9a3-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa9a3-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fa9a3-116">Additional resources</span></span>

[<span data-ttu-id="fa9a3-117">日時の関数</span><span class="sxs-lookup"><span data-stu-id="fa9a3-117">Date and time functions</span></span>](er-functions-category-datetime.md)
