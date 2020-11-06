---
title: ライセンス プレート ラベル印刷の有効化
description: このトピックでは、販売ピッキングの作業プロセスで最後の品目が在庫からピッキングされたあとに、出荷コンテナ シリアル コード (SSCC) ラベルを自動で印刷する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016105"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="077c1-103">ライセンス プレート ラベル印刷の有効化</span><span class="sxs-lookup"><span data-stu-id="077c1-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="077c1-104">このトピックでは、販売ピッキングの作業プロセスで最後の品目が在庫からピッキングされたあとに、出荷コンテナ シリアル コード (SSCC) ラベルを自動で印刷する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="077c1-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="077c1-105">デモ データの会社 USMF でこの手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="077c1-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="077c1-106">自分のデータを使用して実行している場合、ライセンス プレートに番号シーケンスが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="077c1-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="077c1-107">このタスクを開始する前にラベル プリンターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="077c1-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="077c1-108">[組織管理] > [設定] > [ネットワーク プリンター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="077c1-109">アクション ウィンドウで [オプション] をクリックし、[ドキュメント回覧エージェント インストーラーのダウンロード] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="077c1-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="077c1-110">インストーラを実行し、[有効] に設定された使用可能なネットワーク プリンタがあることを確認してから、手順を進めます。</span><span class="sxs-lookup"><span data-stu-id="077c1-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="077c1-111">GS1 会社の接頭語の設定</span><span class="sxs-lookup"><span data-stu-id="077c1-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="077c1-112">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="077c1-113">**GS1 会社の接頭語** フィールドに、GS1 会社の番号 7 つを入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="077c1-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-114">Select **Save**.</span></span>
4. <span data-ttu-id="077c1-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="077c1-116">SSCC ライセンス プレート番号の番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="077c1-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="077c1-117">**ナビゲーション ウィンドウ > モジュール > 組織管理 > 番号順序 > 番号順序** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="077c1-118">**エリア** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="077c1-119">**参照** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="077c1-120">**会社** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="077c1-121">**区分** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="077c1-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="077c1-122">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-122">Select **Edit**.</span></span>
7. <span data-ttu-id="077c1-123">**区分** テーブルで、先頭行を選択する</span><span class="sxs-lookup"><span data-stu-id="077c1-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="077c1-124">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-124">Select **Remove**.</span></span>
9. <span data-ttu-id="077c1-125">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-125">Select **Remove**.</span></span>
10. <span data-ttu-id="077c1-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-126">Select **Save**.</span></span>
11. <span data-ttu-id="077c1-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="077c1-128">ドキュメント回覧レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="077c1-128">Create the document route layout</span></span>
1. <span data-ttu-id="077c1-129">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > ドキュメント回覧 > ドキュメント回覧レイアウト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="077c1-130">SSCC レイアウトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="077c1-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="077c1-131">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-131">Select **New**.</span></span>
3. <span data-ttu-id="077c1-132">**レイアウト ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="077c1-133">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="077c1-134">**テキストの末尾に挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="077c1-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-135">Select **Save**.</span></span>
7. <span data-ttu-id="077c1-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="077c1-137">ドキュメント回覧の設定</span><span class="sxs-lookup"><span data-stu-id="077c1-137">Set up the document routing</span></span>
1. <span data-ttu-id="077c1-138">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > ドキュメント回覧 > ドキュメント回覧** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="077c1-139">**作業指示書タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="077c1-140">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-140">Select **New**.</span></span>
4. <span data-ttu-id="077c1-141">**倉庫** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="077c1-142">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="077c1-143">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-143">Select **New**.</span></span>
7. <span data-ttu-id="077c1-144">**レイアウト ID** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="077c1-145">**名前** フィールドで、使用するプリンター名を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="077c1-146">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-146">Select **Save**.</span></span>
10. <span data-ttu-id="077c1-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="077c1-148">モバイル デバイスのメニューの作成</span><span class="sxs-lookup"><span data-stu-id="077c1-148">Create mobile device menu</span></span>
1. <span data-ttu-id="077c1-149">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー項目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="077c1-150">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-150">Select **New**.</span></span>
3. <span data-ttu-id="077c1-151">**メニュー項目名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="077c1-152">**タイトル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="077c1-153">**モード** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="077c1-154">**既存の作業を使用** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="077c1-155">**ライセンス プレートの生成** フィールドで、 **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="077c1-156">**作業クラス** のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="077c1-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="077c1-157">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-157">Select **New**.</span></span>
10. <span data-ttu-id="077c1-158">**作業クラス ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="077c1-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="077c1-159">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-159">Select **Save**.</span></span>
12. <span data-ttu-id="077c1-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-160">Close the page.</span></span>
13. <span data-ttu-id="077c1-161">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="077c1-162">ツリーで、以前に作成したメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="077c1-163">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-163">Select **Edit**.</span></span>
16. <span data-ttu-id="077c1-164">矢印を選択してメニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="077c1-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="077c1-165">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-165">Select **Save**.</span></span>
18. <span data-ttu-id="077c1-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="077c1-167">作業テンプレートの更新</span><span class="sxs-lookup"><span data-stu-id="077c1-167">Update a work template</span></span>
1. <span data-ttu-id="077c1-168">**ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 作業 > 作業テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="077c1-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="077c1-169">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-169">Select **Edit**.</span></span>
3. <span data-ttu-id="077c1-170">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-170">Select **New**.</span></span>
4. <span data-ttu-id="077c1-171">**作業タイプ** フィールドで **印刷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="077c1-172">**作業クラス ID** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="077c1-173">**上へ移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-173">Select **Move up**.</span></span>
7. <span data-ttu-id="077c1-174">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="077c1-174">Select **Save**.</span></span>
8. <span data-ttu-id="077c1-175">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="077c1-175">Close the page.</span></span>

