--- 
title: "ウェーブ処理のコンフィギュレーション"
description: "このガイドでは、ウェーブが処理されるときに倉庫に対して生成される作業、およびウェーブが手動または自動で処理されるか判断する基準の設定方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="configure-wave-processing"></a><span data-ttu-id="397c5-103">ウェーブ処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="397c5-103">Configure wave processing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="397c5-104">このガイドでは、ウェーブが処理されるときに倉庫に対して生成される作業、およびウェーブが手動または自動で処理されるか判断する基準の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="397c5-104">This guide describes how to set up the criteria that determine what work is generated for a warehouse when a wave is processed, and whether waves are processed manually or automatically.</span></span> <span data-ttu-id="397c5-105">販売注文、製造オーダー、またはかんばんオーダーのリリース済み明細行のあるウェーブと一致する、ウェーブ テンプレートおよびクエリを設定し、基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-105">You specify the criteria by setting up wave templates and queries that match a wave with released lines in sales orders, production orders, or kanban orders.</span></span> <span data-ttu-id="397c5-106">ウェーブ処理は倉庫管理モジュールで機能を使用する倉庫で使用され、在庫管理モジュールで機能を使用する倉庫では使用されません。</span><span class="sxs-lookup"><span data-stu-id="397c5-106">Wave processing is used in warehouses that use the functionality in the Warehouse management module, and not those that use the functionality in the Inventory management module.</span></span> <span data-ttu-id="397c5-107">デモ データの会社 USMF でこの手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-107">You can run this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="397c5-108">[倉庫管理] > [設定] > [ウェーブ] > [ウェーブ テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="397c5-108">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="397c5-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="397c5-109">Click New.</span></span>
3. <span data-ttu-id="397c5-110">[ウェーブ テンプレート名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="397c5-110">In the Wave template name field, type a value.</span></span>
    * <span data-ttu-id="397c5-111">ウェーブ テンプレートを設定する際は、販売注文、製造オーダー、かんばんのリリース済明細行と照合するテンプレートの順番を指定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-111">When you set up a wave template, you specify the sequence in which the templates will be matched to released lines on sales orders, production orders, or kanbans.</span></span> <span data-ttu-id="397c5-112">明細行が倉庫または製造にリリースされる際、基準に合致する最初のウェーブ テンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="397c5-112">When a line is released to the warehouse or to production, it uses the first wave template that it meets the criteria for.</span></span> <span data-ttu-id="397c5-113">最も限定的な基準のテンプレートをリストの最初に置くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="397c5-113">We recommend that you put templates with the most specific criteria at the top of the list.</span></span> <span data-ttu-id="397c5-114">基準の範囲が広いほど、明細行が基準と合致する確率が高くなり、この結果、間違ったウェーブに明細行が割り当てられることになります。</span><span class="sxs-lookup"><span data-stu-id="397c5-114">The broader the criteria, the more likely it is for a line to meet the criteria, and this could lead to lines being assigned to the wrong wave.</span></span>  
4. <span data-ttu-id="397c5-115">[ウェーブ テンプレートの説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="397c5-115">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="397c5-116">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="397c5-117">USMF を使用している場合はサイト 2 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-117">If you’re using USMF, you can select site 2.</span></span>  
6. <span data-ttu-id="397c5-118">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="397c5-119">USMF を使用している場合は倉庫 24 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-119">If you’re using USMF, you can select warehouse 24.</span></span>  
7. <span data-ttu-id="397c5-120">[ウェーブの作成を自動化] フィールドを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-120">Set the Automate wave creation field to Yes.</span></span>
    * <span data-ttu-id="397c5-121">販売注文、製造オーダー、またはかんばんが倉庫にリリースされるときに、自動的にウェーブを作成するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-121">Select this option to automatically create a wave when a sales order, production order, or kanban is released to the warehouse.</span></span>  
8. <span data-ttu-id="397c5-122">[倉庫へのリリース時にウェーブを処理する] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-122">Set the Process wave at release to warehouse option to Yes.</span></span> 
    * <span data-ttu-id="397c5-123">明細行が倉庫にリリースされる際に自動的にウェーブをプロセス処理し、作業を作成するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-123">Select this option to automatically process the wave and create work when a line is released to the warehouse.</span></span>  
9. <span data-ttu-id="397c5-124">[ウェーブを自動的にリリースする] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-124">Set the Automate wave release option to Yes.</span></span> 
    * <span data-ttu-id="397c5-125">自動的にウェーブをリリースするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-125">Select this option to automatically release the wave.</span></span> <span data-ttu-id="397c5-126">ピッキング作業が作成され、モバイル デバイス上で利用できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-126">The picking work is created and made available on mobile devices.</span></span>  
10. <span data-ttu-id="397c5-127">[未処理のウェーブへの割り当て] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-127">Set the Assign to open waves option to Yes.</span></span> 
    * <span data-ttu-id="397c5-128">明細行はウェーブ テンプレートのクエリ フィルターに基づいてウェーブに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="397c5-128">Lines are assigned to waves based on the query filter for the wave template.</span></span>  
11. <span data-ttu-id="397c5-129">[しきい値に達したときにウェーブを自動処理する] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-129">Set the Process wave automatically at threshold option to Yes.</span></span> 
    * <span data-ttu-id="397c5-130">値が [ウェーブのしきい値] フィールド グループで指定されている重量、出荷、明細行のしきい値に達したときに自動的にウェーブを処理するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-130">Select this option to automatically process the wave when its values reach the thresholds for weight, shipment, and lines specified in the Wave thresholds field group.</span></span> <span data-ttu-id="397c5-131">このオプションは、[ウェーブ テンプレート タイプ] フィールドで [出荷] が選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-131">This option is available only if Shipping is selected in the Wave template type field.</span></span>  
12. <span data-ttu-id="397c5-132">[補充作業のリリースの自動化] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-132">Set the Automate replenishment work release option to Yes.</span></span> 
    * <span data-ttu-id="397c5-133">要求ベースの補充作業を作成して自動的にリリースするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-133">Select this option to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="397c5-134">ウェーブ テンプレートに補充ウェーブ メソッドを追加し、[ウェーブ需要] タイプの補充テンプレートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="397c5-134">You must add the replenishment wave method to the wave template, and create a replenishment template of the type Wave demand.</span></span>  
13. <span data-ttu-id="397c5-135">[メソッド] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="397c5-135">Expand the Methods section.</span></span>
    * <span data-ttu-id="397c5-136">ウェーブ テンプレートのメソッドによって各ウェーブの処理時に行われるアクションの順序を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="397c5-136">Wave template methods allow you to control the sequence of activities that each wave is going through when it’s processed.</span></span> <span data-ttu-id="397c5-137">たとえば、ウェーブの補充のメソッドがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="397c5-137">For example, you might have a method for wave replenishment.</span></span> <span data-ttu-id="397c5-138">メソッドを追加するとき、メソッドは手順の順序の適切な場所に自動的に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="397c5-138">When you add a method, it’s automatically listed in the appropriate location in the sequence of steps.</span></span> <span data-ttu-id="397c5-139">[補充作業のリリースの自動化] オプションを [はい] に設定している場合、ここで補充メソッドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="397c5-139">If you’ve set the Automate replenishment work release option to Yes, you need to add the replenish method here.</span></span>  
    * <span data-ttu-id="397c5-140">ウェーブ属性はフィルターとして機能し、ウェーブを使用できる品目の種類を制限します。</span><span class="sxs-lookup"><span data-stu-id="397c5-140">Wave attributes act as filters, to restrict the kind of items that can use the wave.</span></span> <span data-ttu-id="397c5-141">たとえば、品目グループを指定できます。</span><span class="sxs-lookup"><span data-stu-id="397c5-141">For example, you could specify an item group.</span></span>  
14. <span data-ttu-id="397c5-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="397c5-142">Click Save.</span></span>
15. <span data-ttu-id="397c5-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="397c5-143">Close the page.</span></span>
16. <span data-ttu-id="397c5-144">[倉庫管理] > [設定] > [倉庫管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="397c5-144">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
17. <span data-ttu-id="397c5-145">[ウェーブ処理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="397c5-145">Expand the Wave processing section.</span></span>
18. <span data-ttu-id="397c5-146">[ウェーブを処理するバッチ グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-146">In the Wave processing batch group field, enter or select a value.</span></span>
19. <span data-ttu-id="397c5-147">[ウェーブのバッチ処理] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="397c5-147">Set the Process waves in batch option to Yes.</span></span>
20. <span data-ttu-id="397c5-148">[ロックを待機 (ミリ秒)] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="397c5-148">In the Wait for lock (ms) field, enter a number.</span></span>
    * <span data-ttu-id="397c5-149">配賦ステップが、他の配賦ステップでロックされたシステム リソースを待機する時間を、ミリ秒単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="397c5-149">Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="397c5-150">この時間を超えた場合、ウェーブは処理されず、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="397c5-150">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span>  
21. <span data-ttu-id="397c5-151">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="397c5-151">Click Save.</span></span>
22. <span data-ttu-id="397c5-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="397c5-152">Close the page.</span></span>
23. <span data-ttu-id="397c5-153">[生産管理] > [設定] > [生産管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="397c5-153">Go to Production control > Setup > Production control parameters.</span></span>
24. <span data-ttu-id="397c5-154">[倉庫にリリース] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="397c5-154">In the Release to warehouse field, select an option.</span></span>
    * <span data-ttu-id="397c5-155">販売注文とかんばん注文では、棚卸資産は注文が倉庫にリリースされる前に引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="397c5-155">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="397c5-156">そうしなければ、品門行または配賦行はウェーブで処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="397c5-156">Otherwise, the items or allocation lines cannot be processed in a wave.</span></span> <span data-ttu-id="397c5-157">製造オーダーでは、[部分引当の許可] を選択するというオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="397c5-157">For production orders, you also have the option of choosing Allow partial reservation.</span></span> <span data-ttu-id="397c5-158">たとえば、生産を開始する必要がある材料があり、プロセスを終了するための追加の材料が利用可能になるまで待機できる場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="397c5-158">For example, this is useful if you have the materials that you need to start production, and can then wait until the additional materials become available to finish the process.</span></span> <span data-ttu-id="397c5-159">このオプションを選択する場合、追加の材料が使用可能になるときに、倉庫プロセスに手動でリリースを繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="397c5-159">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span>  
25. <span data-ttu-id="397c5-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="397c5-160">Close the page.</span></span>

