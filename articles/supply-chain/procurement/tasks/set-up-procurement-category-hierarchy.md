---
title: 調達カテゴリ階層の設定
description: この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "334522"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="b7adb-103">調達カテゴリ階層の設定</span><span class="sxs-lookup"><span data-stu-id="b7adb-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7adb-104">この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="b7adb-105">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="b7adb-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="b7adb-106">この手順を開始する前に、調達タイプのカテゴリ階層が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7adb-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="b7adb-107">デモ データの会社を使用すると、USMF 会社でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="b7adb-108">新しい調達カテゴリを追加します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-108">Add a new procurement category</span></span>
1. <span data-ttu-id="b7adb-109">[調達] > [調達カテゴリ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="b7adb-110">[カテゴリ階層の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="b7adb-111">現在の調達カテゴリ階層が、ページの左側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="b7adb-112">階層を修正しようとしています。</span><span class="sxs-lookup"><span data-stu-id="b7adb-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="b7adb-113">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-113">Click New category node.</span></span>
    * <span data-ttu-id="b7adb-114">システムは、既定によりトップ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-114">The system selects the top node by default.</span></span> <span data-ttu-id="b7adb-115">タスク ガイドの手順を実行している場合、[ロック解除] ボタンをクリックして、別の親ノードを選択し、新しいノードを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="b7adb-116">その場合、タスクのガイドを再度ロックし、[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="b7adb-117">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b7adb-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b7adb-119">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="b7adb-120">フレンドリ名はオプションです。</span><span class="sxs-lookup"><span data-stu-id="b7adb-120">The friendly name is optional.</span></span> <span data-ttu-id="b7adb-121">これは、カテゴリの名前と一緒に、カテゴリのルックアップに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="b7adb-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="b7adb-123">新しい調達カテゴリへの製品の追加</span><span class="sxs-lookup"><span data-stu-id="b7adb-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="b7adb-124">[調達] > [調達カテゴリ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="b7adb-125">追加したノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-125">Select the node you just added.</span></span> <span data-ttu-id="b7adb-126">タスク ガイドの手順を実行している場合は、ノードを選択するために、タスク ガイドのロック解除が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7adb-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="b7adb-127">[製品] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="b7adb-128">調達カテゴリに製品を関連付けるには、[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="b7adb-129">調達カテゴリに追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="b7adb-130">製品を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="b7adb-131">調達カテゴリに追加する別の製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="b7adb-132">製品を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="b7adb-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="b7adb-134">承認仕入先および優先仕入先の追加</span><span class="sxs-lookup"><span data-stu-id="b7adb-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="b7adb-135">仕入先セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="b7adb-136">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-136">Click Add.</span></span>
    * <span data-ttu-id="b7adb-137">この手順を使用して、仕入先を調達カテゴリに追加し、仕入先がカテゴリに望ましいか、またはカテゴリを承認するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="b7adb-138">カテゴリから仕入先を削除するとき、カテゴリにあるその仕入先との履歴トランザクションは削除されません。</span><span class="sxs-lookup"><span data-stu-id="b7adb-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="b7adb-139">カテゴリに追加する仕入先を検索します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="b7adb-140">仕入先を選択するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="b7adb-141">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7adb-141">Click OK.</span></span>
6. <span data-ttu-id="b7adb-142">変更する仕入先の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="b7adb-143">[仕入先状態] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="b7adb-144">カテゴリのポリシー ルールで設定されている仕入先の選択には、優先するか、承認するか、またはすべての仕入先が購買要求に使用できるかを設定します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="b7adb-145">カテゴリへの補足情報の追加</span><span class="sxs-lookup"><span data-stu-id="b7adb-145">Add additional information to the category</span></span>
1. <span data-ttu-id="b7adb-146">[仕入先の評価基準グループ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="b7adb-147">このタブでは、調達カテゴリの仕入先を評価する基準を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="b7adb-148">これを行うには、[追加] をクリックし、希望する基準を含む仕入先評価グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="b7adb-149">[アンケート] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="b7adb-150">このタブでは、活動タイプを「要求」に設定している場合は、要求に表示されるアンケートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="b7adb-151">次に、要求者は、調達カテゴリの特定の 1 つの製品または複数の製品に関する要求を送信する前に、アンケートを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7adb-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="b7adb-152">[品目売上税グループ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="b7adb-153">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b7adb-154">売上税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7adb-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="b7adb-155">[カテゴリ ページ] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="b7adb-156">カテゴリ ページは、カテゴリ階層ページに作成されます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="b7adb-157">ここには、カテゴリの製品のタイプについての情報やカテゴリの製品の画像などの調達カタログに関する情報や、カテゴリに適用できる割引などの通知に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7adb-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="b7adb-158">カテゴリ ページの情報は、購買要求に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="b7adb-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b7adb-159">Close the page.</span></span>

