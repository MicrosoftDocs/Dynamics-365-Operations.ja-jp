--- 
title: "チャンネル固有の売買契約の作成"
description: "この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4cc797d2e23f0c7b14564415de6153ac0894c727
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-channel-specific-trade-agreements"></a><span data-ttu-id="9ddd6-103">チャンネル固有の売買契約の作成</span><span class="sxs-lookup"><span data-stu-id="9ddd6-103">Create channel-specific trade agreements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9ddd6-104">この手順では、チャンネル固有の販売価格の売買契約の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="9ddd6-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9ddd6-106">[小売りとコマース] > [価格決定と割引] > [価格グループ] > [すべての価格グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="9ddd6-107">価格グループは、売買契約を特定のチャネルに割り当てる方法です。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="9ddd6-108">価格グループを使用して、チャンネル固有の価格設定が可能なチャンネルに売買契約を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="9ddd6-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-109">Click New.</span></span>
3. <span data-ttu-id="9ddd6-110">[価格グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="9ddd6-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9ddd6-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-112">Click Save.</span></span>
6. <span data-ttu-id="9ddd6-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-113">Close the page.</span></span>
7. <span data-ttu-id="9ddd6-114">[小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="9ddd6-115">一覧で「ニューヨーク」を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="9ddd6-116">アクション ウィンドウで、[店舗] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="9ddd6-117">[価格グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-117">Click Price groups.</span></span>
11. <span data-ttu-id="9ddd6-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-118">Click New.</span></span>
12. <span data-ttu-id="9ddd6-119">[価格グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9ddd6-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9ddd6-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-121">Click Save.</span></span>
15. <span data-ttu-id="9ddd6-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-122">Close the page.</span></span>
16. <span data-ttu-id="9ddd6-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-123">Close the page.</span></span>
17. <span data-ttu-id="9ddd6-124">[小売りとコマース] > [製品とカテゴリ] > [カテゴリ別リリース済製品] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="9ddd6-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9ddd6-126">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-126">Click Edit.</span></span>
20. <span data-ttu-id="9ddd6-127">[販売] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="9ddd6-128">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="9ddd6-129">この価格は、適用できる売買契約がない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="9ddd6-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-130">Click Save.</span></span>
23. <span data-ttu-id="9ddd6-131">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="9ddd6-132">売買契約をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="9ddd6-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-133">Click New.</span></span>
26. <span data-ttu-id="9ddd6-134">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="9ddd6-135">一覧で、[小売] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="9ddd6-136">デモ データで、「小売」仕訳帳名の既定のリレーションは「価格 (販売) 」です。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="9ddd6-137">これは、作成されたすべての新しい明細行が、販売価格の売買契約の既定値であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="9ddd6-138">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-138">Click Lines.</span></span>
29. <span data-ttu-id="9ddd6-139">[アカウント コード] フィールドで [グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="9ddd6-140">[勘定の選択] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="9ddd6-141">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9ddd6-142">これによって、チャンネルから価格グループ、売買契約へのリンクが完了します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="9ddd6-143">[商品関係] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="9ddd6-144">[通貨金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="9ddd6-145">[次を検索] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="9ddd6-146">[次を検索] が [はい] に設定されている場合、価格決定エンジンは販売価格の低い適用できる売買契約を検索し続けます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="9ddd6-147">[次を検索] が [いいえ] に設定されている場合、価格エンジンは検索を中止し、その売買契約を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="9ddd6-148">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-148">Click Post.</span></span>
36. <span data-ttu-id="9ddd6-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-149">Click OK.</span></span>
37. <span data-ttu-id="9ddd6-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-150">Close the page.</span></span>
38. <span data-ttu-id="9ddd6-151">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="9ddd6-152">[販売価格] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ddd6-152">Click Sales price.</span></span>


