---
title: 日付と時刻のフィールドを理解する
description: Microsoft Dynamics 365 Human Resources で日付と時刻フィールドを使用する際の予想事項を把握します。 Human Resources、外部ソース、または Common Data Service のフォームで日付と時刻データを操作する際に予想される内容を明確にします。
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430098"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="01790-104">日付と時刻のフィールドを理解する</span><span class="sxs-lookup"><span data-stu-id="01790-104">Understand Date and Time fields</span></span>

<span data-ttu-id="01790-105">**日付と時刻**フィールドは、Dynamics 365 Human Resources の基本的な概念です。</span><span class="sxs-lookup"><span data-stu-id="01790-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="01790-106">Dynamics 365 Human Resources フォーム、Common Data Service、および外部ソースにおいて**日付と時刻**データを操作する方法を理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="01790-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="01790-107">日付フィールドと日付と時刻フィールドのデータ型の違いを理解する</span><span class="sxs-lookup"><span data-stu-id="01790-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="01790-108">**日付と時刻**フィールドにはタイム ゾーン情報が含まれますが、**日付**フィールドには含まれません。</span><span class="sxs-lookup"><span data-stu-id="01790-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="01790-109">**日付**フィールドには、どの場所でも同じ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01790-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="01790-110">日付を**日付**フィールドに入力すると、Human Resources によって同じ日付がデータベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="01790-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="01790-111">**日付と時刻**フィールドにデータを表示する場合、**ユーザー オプション** フォームで設定されたユーザーのタイム ゾーンに基づいて、Human Resources によって日付と時刻が調整されます (**共通 > 設定 > ユーザー オプション**)。</span><span class="sxs-lookup"><span data-stu-id="01790-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="01790-112">フィールドに入力した日付と時刻の情報は、データベースに書き込まれた情報とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="01790-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="01790-113">[![ユーザー オプション フォーム](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="01790-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="01790-114">フォームの日付と時刻のフィールドを理解する</span><span class="sxs-lookup"><span data-stu-id="01790-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="01790-115">**日付と時刻**フィールドにデータを入力する際、ユーザーのタイム ゾーンが協定世界時 (UTC) に設定されていないと、画面に表示されるデータはデータベースに格納されているデータとは異なります。</span><span class="sxs-lookup"><span data-stu-id="01790-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="01790-116">**日付と時刻**フィールドのデータは、常に UTC として保存されます。</span><span class="sxs-lookup"><span data-stu-id="01790-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="01790-117">[![作業者フォーム](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="01790-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="01790-118">データベースの日付と時刻のフィールドを理解する</span><span class="sxs-lookup"><span data-stu-id="01790-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="01790-119">Human Resources が**日付と時刻**の値をデータベースに書き込む際、データを UTC で保存します。</span><span class="sxs-lookup"><span data-stu-id="01790-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="01790-120">これにより、ユーザーは、ユーザー オプションで定義されたタイムゾーンに関連する**日付と時刻**のデータを参照できます。</span><span class="sxs-lookup"><span data-stu-id="01790-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="01790-121">上記の例では、開始時刻は特定の日付ではなく特定時点の時刻です。</span><span class="sxs-lookup"><span data-stu-id="01790-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="01790-122">ログインしているユーザーのタイム ゾーンを GMT + 12:00 から GMT UTC に変更すると、作成された同じレコードが 05/01/2019 12:00:00 ではなく 04/30/2019 12:00:00 と表示されます。</span><span class="sxs-lookup"><span data-stu-id="01790-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="01790-123">次の例では、従業員 000724 の雇用が、タイム ゾーンに関係なく同時に有効になります。</span><span class="sxs-lookup"><span data-stu-id="01790-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="01790-124">従業員は GMT タイム ゾーンの 04/30/2019 で有効になり、GMT + 12:00 タイムゾーンの 05/01/2019 と同じになります。</span><span class="sxs-lookup"><span data-stu-id="01790-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="01790-125">どちらも、特定の日付ではなく、同じ特定時点を参照します。</span><span class="sxs-lookup"><span data-stu-id="01790-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="01790-126">[![作業者フォーム](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="01790-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="01790-127">データ管理フレームワーク、Excel、Common Data Service、および Power BI における日付と時刻のデータ</span><span class="sxs-lookup"><span data-stu-id="01790-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="01790-128">データ管理フレームワーク、Excel アドイン、Common Data Service、および Power BI レポートは、データベース レベルでデータを直接操作できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="01790-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="01790-129">**日付と時刻**のデータをユーザーのタイム ゾーンに調整するクライアントは存在しないため、**日付と時刻**の値はすべて UTC となり、データを入力したり表示したりするときに、誤った推測につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="01790-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="01790-130">DMF、Excel、または Common Data Service を介して送信された**日付と時刻**データは、データベースによって UTC と見なされます。</span><span class="sxs-lookup"><span data-stu-id="01790-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="01790-131">データを表示するユーザーのユーザー タイム ゾーンが UTC に設定されていないため、送信された**日付と時間**の値が期待どおりに表示されない場合、混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="01790-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="01790-132">データがエクスポートされると、同じことが逆に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="01790-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="01790-133">エクスポートされた DMF エンティティの**日付と時刻**データは、Dynamics クライアントに表示されるものと異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="01790-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="01790-134">DMF などの外部ソースを使用してデータを表示または作成するため場合、ユーザーのコンピューターのタイム ゾーンや現在のユーザーのタイム ゾーンの設定に関係なく、**日付と時刻**の値は既定で UTC であると見なされる点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="01790-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="01790-135">同じレコードが異なる製品領域に表示されている例</span><span class="sxs-lookup"><span data-stu-id="01790-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="01790-136">**UTC に設定されているユーザー タイム ゾーンのある Human Resources**</span><span class="sxs-lookup"><span data-stu-id="01790-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="01790-137">[![作業者フォーム](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="01790-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="01790-138">**GMT +12:00 に設定されているユーザー タイム ゾーンのある Human Resources**</span><span class="sxs-lookup"><span data-stu-id="01790-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="01790-139">[![作業者フォーム](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="01790-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="01790-140">**OData を介した Excel**</span><span class="sxs-lookup"><span data-stu-id="01790-140">**Excel Via OData**</span></span>

<span data-ttu-id="01790-141">[![OData を介した Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="01790-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="01790-142">**DMF ステージング**</span><span class="sxs-lookup"><span data-stu-id="01790-142">**DMF Staging**</span></span>

<span data-ttu-id="01790-143">[![DMF ステージング](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="01790-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="01790-144">**DMF エクスポート**</span><span class="sxs-lookup"><span data-stu-id="01790-144">**DMF Export**</span></span>

<span data-ttu-id="01790-145">[![DMF ステージング](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="01790-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="01790-146">**Common Data Service を介した Excel**</span><span class="sxs-lookup"><span data-stu-id="01790-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="01790-147">[![Common Data Service を介した Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="01790-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="01790-148">参照</span><span class="sxs-lookup"><span data-stu-id="01790-148">See also</span></span>

[<span data-ttu-id="01790-149">日付と時刻データ</span><span class="sxs-lookup"><span data-stu-id="01790-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="01790-150">ユーザーの優先タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="01790-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
