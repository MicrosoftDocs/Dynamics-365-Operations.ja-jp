---
title: 基準価格と売買契約
description: この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413813"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="4f320-103">基準価格と売買契約</span><span class="sxs-lookup"><span data-stu-id="4f320-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f320-104">この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="4f320-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="4f320-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f320-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="4f320-106">**ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > 価格と割引の管理 > 価格グループ > すべての価格グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f320-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="4f320-107">価格グループは、売買契約を特定のチャネルに割り当てる方法です。</span><span class="sxs-lookup"><span data-stu-id="4f320-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="4f320-108">価格グループを使用して、チャンネル固有の価格設定が可能なチャンネルに売買契約を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4f320-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="4f320-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-109">Click **New**.</span></span>
3. <span data-ttu-id="4f320-110">**価格グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f320-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="4f320-111">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f320-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="4f320-112">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-112">Click **Save**.</span></span>
6. <span data-ttu-id="4f320-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f320-113">Close the page.</span></span>
7. <span data-ttu-id="4f320-114">**ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > チャネル > 店舗 > すべての店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f320-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="4f320-115">一覧で「ニューヨーク」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f320-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="4f320-116">アクション ウィンドウで、**店舗** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="4f320-117">**価格グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="4f320-118">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-118">Click **New**.</span></span>
12. <span data-ttu-id="4f320-119">**価格グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f320-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="4f320-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4f320-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="4f320-121">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-121">Click **Save**.</span></span>
15. <span data-ttu-id="4f320-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f320-122">Close the page.</span></span>
16. <span data-ttu-id="4f320-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f320-123">Close the page.</span></span>
17. <span data-ttu-id="4f320-124">**ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > 製品とカテゴリ > カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f320-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="4f320-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="4f320-126">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-126">Click **Edit**.</span></span>
20. <span data-ttu-id="4f320-127">**販売** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="4f320-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="4f320-128">**価格** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f320-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="4f320-129">この価格は、適用できる売買契約がない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f320-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="4f320-130">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-130">Click **Save**.</span></span>
23. <span data-ttu-id="4f320-131">**アクション ウィンドウ** で、**販売** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="4f320-132">**売買契約** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="4f320-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-133">Click **New**.</span></span>
26. <span data-ttu-id="4f320-134">**名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f320-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="4f320-135">一覧で、**Commerce** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f320-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="4f320-136">デモ データで、**Commerce** 仕訳帳名の既定のリレーションは **価格 (販売)** です。</span><span class="sxs-lookup"><span data-stu-id="4f320-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="4f320-137">これは、作成されたすべての新しい明細行が、販売価格の売買契約の既定値であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4f320-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="4f320-138">**アクション ウィンドウ** で、**明細行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="4f320-139">**関係者コード タイプ** フィールドで、'グループ' を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f320-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="4f320-140">**勘定の選択** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4f320-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="4f320-141">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4f320-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="4f320-142">これによって、チャンネルから価格グループ、売買契約へのリンクが完了します。</span><span class="sxs-lookup"><span data-stu-id="4f320-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="4f320-143">**商品関係** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f320-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="4f320-144">**通貨金額** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f320-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="4f320-145">**詳細** クイック タブで、**次を検索** チェックボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="4f320-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="4f320-146">**次を検索** が 'はい' に設定されている場合、価格決定エンジンは販売価格の低い適用できる売買契約を検索し続けます。</span><span class="sxs-lookup"><span data-stu-id="4f320-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="4f320-147">**次を検索** が 'いいえ' に設定されている場合、価格エンジンは検索を中止し、その売買契約を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f320-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="4f320-148">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-148">Click **Post**.</span></span>
36. <span data-ttu-id="4f320-149">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-149">Click **OK**.</span></span>
37. <span data-ttu-id="4f320-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f320-150">Close the page.</span></span>
38. <span data-ttu-id="4f320-151">**アクション ウィンドウ** で販売をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="4f320-152">**販売価格** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f320-152">Click **Sales price**.</span></span>

