---
title: 品目の補充ルールの定義
description: この手順の作成に使用するデモ データの会社は USMF です。
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 680d7c9339b089a4da82bef18bae3af41e23af30
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845179"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="5bac1-103">品目の補充ルールの定義</span><span class="sxs-lookup"><span data-stu-id="5bac1-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5bac1-104">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5bac1-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5bac1-105">この手順は、補充ルールを作成し特定の品目の補充設定を上書きする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="5bac1-106">また、既定の在庫設定を指定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="5bac1-107">補充グループの作成</span><span class="sxs-lookup"><span data-stu-id="5bac1-107">Create a coverage group</span></span>
1. <span data-ttu-id="5bac1-108">**ナビゲーション ウィンドウ > モジュール > マスター プラン > 設定 > 補充グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="5bac1-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-109">Click **New**.</span></span>
3. <span data-ttu-id="5bac1-110">**補充グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="5bac1-111">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5bac1-112">**カレンダー** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="5bac1-113">このグループの品目の補充提案を作成するためにマスター プランが使用するカレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="5bac1-114">**補充コード** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="5bac1-115">この手順で '要求' を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="5bac1-116">**補充品タイム フェンス (日) フィールド**に '90' と入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="5bac1-117">このグループの品目について、マスター プランにより今後 90 日間までの補充提案を作成します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="5bac1-118">**マイナス在庫日数**フィールドに '1' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="5bac1-119">**プラス在庫日数**フィールドに '1' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="5bac1-120">**その他**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="5bac1-121">**安全マージン日数**セクションの、**要求期日に追加される受領安全日数**フィールドに '1' と入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="5bac1-122">たとえば、受領安全日数が 1 日に設定され、購買注文明細行で 5 月 15 日に入庫がスケジューリングされている場合、マスター プランは調整済の入庫日を 5 月 16 日として計算します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="5bac1-123">**要求期日から差し引かれる払出安全日数**フィールドで '1' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="5bac1-124">たとえば、安全マージンが 1 日に設定され、販売注文明細行で 5 月 15 日に出庫がスケジューリングされている場合、マスター スケジュールは調整済の出荷日を 5 月 14 日として計算します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="5bac1-125">**品目のリード タイムに追加される再発注余裕日数**フィールドで '1' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="5bac1-126">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="5bac1-127">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="5bac1-127">Create a new product</span></span>
1. <span data-ttu-id="5bac1-128">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="5bac1-129">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-129">Click **New**.</span></span>
3. <span data-ttu-id="5bac1-130">**製品番号**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="5bac1-131">**製品名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="5bac1-132">**品目モデル グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5bac1-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="5bac1-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5bac1-135">**品目グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5bac1-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="5bac1-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5bac1-138">**保管分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="5bac1-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="5bac1-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="5bac1-141">**追跡用分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5bac1-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="5bac1-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="5bac1-144">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="5bac1-145">既定の注文設定の設定</span><span class="sxs-lookup"><span data-stu-id="5bac1-145">Setup default order settings</span></span>
1. <span data-ttu-id="5bac1-146">**アクション** ペインで**計画**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="5bac1-147">**注文設定**で、**既定の注文設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="5bac1-148">**購買サイト**の、**既定のサイト** フィールドで、発注書を作成する際に既定として使用するサイトを入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="5bac1-149">**既定の倉庫**フィールドで、品目が格納されているサイトを入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="5bac1-150">**在庫**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="5bac1-151">**複数**フィールドに '10' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="5bac1-152">**最小注文数量**フィールドに '10' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="5bac1-153">**最大注文数量**フィールドに '100' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="5bac1-154">**標準注文数量**フィールドに '10' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="5bac1-155">**購買のリード タイム** フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="5bac1-156">**稼動日**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="5bac1-157">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-157">Click **Save**.</span></span>
13. <span data-ttu-id="5bac1-158">**既定の注文タイプ** フィールドで '発注書' を選択します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="5bac1-159">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-159">Click **Save**.</span></span>
15. <span data-ttu-id="5bac1-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-160">Close the page.</span></span> <span data-ttu-id="5bac1-161">[既定の注文設定] ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="5bac1-162">補充グループへの品目の追加</span><span class="sxs-lookup"><span data-stu-id="5bac1-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="5bac1-163">**計画**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="5bac1-164">**補充グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bac1-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5bac1-165">一覧で、作成した**補充グループ**を検索します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="5bac1-166">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="5bac1-167">品目補充ルールの作成</span><span class="sxs-lookup"><span data-stu-id="5bac1-167">Create item coverage rules</span></span>
1. <span data-ttu-id="5bac1-168">**アクション** ペインで**計画**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="5bac1-169">**補充**で、**品目補充**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="5bac1-170">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-170">Click **New**.</span></span>
4. <span data-ttu-id="5bac1-171">**一般** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="5bac1-172">**補充グループの上書き**設定のヘッダーにあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="5bac1-173">**補充品タイム フェンス (日)** フィールドに '60' と入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="5bac1-174">補充グループ [必要] の品目は90日先まで計画されますが、この品目は 60 日先までの計画となります。</span><span class="sxs-lookup"><span data-stu-id="5bac1-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="5bac1-175">**マイナス在庫日数**フィールドに '2' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="5bac1-176">**プラス在庫日数**フィールドに '2' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="5bac1-177">**リード タイム** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="5bac1-178">**購買**のヘッダーにあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="5bac1-179">**購買時間**フィールドに '5' を入力します。</span><span class="sxs-lookup"><span data-stu-id="5bac1-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="5bac1-180">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bac1-180">Click **Save**.</span></span>

