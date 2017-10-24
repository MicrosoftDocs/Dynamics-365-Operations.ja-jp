--- 
title: "調達カテゴリ階層の設定"
description: "この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="0f935-103">調達カテゴリ階層の設定</span><span class="sxs-lookup"><span data-stu-id="0f935-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f935-104">この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0f935-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="0f935-105">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="0f935-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="0f935-106">この手順を開始する前に、調達タイプのカテゴリ階層が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f935-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="0f935-107">デモ データの会社を使用すると、USMF 会社でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="0f935-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="0f935-108">新しい調達カテゴリを追加します。</span><span class="sxs-lookup"><span data-stu-id="0f935-108">Add a new procurement category</span></span>
1. <span data-ttu-id="0f935-109">次の順に移動します: [調達] > [..]</span><span class="sxs-lookup"><span data-stu-id="0f935-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="0f935-110">> [調達カテゴリ]。</span><span class="sxs-lookup"><span data-stu-id="0f935-110">> Procurement categories.</span></span>
2. <span data-ttu-id="0f935-111">[カテゴリ階層の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="0f935-112">現在の調達カテゴリ階層が、ページの左側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f935-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="0f935-113">階層を修正しようとしています。</span><span class="sxs-lookup"><span data-stu-id="0f935-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="0f935-114">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-114">Click New category node.</span></span>
    * <span data-ttu-id="0f935-115">システムは、既定によりトップ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-115">The system selects the top node by default.</span></span> <span data-ttu-id="0f935-116">タスク ガイドの手順を実行している場合、[ロック解除] ボタンをクリックして、別の親ノードを選択し、新しいノードを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="0f935-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="0f935-117">その場合、タスクのガイドを再度ロックし、[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="0f935-118">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f935-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0f935-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f935-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0f935-120">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f935-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="0f935-121">フレンドリ名はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0f935-121">The friendly name is optional.</span></span> <span data-ttu-id="0f935-122">これは、カテゴリの名前と一緒に、カテゴリのルックアップに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f935-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="0f935-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="0f935-124">新しい調達カテゴリへの製品の追加</span><span class="sxs-lookup"><span data-stu-id="0f935-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="0f935-125">次の順に移動します: [調達] > [..]</span><span class="sxs-lookup"><span data-stu-id="0f935-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="0f935-126">> [調達カテゴリ]。</span><span class="sxs-lookup"><span data-stu-id="0f935-126">> Procurement categories.</span></span>
    * <span data-ttu-id="0f935-127">追加したノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-127">Select the node you just added.</span></span> <span data-ttu-id="0f935-128">タスク ガイドの手順を実行している場合は、ノードを選択するために、タスク ガイドのロック解除が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f935-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="0f935-129">[製品] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="0f935-130">調達カテゴリに製品を関連付けるには、[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="0f935-131">調達カテゴリに追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="0f935-132">製品を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="0f935-133">調達カテゴリに追加する別の製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="0f935-134">製品を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="0f935-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="0f935-136">承認仕入先および優先仕入先の追加</span><span class="sxs-lookup"><span data-stu-id="0f935-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="0f935-137">仕入先セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="0f935-138">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-138">Click Add.</span></span>
    * <span data-ttu-id="0f935-139">この手順を使用して、仕入先を調達カテゴリに追加し、仕入先がカテゴリに望ましいか、またはカテゴリを承認するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0f935-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="0f935-140">カテゴリから仕入先を削除するとき、カテゴリにあるその仕入先との履歴トランザクションは削除されません。</span><span class="sxs-lookup"><span data-stu-id="0f935-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="0f935-141">カテゴリに追加する仕入先を検索します。</span><span class="sxs-lookup"><span data-stu-id="0f935-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="0f935-142">仕入先を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="0f935-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f935-143">Click OK.</span></span>
6. <span data-ttu-id="0f935-144">変更する仕入先の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="0f935-145">[仕入先状態] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="0f935-146">カテゴリのポリシー ルールで設定されている仕入先の選択には、優先するか、承認するか、またはすべての仕入先が購買要求に使用できるかを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f935-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="0f935-147">カテゴリへの補足情報の追加</span><span class="sxs-lookup"><span data-stu-id="0f935-147">Add additional information to the category</span></span>
1. <span data-ttu-id="0f935-148">[仕入先の評価基準グループ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="0f935-149">このタブでは、調達カテゴリの仕入先を評価する基準を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="0f935-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="0f935-150">これを行うには、[追加] をクリックし、希望する基準を含む仕入先評価グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="0f935-151">[アンケート] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="0f935-152">このタブでは、活動タイプを「要求」に設定している場合は、要求に表示されるアンケートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="0f935-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="0f935-153">次に、要求者は、調達カテゴリの特定の 1 つの製品または複数の製品に関する要求を送信する前に、アンケートを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f935-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="0f935-154">[品目売上税グループ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="0f935-155">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f935-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0f935-156">売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f935-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="0f935-157">[カテゴリ ページ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f935-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="0f935-158">カテゴリ ページは、カテゴリ階層ページに作成されます。</span><span class="sxs-lookup"><span data-stu-id="0f935-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="0f935-159">ここには、カテゴリの製品のタイプについての情報やカテゴリの製品の画像などの調達カタログに関する情報や、カテゴリに適用できる割引などの通知に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f935-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="0f935-160">カテゴリ ページの情報は、購買要求に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f935-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="0f935-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0f935-161">Close the page.</span></span>


