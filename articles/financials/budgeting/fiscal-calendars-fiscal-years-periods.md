---
title: "会計カレンダー、会計年度期間、および会計年度"
description: "この記事は、法人、固定資産、予算作成で会計カレンダー、会計年度、会計期間を活用する方法について説明します。"
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 33c358e5f522500cea05c9f85a84c519f8c7b845
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a><span data-ttu-id="f6094-103">会計カレンダー、会計年度期間、および会計年度</span><span class="sxs-lookup"><span data-stu-id="f6094-103">Fiscal calendars, fiscal years, and periods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6094-104">この記事は、法人、固定資産、予算作成で会計カレンダー、会計年度、会計期間を活用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6094-104">This article discusses fiscal calendars, fiscal years and periods and how to utilize them for legal entities, fixed assets and budgeting.</span></span>

<span data-ttu-id="f6094-105">会計カレンダーは、組織の財務活動のためのフレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="f6094-105">Fiscal calendars provide a framework for the financial activity of an organization.</span></span> <span data-ttu-id="f6094-106">各会計カレンダーには1 つ以上の会計年度が含まれ、各会計年度には複数の期間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f6094-106">Each fiscal calendar contains one or more fiscal years, and each fiscal year contains multiple periods.</span></span> <span data-ttu-id="f6094-107">会計カレンダーは 1 月 1 日から 12 月 31 日の暦年か、または選択した任意の日にちに基づくことができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-107">Fiscal calendars can be based on a January 1 to December 31 calendar year, or on any dates that you select.</span></span> <span data-ttu-id="f6094-108">たとえば、1 年うちの 7 月 1 日で始まり、次の年の 6 月 30 日で終わる会計カレンダーを選択する組織もあります。</span><span class="sxs-lookup"><span data-stu-id="f6094-108">For example, some organizations select a fiscal calendar that starts on July 1 of one year and ends on June 30 of the following year.</span></span> 

<span data-ttu-id="f6094-109">作成できる会計カレンダーの数に制限はありません。また 1 つの会計カレンダーに対して作成できる会計年度の数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="f6094-109">There is no limit to the number of fiscal calendars that you can create, and no limit to the number of fiscal years that can be created for a fiscal calendar.</span></span> <span data-ttu-id="f6094-110">各会計カレンダーは、自身の組織には関係なく、組織内の複数の法人が使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-110">Each fiscal calendar is independent of your organization, and can be used by multiple legal entities in the organization.</span></span> <span data-ttu-id="f6094-111">たとえば、組織に 8 つの部門があり、各部門が別々の法人です。</span><span class="sxs-lookup"><span data-stu-id="f6094-111">For example, an organization has eight departments and each department is a separate legal entity.</span></span> <span data-ttu-id="f6094-112">これらのうちの 5 つの法人が同じ会計カレンダーを共有し、3 つの法人が異なる会計カレンダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6094-112">Five of them share the same fiscal calendar and three use different fiscal calendars.</span></span> <span data-ttu-id="f6094-113">同じ会計カレンダーを共有する 5 つの法人には 1 つの会計カレンダーを作成し、残りの法人には別々の会計カレンダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-113">You can create one fiscal calendar for the five legal entities that share the same fiscal calendar, and then create separate fiscal calendars for the other legal entities.</span></span>

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a><span data-ttu-id="f6094-114">会計カレンダー、会計年度、および期間の作成</span><span class="sxs-lookup"><span data-stu-id="f6094-114">Create fiscal calendars, fiscal years, and periods</span></span>
<span data-ttu-id="f6094-115">会計カレンダー、会計年度、および期間の作成と削除を [会計カレンダー] ページで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-115">You can create and delete fiscal calendars, fiscal years, and periods on the Fiscal calendars page.</span></span> <span data-ttu-id="f6094-116">既存の期間を分割して、会計年度の決算に使用できる決算期間を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-116">You can also divide existing periods and create closing periods that can be used to close a fiscal year.</span></span> 

<span data-ttu-id="f6094-117">決算期間は、会計年度の終了時に生成される一般会計トランザクションを区切るために使用します。</span><span class="sxs-lookup"><span data-stu-id="f6094-117">A closing period is used to separate general ledger transactions that are generated when a fiscal year is closed.</span></span> <span data-ttu-id="f6094-118">決算トランザクションが 1 つの会計期間にある場合は、異なるタイプの決算エントリを含めるか除外する財務諸表を作成する方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="f6094-118">When the closing transactions are in one fiscal period, it is easier to create financial statements that either include or exclude different types of closing entries.</span></span> <span data-ttu-id="f6094-119">会計年度が 12 の会計年度期間に分けられている場合、決算期間は通常 13 番目の期間です。</span><span class="sxs-lookup"><span data-stu-id="f6094-119">If a fiscal year is divided into 12 fiscal periods, the closing period is usually the 13th period.</span></span> <span data-ttu-id="f6094-120">ただし、決算期間は、ステータスが [オープン] になっているすべての期間から作成できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-120">However, a closing period can be created from any period that has a status of Open.</span></span> 

<span data-ttu-id="f6094-121">決算期間の作成時には、ステータスが [オープン] になっており、使用する日付が含まれている期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6094-121">When you create a closing period, select a period that has a status of Open and that has the dates that you want to use.</span></span> <span data-ttu-id="f6094-122">新しい決済期間には、既存期間の開始日と終了日がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f6094-122">The new closing period will copy the starting and ending dates from the existing period.</span></span> <span data-ttu-id="f6094-123">元の期間も引き続き残ります。</span><span class="sxs-lookup"><span data-stu-id="f6094-123">The original period will continue to exist.</span></span> <span data-ttu-id="f6094-124">たとえば、会計年度の最終期間にあたり、なおかつ 8 月 1 日から 8 月 31 日を含む [期間 12] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6094-124">For example, you select Period 12, which is the last period in the fiscal year, and that has dates of August 1 through August 31.</span></span> <span data-ttu-id="f6094-125">決算期間に「決算」といった名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f6094-125">You enter a name for the closing period, such as Close.</span></span> <span data-ttu-id="f6094-126">新しい決算期間を作成すると、元の期間と決算期間が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f6094-126">After you create the new closing period, you now have the original period and the closing period.</span></span> <span data-ttu-id="f6094-127">両期間とも 8 月 1 日に始まり、8 月 31 日に終了します。</span><span class="sxs-lookup"><span data-stu-id="f6094-127">Both have dates that start on August 1 and end on August 31.</span></span>

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a><span data-ttu-id="f6094-128">元帳、固定資産、および予算サイクル用の会計カレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6094-128">Select fiscal calendars for ledgers, fixed assets, and budget cycles</span></span>
<span data-ttu-id="f6094-129">会計カレンダーは、固定資産減価償却、財務トランザクションおよび予算サイクルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f6094-129">Fiscal calendars are used with fixed asset depreciation, financial transactions, and budget cycles.</span></span> <span data-ttu-id="f6094-130">会計カレンダーを作成すると、複数の目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-130">When you create a fiscal calendar, you can use it for multiple purposes.</span></span> <span data-ttu-id="f6094-131">価値モデルまたは減価償却簿用の会計カレンダーを選択して、それを固定資産カレンダーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-131">You can select a fiscal calendar for a value model or depreciation book to make it a fixed asset calendar.</span></span> <span data-ttu-id="f6094-132">元帳用の会計カレンダーを選択して、それを元帳カレンダーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-132">You can select a fiscal calendar for a ledger to make it a ledger calendar.</span></span> <span data-ttu-id="f6094-133">また、予算サイクル用の会計カレンダーを選択して、それを予算カレンダーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-133">And you can select a fiscal calendar for a budget cycle to make it a budget calendar.</span></span> <span data-ttu-id="f6094-134">これらのすべてに対して、同じ会計カレンダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-134">You can use the same fiscal calendar for all of these.</span></span>

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a><span data-ttu-id="f6094-135">自身の法人用の会計カレンダーの選択</span><span class="sxs-lookup"><span data-stu-id="f6094-135">Select a fiscal calendar for your legal entity</span></span>

<span data-ttu-id="f6094-136">"元帳" フォームで、自身の法人の元帳に使用する会計カレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f6094-136">Select the fiscal calendar that you want to use for the ledger for your legal entity in the Ledger form.</span></span> <span data-ttu-id="f6094-137">会計カレンダーは、[元帳] ページで、すべての法人に対して選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6094-137">A fiscal calendar must be selected on the Ledger page for every legal entity.</span></span> <span data-ttu-id="f6094-138">会計カレンダーの選択後は、元帳カレンダーのページで、会計年度のあらゆる期間に対して、期間のステータスとアクセス許可を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-138">After a fiscal calendar is selected, you can set up period statuses and permissions on the Ledger calendar page for any of the periods that are part of a fiscal year.</span></span>

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a><span data-ttu-id="f6094-139">固定資産用の会計カレンダーの選択</span><span class="sxs-lookup"><span data-stu-id="f6094-139">Select a fiscal calendar for fixed assets</span></span>

<span data-ttu-id="f6094-140">価値モデルまたは減価償却簿用の会計カレンダーを選択することができます。この会計カレンダーは、選択した価値モデルまたは減価償却簿を使用する固定資産によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f6094-140">You can select a fiscal calendar for a value model or depreciation book, and that fiscal calendar will be used by the fixed assets that use the selected value model or depreciation book.</span></span> <span data-ttu-id="f6094-141">会計カレンダーのページで定義されているすべての会計カレンダーから選択できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-141">You can select from any fiscal calendar that is defined on the Fiscal calendars page.</span></span>

### <a name="define-budget-cycle-time-spans"></a><span data-ttu-id="f6094-142">予算サイクル期間の定義</span><span class="sxs-lookup"><span data-stu-id="f6094-142">Define budget cycle time spans</span></span>

<span data-ttu-id="f6094-143">予算サイクルとは、予算が使用される期間の長さです。</span><span class="sxs-lookup"><span data-stu-id="f6094-143">Budget cycles are the length of time during which a budget is used.</span></span> <span data-ttu-id="f6094-144">予算サイクルには、2 年に一度の 2 年間の予算サイクル、または 3 年に一度の 3 年間の予算サイクルなど、1 つ以上の会計年度を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f6094-144">Budget cycles can include part of a fiscal year or multiple fiscal years, such as a biennial budget cycle of two years or a triennial budget cycle of three years.</span></span> <span data-ttu-id="f6094-145">予算サイクル期間は、予算サイクルに含まれる期間の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f6094-145">The budget cycle time span defines the number of periods that are included in the budget cycle.</span></span> <span data-ttu-id="f6094-146">予算サイクル期間を指定するには、[予算サイクル期間] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6094-146">To specify the budget cycle time span, use the Budget cycle time spans page.</span></span>

## <a name="maintain-periods-for-your-organization"></a><span data-ttu-id="f6094-147">組織の期間の管理</span><span class="sxs-lookup"><span data-stu-id="f6094-147">Maintain periods for your organization</span></span>
<span data-ttu-id="f6094-148">元帳カレンダーのページを使用して、組織で使用される会計カレンダー、会計年度、および期間の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-148">You can use the Ledger calendar page to view the details of the fiscal calendar, fiscal years, and periods used by your organization.</span></span> <span data-ttu-id="f6094-149">また、期間の状態を変更して、会計トランザクションを期間に転記できるユーザーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f6094-149">You can also change the status of the periods and select which users can post accounting transactions to periods.</span></span> <span data-ttu-id="f6094-150">たとえば、新しい期間の開始時に、ユーザーの 1 つのグループが前の期間の財務トランザクションの転記を終了し、他のグループは新しい期間でのみ作業する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f6094-150">For example, at the start of a new period, you might want a group of users to finish posting financial transactions in the previous period, while other groups work only in the new period.</span></span>






