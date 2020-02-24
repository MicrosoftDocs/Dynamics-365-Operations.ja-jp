---
title: 従業員のけが/病気の情報の管理
description: 設定情報の一部をここで使用するため、「けがおよび病気の設定」タスク ガイドを最初に完了することをお勧めします。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786461338d994ab04dfa57428e7720162ab16f86
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009706"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="5fd32-103">従業員のけが/病気の情報の管理</span><span class="sxs-lookup"><span data-stu-id="5fd32-103">Maintain employee injury and illness information</span></span>



<span data-ttu-id="5fd32-104">設定情報の一部をここで使用するため、「けがおよび病気の設定」タスク ガイドを最初に完了することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="5fd32-105">このタスク記録では、傷害または疾病ケースを作成する基本的な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="5fd32-106">傷害または疾病の詳細の追跡に加え、ケース ステータスも同様に追跡されます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="5fd32-107">ケースは「未処理」ステータスを規定値に設定しています。</span><span class="sxs-lookup"><span data-stu-id="5fd32-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="5fd32-108">ステータスは、ページ上部の「ケース ステータス」メニュー項目から管理できます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-108">The statuses can be managed from the 'Case status' menu item at the top of the page.</span></span>

1. <span data-ttu-id="5fd32-109">[人事管理] > [作業者] > [けが / 病気] > [けがまたは病気のインシデント] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="5fd32-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-110">Click New.</span></span>
3. <span data-ttu-id="5fd32-111">[ケースの説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="5fd32-112">例 : 手首のけが</span><span class="sxs-lookup"><span data-stu-id="5fd32-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="5fd32-113">[作業者] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-114">例 : アーメド バーネット</span><span class="sxs-lookup"><span data-stu-id="5fd32-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="5fd32-115">[インシデントの日時] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="5fd32-116">例 : 1/20/2016 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="5fd32-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="5fd32-117">[けが / 病気のタイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-118">例: 挫傷</span><span class="sxs-lookup"><span data-stu-id="5fd32-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="5fd32-119">[身体部位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-120">例: 手首</span><span class="sxs-lookup"><span data-stu-id="5fd32-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="5fd32-121">[結果タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-122">例: 療法</span><span class="sxs-lookup"><span data-stu-id="5fd32-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="5fd32-123">[報告された日時] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="5fd32-124">報告された日時はインシデントの日時よりも後にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fd32-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="5fd32-125">[ケースの報告者] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-126">これは従業員またはインシデントの別の証人である場合があります。</span><span class="sxs-lookup"><span data-stu-id="5fd32-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="5fd32-127">例 : アーメド バーネット</span><span class="sxs-lookup"><span data-stu-id="5fd32-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="5fd32-128">[インシデント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="5fd32-129">[インシデントが発生した場所] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="5fd32-130">例 : 倉庫</span><span class="sxs-lookup"><span data-stu-id="5fd32-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="5fd32-131">[作業敷地内] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="5fd32-132">作業構内でインシデントが発生した場合、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="5fd32-133">[作業開始日時] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="5fd32-134">インシデントの発生する前に、対象の個人が作業を開始した日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="5fd32-135">[従業員のジョブまたはタスク] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="5fd32-136">インシデント発生時に作業者が実行していたジョブまたはタスクを入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="5fd32-137">例: 箱の荷積</span><span class="sxs-lookup"><span data-stu-id="5fd32-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="5fd32-138">[インシデントの原因] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="5fd32-139">インシデントの原因を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="5fd32-140">例: ぬれたフロアで滑った</span><span class="sxs-lookup"><span data-stu-id="5fd32-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="5fd32-141">[重大度] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="5fd32-142">[実行されるアクション] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="5fd32-143">例 : こぼれをすみやかに掃除</span><span class="sxs-lookup"><span data-stu-id="5fd32-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="5fd32-144">[仕事を休む予測日数] に、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="5fd32-145">個人が仕事を休む予測日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="5fd32-146">個人が作業に戻ったら、「離職日数」フィールドで、実際に休んだ日数を更新します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="5fd32-147">[けが / 病気のコスト] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="5fd32-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-148">Click Add.</span></span>
22. <span data-ttu-id="5fd32-149">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="5fd32-150">[コスト タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-151">例: [治療] 金額を入力し、請求書または医者の注記などのサポート ドキュメントを費用に添付できます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="5fd32-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-152">Click Add.</span></span>
25. <span data-ttu-id="5fd32-153">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="5fd32-154">[コスト タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-155">例 : [医師]</span><span class="sxs-lookup"><span data-stu-id="5fd32-155">Example: Doctor</span></span>  
27. <span data-ttu-id="5fd32-156">[けが / 病気の処置] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="5fd32-157">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-157">Click Add.</span></span>
29. <span data-ttu-id="5fd32-158">[処置の日付] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="5fd32-159">[処置のタイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd32-160">例 : [そえ木]</span><span class="sxs-lookup"><span data-stu-id="5fd32-160">Example:  Splint</span></span>  
31. <span data-ttu-id="5fd32-161">必要に応じて、救急病院の利用セクションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="5fd32-162">[処置に関するコメント] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="5fd32-163">例 : そえ木を2週間</span><span class="sxs-lookup"><span data-stu-id="5fd32-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="5fd32-164">[医師名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="5fd32-165">例 : 先生 アンダーソン</span><span class="sxs-lookup"><span data-stu-id="5fd32-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="5fd32-166">[処置施設および場所] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="5fd32-167">例 : エルム ストリート 緊急事態</span><span class="sxs-lookup"><span data-stu-id="5fd32-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="5fd32-168">[処置の詳細] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="5fd32-169">例 : x 線で骨折を確認、そえ木を装着</span><span class="sxs-lookup"><span data-stu-id="5fd32-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="5fd32-170">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd32-170">Click Save.</span></span>
    * <span data-ttu-id="5fd32-171">ケース ステータスはいつでも更新できます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="5fd32-172">傷害または疾病が処理中の場合、ケースを処理中に設定します。</span><span class="sxs-lookup"><span data-stu-id="5fd32-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="5fd32-173">インシデントを閉じた後は、コスト、治療、インシデント関連のファイリングのみ追加や削除ができます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="5fd32-174">他の情報を変更するには、ケースを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="5fd32-174">To modify other information, reopen the case.</span></span>  

