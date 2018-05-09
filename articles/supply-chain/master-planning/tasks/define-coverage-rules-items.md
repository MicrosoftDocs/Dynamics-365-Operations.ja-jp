--- 
title: "品目の補充ルールの定義"
description: "この手順の作成に使用するデモ データの会社は USMF です。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3205fe6a10ce714073334c7ccd25acb755e0aebf
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="7c5f7-103">品目の補充ルールの定義</span><span class="sxs-lookup"><span data-stu-id="7c5f7-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c5f7-104">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7c5f7-105">この手順は、補充ルールを作成し特定の品目の補充設定を上書きする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="7c5f7-106">また、既定の在庫設定を指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="7c5f7-107">補充グループの作成</span><span class="sxs-lookup"><span data-stu-id="7c5f7-107">Create a coverage group</span></span>
1. <span data-ttu-id="7c5f7-108">[補充グループ] に進みます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="7c5f7-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-109">Click New.</span></span>
3. <span data-ttu-id="7c5f7-110">[補充グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="7c5f7-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7c5f7-112">[カレンダー] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="7c5f7-113">このグループの品目の補充提案を作成するためにマスター プランが使用するカレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="7c5f7-114">[補充コード] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="7c5f7-115">この手順で [要求] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="7c5f7-116">[補充品タイム フェンス (日)] フィールドに「90」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="7c5f7-117">このグループの品目について、マスター プランにより今後 90 日間までの補充提案を作成します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="7c5f7-118">[マイナス在庫日数] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="7c5f7-119">[プラス在庫日数] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="7c5f7-120">[その他] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="7c5f7-121">[要求期日に追加される受領安全日数] フィールドで「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="7c5f7-122">たとえば、受領安全日数が 1 日に設定され、購買注文明細行で 5 月 15 日に入庫がスケジューリングされている場合、マスター プランは調整済の入庫日を 5 月 16 日として計算します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="7c5f7-123">[要求期日から差し引かれる払出安全日数] フィールドで「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="7c5f7-124">たとえば、安全マージンが 1 日に設定され、販売注文明細行で 5 月 15 日に出庫がスケジューリングされている場合、マスター スケジュールは調整済の出荷日を 5 月 14 日として計算します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="7c5f7-125">[品目のリード タイムに追加される再発注余裕日数] フィールドで「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="7c5f7-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="7c5f7-127">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="7c5f7-127">Create a new product</span></span>
1. <span data-ttu-id="7c5f7-128">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-128">Go to Released products.</span></span>
2. <span data-ttu-id="7c5f7-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-129">Click New.</span></span>
3. <span data-ttu-id="7c5f7-130">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="7c5f7-131">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="7c5f7-132">[品目モデル グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7c5f7-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7c5f7-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="7c5f7-135">[品目グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="7c5f7-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7c5f7-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="7c5f7-138">[保管分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="7c5f7-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="7c5f7-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7c5f7-141">[追跡用分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="7c5f7-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="7c5f7-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="7c5f7-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="7c5f7-145">既定の注文設定の設定</span><span class="sxs-lookup"><span data-stu-id="7c5f7-145">Setup default order settings</span></span>
1. <span data-ttu-id="7c5f7-146">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="7c5f7-147">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-147">Click Default order settings.</span></span>
3. <span data-ttu-id="7c5f7-148">[購買サイト] フィールドで、発注書を作成する際に既定として使用するサイトを入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="7c5f7-149">[在庫サイト] フィールドで、品目を保管するサイトを入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="7c5f7-150">[在庫] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="7c5f7-151">[複数] を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="7c5f7-152">[Min] を設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-152">Set Min.</span></span> <span data-ttu-id="7c5f7-153">注文数量を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="7c5f7-154">最大を設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-154">Set Max.</span></span> <span data-ttu-id="7c5f7-155">注文数量を「100」に設定します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="7c5f7-156">[標準注文数量] を「10」にします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="7c5f7-157">[購買のリード タイム] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="7c5f7-158">[稼動日] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="7c5f7-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-159">Click Save.</span></span>
13. <span data-ttu-id="7c5f7-160">[既定の注文タイプ] フィールドで「発注書」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="7c5f7-161">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-161">Click Save.</span></span>
15. <span data-ttu-id="7c5f7-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-162">Close the page.</span></span>
    * <span data-ttu-id="7c5f7-163">[既定の注文設定] ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="7c5f7-164">補充グループへの品目の追加</span><span class="sxs-lookup"><span data-stu-id="7c5f7-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="7c5f7-165">[計画] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="7c5f7-166">[補充グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7c5f7-167">一覧で、作成した補充グループを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="7c5f7-168">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="7c5f7-169">品目補充ルールの作成</span><span class="sxs-lookup"><span data-stu-id="7c5f7-169">Create item coverage rules</span></span>
1. <span data-ttu-id="7c5f7-170">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="7c5f7-171">[品目補充] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-171">Click Item coverage.</span></span>
3. <span data-ttu-id="7c5f7-172">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-172">Click New.</span></span>
4. <span data-ttu-id="7c5f7-173">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-173">Click the General tab.</span></span>
5. <span data-ttu-id="7c5f7-174">[補充グループ設定の上書き] のヘッダーのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="7c5f7-175">[補充タイム フェンス (日)] フィールドに「60」と入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="7c5f7-176">補充グループ [必要] の品目は 90 日先まで計画されますが、この品目は 60 日先までの計画となります。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-176">Although items in coverage group Requirement are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="7c5f7-177">[マイナス在庫日数] フィールドに「2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="7c5f7-178">[プラス在庫日数] フィールドに「2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="7c5f7-179">[リード タイム] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="7c5f7-180">[購買] のヘッダーのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="7c5f7-181">[購買時間] フィールドに「5」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="7c5f7-182">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7c5f7-182">Click Save.</span></span>


