---
title: DAYS ER 関数
description: このトピックでは、DAYS 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 4f8c12a22f7654285d5598064473bf86689ed207
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916295"
---
# <span data-ttu-id="62d16-103"><a name="DAYS">DAYS ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="62d16-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62d16-104">`DAYS` 関数は、ある指定された日付から 2 番目の指定された日付までの日数を表す*整数*値を返します。</span><span class="sxs-lookup"><span data-stu-id="62d16-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d16-105">構文</span><span class="sxs-lookup"><span data-stu-id="62d16-105">Syntax</span></span>

```
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="62d16-106">引数</span><span class="sxs-lookup"><span data-stu-id="62d16-106">Arguments</span></span>

<span data-ttu-id="62d16-107">`date 1`: *日付*</span><span class="sxs-lookup"><span data-stu-id="62d16-107">`date 1`: *Date*</span></span>

<span data-ttu-id="62d16-108">日数の計算の開始日を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="62d16-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="62d16-109">`date 2`: *日付*</span><span class="sxs-lookup"><span data-stu-id="62d16-109">`date 2`: *Date*</span></span>

<span data-ttu-id="62d16-110">日数の計算の終了日を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="62d16-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="62d16-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="62d16-111">Return values</span></span>

<span data-ttu-id="62d16-112">*整数*</span><span class="sxs-lookup"><span data-stu-id="62d16-112">*Integer*</span></span>

<span data-ttu-id="62d16-113">結果数値。</span><span class="sxs-lookup"><span data-stu-id="62d16-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="62d16-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="62d16-114">Usage notes</span></span>

<span data-ttu-id="62d16-115">`DAYS` 関数は、最初の日付が 2 番目の日付より遅い場合は正の値を返し、最初の日付が 2 番目の日付と同じである場合は **0** (ゼロ) を返します。最初の日付が 2 番目の日付より早い場合は、負の値を返します。</span><span class="sxs-lookup"><span data-stu-id="62d16-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="62d16-116">例</span><span class="sxs-lookup"><span data-stu-id="62d16-116">Example</span></span>

<span data-ttu-id="62d16-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` は、**-1** を返します。</span><span class="sxs-lookup"><span data-stu-id="62d16-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62d16-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="62d16-118">Additional resources</span></span>

[<span data-ttu-id="62d16-119">日時の関数</span><span class="sxs-lookup"><span data-stu-id="62d16-119">Date and time functions</span></span>](er-functions-category-datetime.md)
