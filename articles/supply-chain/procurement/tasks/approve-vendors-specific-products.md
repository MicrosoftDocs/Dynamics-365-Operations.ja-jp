---
title: 特定の製品の仕入先の承認
description: この手順では、特定の製品に対する仕入先の承認方法を示します。
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431909"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="4ff00-103">特定の製品の仕入先の承認</span><span class="sxs-lookup"><span data-stu-id="4ff00-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ff00-104">この手順では、特定の製品に対する仕入先の承認方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="4ff00-105">'これにより、注文書に製品が追加された際にどの仕入先を使用できるかを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="4ff00-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="4ff00-107">通常、このタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="4ff00-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="4ff00-108">ナビゲーション ウィンドウで、**モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="4ff00-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4ff00-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4ff00-111">**購買** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="4ff00-112">**仕入先** フィールドに主要仕入れ先が表示されている場合は、次のステップでこの仕入先を承認仕入先として追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ff00-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="4ff00-113">仕入先が表示されている場合は、その仕入先番号を記録します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="4ff00-114">アクション ウィンドウで、**購買** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="4ff00-115">**設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-115">Click **Setup**.</span></span>
7. <span data-ttu-id="4ff00-116">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-116">Click **Add**.</span></span>
8. <span data-ttu-id="4ff00-117">[仕入先] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="4ff00-118">承認済の仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-118">Select the approved vendor.</span></span> <span data-ttu-id="4ff00-119">製品レコードに主要仕入先がある場合は、少なくとも明細行の 1 つが主要仕入先である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ff00-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="4ff00-120">これまでに使用した仕入先番号がある場合は、ここでその番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="4ff00-121">**有効期限** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="4ff00-122">2 か月先の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="4ff00-123">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-123">Click **Add**.</span></span>
11. <span data-ttu-id="4ff00-124">**仕入先** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="4ff00-125">**有効期限** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="4ff00-126">前の有効期限とは異なる日付をを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="4ff00-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-127">Close the page.</span></span>
14. <span data-ttu-id="4ff00-128">アクション ウィンドウで、**承認仕入先** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="4ff00-129">**有効期限** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="4ff00-130">この日付は、特定の日付の時点で、誰が承認済仕入先かを確認することができるフィルターとして機能します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="4ff00-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-131">Close the page.</span></span>
17. <span data-ttu-id="4ff00-132">アクション ウィンドウで、**有効期間** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="4ff00-133">**期限切れの仕入先を表示** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="4ff00-134">このページを使用して、特定の日付以降、承認ステータスの有効期限が切れる仕入先を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="4ff00-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-135">Close the page.</span></span>
20. <span data-ttu-id="4ff00-136">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-136">Click **Edit**.</span></span>
21. <span data-ttu-id="4ff00-137">**承認仕入先チェック メソッド** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="4ff00-138">このフィールドを使用して、承認済仕入先ではない仕入先への発注書の明細行に製品が追加された場合に、どのように処理すべきかというポリシーを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="4ff00-139">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-139">Click **Save**.</span></span>
23. <span data-ttu-id="4ff00-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-140">Close the page.</span></span>
24. <span data-ttu-id="4ff00-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-141">Close the page.</span></span>
25. <span data-ttu-id="4ff00-142">ナビゲーション ウィンドウで、**モジュール > 調達 > 仕入先 > 仕入先/品目関係 > 品目別の承認仕入先リスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="4ff00-143">このページは、すべての製品および承認済仕入先の概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="4ff00-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-144">Close the page.</span></span>
27. <span data-ttu-id="4ff00-145">ナビゲーション ウィンドウで、**モジュール > 調達 > 仕入先 > すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="4ff00-146">仕入先から開始し、その仕入先の承認済製品の一覧に移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="4ff00-147">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4ff00-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="4ff00-148">アクション ウィンドウで、**調達** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="4ff00-149">**仕入先別の承認仕入先リスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ff00-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="4ff00-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-150">Close the page.</span></span>
32. <span data-ttu-id="4ff00-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4ff00-151">Close the page.</span></span>

