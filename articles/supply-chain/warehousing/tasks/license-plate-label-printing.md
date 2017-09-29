--- 
title: "ライセンス プレート ラベル印刷の有効化"
description: "この手順は、販売ピッキングの作業プロセスで最後の品目が在庫からピッキングされたあとに、出荷コンテナ シリアル コード (SSCC) ラベルを自動で印刷するようにします。"
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="6b625-103">ライセンス プレート ラベル印刷の有効化</span><span class="sxs-lookup"><span data-stu-id="6b625-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b625-104">この手順は、販売ピッキングの作業プロセスで最後の品目が在庫からピッキングされたあとに、出荷コンテナ シリアル コード (SSCC) ラベルを自動で印刷するようにします。</span><span class="sxs-lookup"><span data-stu-id="6b625-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="6b625-105">デモ データの会社 USMF でこの手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="6b625-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="6b625-106">自分のデータを使用して実行している場合、ライセンス番号に使用する番号順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b625-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="6b625-107">このタスクを開始する前にラベル プリンターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b625-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="6b625-108">[組織管理] > [設定] > [ネットワーク プリンター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="6b625-109">アクション ペインで [オプション] をクリックし、[ドキュメント回覧エージェント インストーラーのダウンロード] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="6b625-110">インストーラを実行し、[有効] に設定された使用可能なネットワーク プリンタがあることを確認してから、手順を進めます。</span><span class="sxs-lookup"><span data-stu-id="6b625-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="6b625-111">GS1 会社の接頭語の設定</span><span class="sxs-lookup"><span data-stu-id="6b625-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="6b625-112">[倉庫管理] > [設定] > [倉庫管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="6b625-113">[GS1 会社の接頭語] フィールドに、GS1 会社の番号 7 つを入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="6b625-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-114">Click Save.</span></span>
4. <span data-ttu-id="6b625-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="6b625-116">SSCC ライセンス プレート番号の番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="6b625-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="6b625-117">[組織管理] > [番号順序] > [番号順序] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="6b625-118">[エリア] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="6b625-119">[参照] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="6b625-120">[会社] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="6b625-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6b625-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6b625-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6b625-123">[区分] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b625-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="6b625-124">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-124">Click Edit.</span></span>
9. <span data-ttu-id="6b625-125">区分テーブルで、先頭行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="6b625-126">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-126">Click Remove.</span></span>
11. <span data-ttu-id="6b625-127">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-127">Click Remove.</span></span>
12. <span data-ttu-id="6b625-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-128">Click Save.</span></span>
13. <span data-ttu-id="6b625-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="6b625-130">ドキュメント回覧レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="6b625-130">Create the document route layout</span></span>
1. <span data-ttu-id="6b625-131">[倉庫管理] > [設定] > [ドキュメント回覧] > [ドキュメント回覧レイアウト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="6b625-132">SSCC レイアウトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6b625-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="6b625-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-133">Click New.</span></span>
3. <span data-ttu-id="6b625-134">[レイアウト ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="6b625-135">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6b625-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="6b625-137">[テキストの末尾に挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="6b625-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-138">Click Save.</span></span>
8. <span data-ttu-id="6b625-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="6b625-140">ドキュメント回覧の設定</span><span class="sxs-lookup"><span data-stu-id="6b625-140">Set up the document routing</span></span>
1. <span data-ttu-id="6b625-141">[倉庫管理] > [設定] > [ドキュメント回覧] > [ドキュメント回覧] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="6b625-142">[ワーク オーダー タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="6b625-143">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-143">Click New.</span></span>
4. <span data-ttu-id="6b625-144">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="6b625-145">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="6b625-146">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-146">Click New.</span></span>
7. <span data-ttu-id="6b625-147">[レイアウト ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="6b625-148">[名前] フィールドで、使用したいプリンター名を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="6b625-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-149">Click Save.</span></span>
10. <span data-ttu-id="6b625-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="6b625-151">モバイル デバイスのメニューの作成</span><span class="sxs-lookup"><span data-stu-id="6b625-151">Create mobile device menu</span></span>
1. <span data-ttu-id="6b625-152">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="6b625-153">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-153">Click New.</span></span>
3. <span data-ttu-id="6b625-154">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="6b625-155">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="6b625-156">[モード] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="6b625-157">[既存の作業を使用] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="6b625-158">[ライセンス プレートの生成] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="6b625-159">作業クラスのセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b625-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="6b625-160">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-160">Click New.</span></span>
10. <span data-ttu-id="6b625-161">[作業クラス ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b625-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="6b625-162">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-162">Click Save.</span></span>
12. <span data-ttu-id="6b625-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-163">Close the page.</span></span>
13. <span data-ttu-id="6b625-164">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="6b625-165">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6b625-166">ツリーで、[ツリーで、以前に作成したメニュー項目を選択する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="6b625-167">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-167">Click Edit.</span></span>
17. <span data-ttu-id="6b625-168">矢印をクリックしてメニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="6b625-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="6b625-169">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-169">Click Save.</span></span>
19. <span data-ttu-id="6b625-170">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="6b625-171">作業テンプレートの更新</span><span class="sxs-lookup"><span data-stu-id="6b625-171">Update a work template</span></span>
1. <span data-ttu-id="6b625-172">[倉庫管理] > [設定] > [作業] > [作業テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b625-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="6b625-173">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6b625-174">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-174">Click Edit.</span></span>
4. <span data-ttu-id="6b625-175">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-175">Click New.</span></span>
5. <span data-ttu-id="6b625-176">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6b625-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6b625-177">[作業タイプ] フィールドで [印刷] を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="6b625-178">[作業クラス ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b625-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="6b625-179">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6b625-180">[上へ移動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-180">Click Move up.</span></span>
10. <span data-ttu-id="6b625-181">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b625-181">Click Save.</span></span>
11. <span data-ttu-id="6b625-182">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b625-182">Close the page.</span></span>


