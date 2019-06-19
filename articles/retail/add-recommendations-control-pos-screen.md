---
title: POS デバイスのトランザクション画面への推奨事項コントロールの追加
description: このトピックでは、Microsoft Dynamics 365 for Retail の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606852"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="e6eb8-103">POS デバイスのトランザクション画面への推奨事項コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="e6eb8-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="e6eb8-104">より良いアルゴリズムとより新しい小売指向の機能を加えたこの機能をデザインするため、製品レコメンデーション サービスの現在のバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="e6eb8-105">詳細については、[削除済みまたは推奨されない機能](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="e6eb8-106">このトピックでは、Microsoft Dynamics 365 for Retail の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="e6eb8-107">Microsoft Dynamics 365 for Retail を使用するときに、POS デバイスに製品レコメンデーションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="e6eb8-108">*レコメンデーション* は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目です。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="e6eb8-109">製品レコメンデーションを表示するには、画面レイアウト デザイナーを使用してトランザクション画面にコントロールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="e6eb8-110">レイアウト デザイナーを開く</span><span class="sxs-lookup"><span data-stu-id="e6eb8-110">Open Layout designer</span></span>

1. <span data-ttu-id="e6eb8-111">**小売り** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **POS** &gt; **画面レイアウト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e6eb8-112">クイック フィルターを使用して、コントロールを追加する画面を検索します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e6eb8-113">たとえば、**F2CP16:9M** の値を使用して**画面レイアウト ID** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e6eb8-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="e6eb8-115">たとえば、**名前: F2CP16:9M 画面レイアウト ID: F2CP16:9M** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e6eb8-116">**レイアウト デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e6eb8-117">プロンプトに従ってレイアウト デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e6eb8-118">資格情報を求められたら、レイアウト デザイナーを**画面レイアウト**ページから起動した際に使用していたものと同じ資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e6eb8-119">ログインすると、以下のものに類似したページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e6eb8-120">レイアウトは、店舗に対して行われたカスタマイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="e6eb8-121">[![レイアウト デザイナー](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e6eb8-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e6eb8-122">表示オプションを選択</span><span class="sxs-lookup"><span data-stu-id="e6eb8-122">Choose a display option</span></span>

<span data-ttu-id="e6eb8-123">使用できる 2 つのコンフィギュレーション オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-123">There are two configurations options available.</span></span> <span data-ttu-id="e6eb8-124">店舗に最も合っているオプションを選択し、残りの手順にに従ってコントロールのセットアップを完了します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e6eb8-125">2 つのオプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-125">The two options are:</span></span>

- <span data-ttu-id="e6eb8-126">レコメンデーションは常に表示できます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="e6eb8-127">**レコメンデーション**タブが画面の右側のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e6eb8-128">レコメンデーションを常に表示する</span><span class="sxs-lookup"><span data-stu-id="e6eb8-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="e6eb8-129">左側が顧客パネルと同じ高さになるように、トランザクション明細行の詳細領域の高さを下げます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="e6eb8-130">[![トランザクション明細行の詳細領域の高さを減少](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e6eb8-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e6eb8-131">左側のメニューから、トランザクション明細行の詳細領域とトランザクション画面の中央下にあるボタン グリッドの間にレコメンデーション コントロールをドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e6eb8-132">そのスペースに合うようにコントロールのサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e6eb8-133">[![レイアウトに追加されたレコメンデーション コントロール](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e6eb8-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="e6eb8-134">**X** をクリックして、レイアウト デザイナーを保存して終了します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e6eb8-135">Dynamics 365 for Retail で、**小売り** &gt; **小売 IT** &gt; **配送スケジュール**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e6eb8-136">ボックスの一覧で、 **1090 レジスター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e6eb8-137">**今すぐ実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e6eb8-138">画面の右側のボタン グリッドにレコメンデーション タブを追加する</span><span class="sxs-lookup"><span data-stu-id="e6eb8-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e6eb8-139">ページの右側にあるボタン グリッドで最後のタブの下にある空いている場所を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="e6eb8-140"> **カスタマイズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-140">Click **Customize**.</span></span>

    <span data-ttu-id="e6eb8-141">[![カスタマイズ - タブコントロール ダイアログ ボックス](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e6eb8-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e6eb8-142">**新しいタブ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-142">Click **New tab**.</span></span>
4. <span data-ttu-id="e6eb8-143">さっき追加した新しいタブを探します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-143">Find the new tab that you just added.</span></span> <span data-ttu-id="e6eb8-144">スクロール ダウンしなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="e6eb8-145">**コンテンツ**のドロップダウンで、**お勧めの製品**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e6eb8-146">[![コンテンツ フィールドのお勧め製品を選択](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e6eb8-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e6eb8-147">**ラベル**フィールドに、このレコメンデーション タブの名前を入力します。たとえば、「お勧めの製品」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e6eb8-148">**画像**フィールドで、タブで表示する画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e6eb8-149"> **OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-149">Click **OK**.</span></span> <span data-ttu-id="e6eb8-150">新しいタブがボタン グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e6eb8-151">**X** をクリックして、レイアウト デザイナーを保存して終了します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e6eb8-152">Dynamics 365 for Retail で、**小売り** &gt; **小売 IT** &gt; **配送スケジュール**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e6eb8-153">一覧で、 **1090 レジスター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e6eb8-154">**今すぐ実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6eb8-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6eb8-155">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="e6eb8-155">Additional resources</span></span>

[<span data-ttu-id="e6eb8-156">カスタマイズされた製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="e6eb8-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
