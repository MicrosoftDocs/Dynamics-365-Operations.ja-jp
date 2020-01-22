---
title: DATETODATETIME ER 関数
description: このトピックでは、DATETODATETIME 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916387"
---
# <span data-ttu-id="0d55b-103"><a name="DATETODATETIME">DATETODATETIME ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="0d55b-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d55b-104">`DATETODATETIME` 関数は、特定の日付値から協定世界時 (グリニッジ標準時\[GMT\]) に変換された *DateTime* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="0d55b-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d55b-105">構文</span><span class="sxs-lookup"><span data-stu-id="0d55b-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="0d55b-106">引数</span><span class="sxs-lookup"><span data-stu-id="0d55b-106">Arguments</span></span>

<span data-ttu-id="0d55b-107">`date`: *日付*</span><span class="sxs-lookup"><span data-stu-id="0d55b-107">`date`: *Date*</span></span>

<span data-ttu-id="0d55b-108">変換する日付を表す日付値。</span><span class="sxs-lookup"><span data-stu-id="0d55b-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d55b-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d55b-109">Return values</span></span>

<span data-ttu-id="0d55b-110">*日時*</span><span class="sxs-lookup"><span data-stu-id="0d55b-110">*DateTime*</span></span>

<span data-ttu-id="0d55b-111">結果日時値。</span><span class="sxs-lookup"><span data-stu-id="0d55b-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0d55b-112">例 1</span><span class="sxs-lookup"><span data-stu-id="0d55b-112">Example 1</span></span>

<span data-ttu-id="0d55b-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` は、現在の Microsoft Dynamics 365 Finance セッションの日付 2015年12月24日を**12/24/2015 12:00:00 AM**として返します。</span><span class="sxs-lookup"><span data-stu-id="0d55b-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="0d55b-114">この例では、**CompInfo** は、**Finance and Operations/Table** タイプの電子申告 (ER) データ ソースで、CompanyInfo テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="0d55b-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="0d55b-115">例 2</span><span class="sxs-lookup"><span data-stu-id="0d55b-115">Example 2</span></span>

<span data-ttu-id="0d55b-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` は、日時値 **2019 12:00:00 11/12 AM** を返します。</span><span class="sxs-lookup"><span data-stu-id="0d55b-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d55b-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0d55b-117">Additional resources</span></span>

[<span data-ttu-id="0d55b-118">日時の関数</span><span class="sxs-lookup"><span data-stu-id="0d55b-118">Date and time functions</span></span>](er-functions-category-datetime.md)
