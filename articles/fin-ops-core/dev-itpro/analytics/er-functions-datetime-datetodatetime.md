---
title: DATETODATETIME ER 関数
description: このトピックでは、DATETODATETIME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746966"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="bb745-103">DATETODATETIME ER 関数</span><span class="sxs-lookup"><span data-stu-id="bb745-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb745-104">`DATETODATETIME` 関数は、特定の日付値から協定世界時 (グリニッジ標準時\[GMT\]) に変換された *DateTime* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="bb745-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb745-105">構文</span><span class="sxs-lookup"><span data-stu-id="bb745-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="bb745-106">引数</span><span class="sxs-lookup"><span data-stu-id="bb745-106">Arguments</span></span>

<span data-ttu-id="bb745-107">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="bb745-107">`date`: *Date*</span></span>

<span data-ttu-id="bb745-108">変換する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="bb745-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb745-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb745-109">Return values</span></span>

<span data-ttu-id="bb745-110">*日時*</span><span class="sxs-lookup"><span data-stu-id="bb745-110">*DateTime*</span></span>

<span data-ttu-id="bb745-111">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="bb745-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="bb745-112">例 1</span><span class="sxs-lookup"><span data-stu-id="bb745-112">Example 1</span></span>

<span data-ttu-id="bb745-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` は、現在の Microsoft Dynamics 365 Finance セッションの日付 2015年12月24日を **12/24/2015 12:00:00 AM** として返します。</span><span class="sxs-lookup"><span data-stu-id="bb745-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="bb745-114">この例では、**CompInfo** は、**Finance and Operations/Table** タイプの電子申告 (ER) データ ソースで、CompanyInfo テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="bb745-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="bb745-115">例 2</span><span class="sxs-lookup"><span data-stu-id="bb745-115">Example 2</span></span>

<span data-ttu-id="bb745-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` は、日時値 **2019 12:00:00 11/12 AM** を返します。</span><span class="sxs-lookup"><span data-stu-id="bb745-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb745-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bb745-117">Additional resources</span></span>

[<span data-ttu-id="bb745-118">日時の関数</span><span class="sxs-lookup"><span data-stu-id="bb745-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]