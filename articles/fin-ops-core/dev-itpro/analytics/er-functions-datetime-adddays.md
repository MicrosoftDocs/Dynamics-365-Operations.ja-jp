---
title: ADDDAYS ER 関数
description: このトピックでは、ADDDAYS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747062"
---
# <a name="adddays-er-function"></a><span data-ttu-id="26924-103">ADDDAYS ER 関数</span><span class="sxs-lookup"><span data-stu-id="26924-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26924-104">`ADDDAYS` 関数は、指定された開始日前後の指定された日数の *日時* 値を計算します。</span><span class="sxs-lookup"><span data-stu-id="26924-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="26924-105">構文</span><span class="sxs-lookup"><span data-stu-id="26924-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="26924-106">引数</span><span class="sxs-lookup"><span data-stu-id="26924-106">Arguments</span></span>

<span data-ttu-id="26924-107">`datetime`: *日時*</span><span class="sxs-lookup"><span data-stu-id="26924-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="26924-108">開始日を表す日付/時刻値。</span><span class="sxs-lookup"><span data-stu-id="26924-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="26924-109">`days`: *整数*</span><span class="sxs-lookup"><span data-stu-id="26924-109">`days`: *Integer*</span></span>

<span data-ttu-id="26924-110">`datetime` の前後の日数。</span><span class="sxs-lookup"><span data-stu-id="26924-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="26924-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="26924-111">Return values</span></span>

<span data-ttu-id="26924-112">*日時*</span><span class="sxs-lookup"><span data-stu-id="26924-112">*DateTime*</span></span>

<span data-ttu-id="26924-113">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="26924-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26924-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="26924-114">Usage notes</span></span>

<span data-ttu-id="26924-115">`days` の正の値は、未来の日付になります。</span><span class="sxs-lookup"><span data-stu-id="26924-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="26924-116">負の値は、過去の日付になります。</span><span class="sxs-lookup"><span data-stu-id="26924-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="26924-117">例 1</span><span class="sxs-lookup"><span data-stu-id="26924-117">Example 1</span></span>

<span data-ttu-id="26924-118">`ADDDAYS (NOW(), 7)` は、7 日後の日付と時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="26924-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="26924-119">例 2</span><span class="sxs-lookup"><span data-stu-id="26924-119">Example 2</span></span>

<span data-ttu-id="26924-120">`ADDDAYS (NOW(), -3)` は、3 日前の日付と時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="26924-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26924-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="26924-121">Additional resources</span></span>

[<span data-ttu-id="26924-122">日時の関数</span><span class="sxs-lookup"><span data-stu-id="26924-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]