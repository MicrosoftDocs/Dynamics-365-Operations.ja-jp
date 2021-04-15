---
title: 日付と時刻のフィールドを理解する
description: Microsoft Dynamics 365 Human Resources で日付と時刻フィールドを使用する際の予想事項を把握します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802434"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="31109-103">日付と時刻のフィールドの理解</span><span class="sxs-lookup"><span data-stu-id="31109-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="31109-104">**日付と時刻** フィールドは、Dynamics 365 Human Resources の基本的な概念です。</span><span class="sxs-lookup"><span data-stu-id="31109-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="31109-105">フォーム、Dataverse、外部ソースにおいて **日付と時刻** データを操作する方法を理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="31109-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="31109-106">日付フィールドと日付と時刻フィールドのデータ型の違いを理解する</span><span class="sxs-lookup"><span data-stu-id="31109-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="31109-107">**日付と時刻** フィールドにはタイム ゾーン情報が含まれますが、**日付** フィールドには含まれません。</span><span class="sxs-lookup"><span data-stu-id="31109-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="31109-108">**日付** フィールドには、どの場所でも同じ情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="31109-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="31109-109">日付を **日付** フィールドに入力すると、Human Resources によって同じ日付がデータベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="31109-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="31109-110">**日付と時刻** フィールドにデータを表示する場合、**ユーザー オプション** フォームで設定されたユーザーのタイム ゾーンに基づいて、Human Resources によって日付と時刻が調整されます (**共通 > 設定 > ユーザー オプション**)。</span><span class="sxs-lookup"><span data-stu-id="31109-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="31109-111">フィールドに入力した日付と時刻の情報は、データベースに書き込まれた情報とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="31109-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="31109-112">[![ユーザー オプション フォーム](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="31109-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="31109-113">フォームの日付と時刻のフィールドを理解する</span><span class="sxs-lookup"><span data-stu-id="31109-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="31109-114">ユーザーのタイムゾーンが協定世界時 (UTC) に設定されていない場合、画面に表示される **日付と時刻** データはデータベースに保存されているデータとは異なります。</span><span class="sxs-lookup"><span data-stu-id="31109-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="31109-115">**日付と時刻** フィールドのデータは、常に UTC として保存されます。</span><span class="sxs-lookup"><span data-stu-id="31109-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="31109-116">[![作業者フォーム UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="31109-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="31109-117">データベースの日付と時刻のフィールドを理解する</span><span class="sxs-lookup"><span data-stu-id="31109-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="31109-118">Human Resources が **日付と時刻** の値をデータベースに書き込む際、データを UTC で保存します。</span><span class="sxs-lookup"><span data-stu-id="31109-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="31109-119">これにより、ユーザーは、ユーザー オプションで定義されたタイムゾーンに関連する **日付と時刻** のデータを参照できます。</span><span class="sxs-lookup"><span data-stu-id="31109-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="31109-120">上記の例では、開始時刻は特定の日付ではなく特定時点の時刻です。</span><span class="sxs-lookup"><span data-stu-id="31109-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="31109-121">ログインしているユーザーのタイム ゾーンを [GMT +12:00] から [GMT UTC] に変更すると、作成されたレコードが [05/01/2019 12:00:00] ではなく [04/30/2019 12:00:00] と表示されます。</span><span class="sxs-lookup"><span data-stu-id="31109-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="31109-122">次の例では、従業員 000724 の雇用が、タイム ゾーンに関係なく同時に有効になります。</span><span class="sxs-lookup"><span data-stu-id="31109-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="31109-123">従業員は GMT タイム ゾーンの 04/30/2019 で有効になり、GMT + 12:00 タイムゾーンの 05/01/2019 と同じになります。</span><span class="sxs-lookup"><span data-stu-id="31109-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="31109-124">どちらも、特定の日付ではなく、同じ特定時点を参照します。</span><span class="sxs-lookup"><span data-stu-id="31109-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="31109-125">[![作業者フォーム GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="31109-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="31109-126">データ管理フレームワーク、Excel、Dataverse、および Power BI における日付と時刻のデータ</span><span class="sxs-lookup"><span data-stu-id="31109-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="31109-127">データ管理フレームワーク、Excel アドイン、Dataverse、および Power BI レポートは、データベース レベルでデータを直接操作できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="31109-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="31109-128">**日付と時刻** のデータをユーザーのタイム ゾーンに調整するクライアントは存在しないため、**日付と時刻** の値はすべて UTC となり、データの入力や表示の際に誤った認識につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="31109-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="31109-129">DMF、Excel、 Dataverse を介して送信された **日付と時刻** データは、データベースによって UTC と見なされます。</span><span class="sxs-lookup"><span data-stu-id="31109-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="31109-130">データを表示するユーザーのユーザー タイム ゾーンが UTC に設定されていないため、送信された **日付と時間** の値が期待どおりに表示されない場合、混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="31109-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="31109-131">データがエクスポートされると、同じことが逆に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="31109-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="31109-132">エクスポートされた DMF エンティティの **日付と時刻** データは、Dynamics クライアントに表示されるものとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="31109-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="31109-133">DMF などの外部ソースを使用してデータを表示または作成する場合、ユーザーのコンピューターのタイム ゾーンや現在のユーザーのタイム ゾーンの設定に関係なく、**日付と時刻** の値は既定で UTC であると見なされる点にご注意ください。</span><span class="sxs-lookup"><span data-stu-id="31109-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="31109-134">同じレコードが異なる製品領域に表示されている例</span><span class="sxs-lookup"><span data-stu-id="31109-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="31109-135">**UTC に設定されているユーザー タイム ゾーンのある Human Resources**</span><span class="sxs-lookup"><span data-stu-id="31109-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="31109-136">[![ワーカーのフォームを UTC に設定](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="31109-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="31109-137">**GMT +12:00 に設定されているユーザー タイム ゾーンのある Human Resources**</span><span class="sxs-lookup"><span data-stu-id="31109-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="31109-138">[![ワーカーのフォームを GMT に設定](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="31109-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="31109-139">**OData を介した Excel**</span><span class="sxs-lookup"><span data-stu-id="31109-139">**Excel Via OData**</span></span>

<span data-ttu-id="31109-140">[![OData を介した Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="31109-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="31109-141">**DMF ステージング**</span><span class="sxs-lookup"><span data-stu-id="31109-141">**DMF Staging**</span></span>

<span data-ttu-id="31109-142">[![DMF ステージング](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="31109-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="31109-143">**DMF エクスポート**</span><span class="sxs-lookup"><span data-stu-id="31109-143">**DMF Export**</span></span>

<span data-ttu-id="31109-144">[![DMF エクスポート](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="31109-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="31109-145">**Dataverse を介した Excel**</span><span class="sxs-lookup"><span data-stu-id="31109-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="31109-146">[![Dataverse を介した Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="31109-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="31109-147">参照</span><span class="sxs-lookup"><span data-stu-id="31109-147">See also</span></span>

[<span data-ttu-id="31109-148">日付と時刻データ</span><span class="sxs-lookup"><span data-stu-id="31109-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="31109-149">ユーザーの優先タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="31109-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]