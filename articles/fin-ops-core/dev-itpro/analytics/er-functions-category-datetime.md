---
title: 日付と時刻のカテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる日時の関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 52b84f9b611f703fd390eca58c1364a4992bece2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561713"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="d9c81-103">日付と時刻のカテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="d9c81-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9c81-104">電子報告 (ER) 日時の関数を使用して、日付と時刻の値から情報を抽出し、操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="d9c81-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="d9c81-105">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="d9c81-106">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="d9c81-106">List of supported functions</span></span>

| <span data-ttu-id="d9c81-107">職務</span><span class="sxs-lookup"><span data-stu-id="d9c81-107">Function</span></span> | <span data-ttu-id="d9c81-108">説明</span><span class="sxs-lookup"><span data-stu-id="d9c81-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d9c81-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="d9c81-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="d9c81-110">この関数は、指定された開始日前後の指定された日数の *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="d9c81-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="d9c81-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="d9c81-112">この関数は、特定の日付値を指定された形式およびオプションで指定されたカルチャのテキストとして表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="d9c81-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d9c81-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="d9c81-114">この関数は、特定の日付/時刻値を指定された形式およびオプションで指定されたカルチャのテキストとして表す *文字列* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="d9c81-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="d9c81-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="d9c81-116">この関数は、指定された形式およびオプションで指定されたカルチャの特定のテキスト値から日付/時刻値に変換される *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="d9c81-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="d9c81-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="d9c81-118">この関数は、特定の日付値から協定世界時 (グリニッジ標準時 \[GMT\]) の日付/時刻値に変換された *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="d9c81-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="d9c81-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="d9c81-120">この関数は、指定された形式およびオプションで指定されたカルチャの特定のテキスト値から日付値に変換される *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="d9c81-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="d9c81-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="d9c81-122">この関数は、1 月 1 日から指定された日付までの日数を表す *整数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="d9c81-123">日数</span><span class="sxs-lookup"><span data-stu-id="d9c81-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="d9c81-124">この関数は、ある指定された日付から 2 番目の指定された日付までの日数を表す *整数* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="d9c81-125">Now</span><span class="sxs-lookup"><span data-stu-id="d9c81-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="d9c81-126">この関数は、現在のアプリケーション サーバーの日付と時刻を表す *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="d9c81-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="d9c81-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="d9c81-128">この関数は、**null** の日付 (1900 年 1 月 1 日) を表す *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="d9c81-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="d9c81-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="d9c81-130">この関数は、協定世界時の **null** の日付/時刻値 (1900 年 1 月 1 日) を表す *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="d9c81-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="d9c81-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="d9c81-132">この関数は、現在のアプリケーション セッションの日付と時刻を表す *日時* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="d9c81-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="d9c81-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="d9c81-134">この関数は、現在のアプリケーション セッションの日付を表す *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="d9c81-135">今日</span><span class="sxs-lookup"><span data-stu-id="d9c81-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="d9c81-136">この関数は、現在のアプリケーション サーバーの日付を表す *日付* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9c81-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d9c81-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d9c81-137">Additional resources</span></span>

[<span data-ttu-id="d9c81-138">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="d9c81-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d9c81-139">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="d9c81-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="d9c81-140">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="d9c81-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]