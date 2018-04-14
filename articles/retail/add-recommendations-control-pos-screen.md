---
title: "POS デバイスのトランザクション ページへのレコメンデーション コントロールの追加"
description: "このトピックでは、Microsoft Dynamics 365 for Retail の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7d1e5392e4d3fa86bf62943cb4f5b5f4c7b383
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="96dd4-103">POS デバイスのトランザクション ページへのレコメンデーション コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="96dd4-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="96dd4-104">より良いアルゴリズムとより新しい小売指向の機能を加えたこの機能をデザインするため、製品レコメンデーション サービスの現在のバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="96dd4-105">詳細については、[削除済みまたは推奨されない機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96dd4-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="96dd4-106">このトピックでは、Microsoft Dynamics 365 for Retail の画面レイアウト デザイナーを使用して販売時点管理 (POS) デバイスのトランザクション画面にレコメンデーション コントロールを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="96dd4-107">Microsoft Dynamics 365 for Retail を使用するときに、POS デバイスに製品レコメンデーションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="96dd4-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="96dd4-108">[*レコメンデーション*] は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目です。</span><span class="sxs-lookup"><span data-stu-id="96dd4-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="96dd4-109">製品レコメンデーションを表示するには、画面レイアウト デザイナーを使用してトランザクション画面にコントロールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96dd4-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="96dd4-110">レイアウト デザイナーを開く</span><span class="sxs-lookup"><span data-stu-id="96dd4-110">Open Layout designer</span></span>
1.  <span data-ttu-id="96dd4-111">[小売り] &gt; [チャンネル設定] &gt; [POS 設定] &gt; [POS] &gt; [画面レイアウト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="96dd4-112">クイック フィルターを使用して、コントロールを追加する画面を検索します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="96dd4-113">たとえば、「F2CP16:9M」の値を使用して [画面レイアウト ID] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="96dd4-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="96dd4-115">たとえば、「名前: F2CP16:9M 画面レイアウト ID: F2CP16:9M」を選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="96dd4-116">[レイアウト デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="96dd4-117">プロンプトに従ってレイアウト デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="96dd4-118">資格情報を求められたら、レイアウト デザイナーを [画面レイアウト] ページから起動した際に使用していたものと同じ資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="96dd4-119">ログインすると、以下のものに類似したページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="96dd4-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="96dd4-120">レイアウトは、店舗に対して行われたカスタマイズによって異なります。</span><span class="sxs-lookup"><span data-stu-id="96dd4-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="96dd4-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) 表示オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="96dd4-122">使用できる 2 つのコンフィギュレーション オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="96dd4-122">There are two configurations options available.</span></span> <span data-ttu-id="96dd4-123">店舗に最も合っているオプションを選択し、残りの手順にに従ってコントロールのセットアップを完了します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="96dd4-124">2 つのオプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="96dd4-124">The two options are:</span></span>
-   <span data-ttu-id="96dd4-125">レコメンデーションは常に表示できます。</span><span class="sxs-lookup"><span data-stu-id="96dd4-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="96dd4-126">[レコメンデーション] タブが画面の右側のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="96dd4-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="96dd4-127">レコメンデーションを常に表示する方法</span><span class="sxs-lookup"><span data-stu-id="96dd4-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="96dd4-128">左側が顧客パネルと同じ高さになるように、トランザクション明細行の詳細領域の高さを下げます。[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="96dd4-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="96dd4-129">左側のメニューから、トランザクション明細行の詳細領域とトランザクション画面の中央下にあるボタン グリッドの間にレコメンデーション コントロールをドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="96dd4-130">そのスペースに合うようにコントロールのサイズを変更します。[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="96dd4-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="96dd4-131">[X] をクリックして、レイアウト デザイナーを保存して終了します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="96dd4-132">Dynamics 365 for Retail で、[小売り] &gt; [小売 IT] &gt; [配送スケジュール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="96dd4-133">ボックスの一覧で、[1090 レジスター] を選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="96dd4-134">[今すぐ実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="96dd4-135">画面の右側のボタン グリッドに [レコメンデーション] タブを追加する方法</span><span class="sxs-lookup"><span data-stu-id="96dd4-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="96dd4-136">ページの右側にあるボタン グリッドで最後のタブの下にある空いている場所を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="96dd4-137">[カスタマイズ] をクリックします。[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="96dd4-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="96dd4-138">[新しいタブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="96dd4-139">さっき追加した新しいタブを探します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-139">Find the new tab that you just added.</span></span> <span data-ttu-id="96dd4-140">スクロール ダウンしなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="96dd4-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="96dd4-141">[コンテンツ] のドロップダウンで、[お勧めの製品] を選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="96dd4-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="96dd4-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="96dd4-143">[ラベル] フィールドに、このレコメンデーション タブの名前を入力します。たとえば、「お勧めの製品」と入力します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="96dd4-144">[画像] フィールドで、タブで表示する画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="96dd4-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-145">Click **OK**.</span></span> <span data-ttu-id="96dd4-146">新しいタブがボタン グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="96dd4-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="96dd4-147">[X] をクリックして、レイアウト デザイナーを保存して終了します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="96dd4-148">Dynamics 365 for Retail で、[小売り] &gt; [小売 IT] &gt; [配送スケジュール] に移動します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="96dd4-149">ボックスの一覧で、[1090 レジスター] を選択します。</span><span class="sxs-lookup"><span data-stu-id="96dd4-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="96dd4-150">[今すぐ実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="96dd4-150">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="96dd4-151">参照</span><span class="sxs-lookup"><span data-stu-id="96dd4-151">See also</span></span>
--------

[<span data-ttu-id="96dd4-152">パーソナライズされた製品の推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="96dd4-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




