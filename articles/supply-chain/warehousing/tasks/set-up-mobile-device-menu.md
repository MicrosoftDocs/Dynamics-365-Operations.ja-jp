--- 
title: "発注書の作業を完了するためのモバイル デバイスのメニュー項目の設定"
description: "この手順では、モバイル デバイスのメニュー項目の設定方法について説明します。"
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 37010003ad638e068ed7650532da29c6dbc033cb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="8cec4-103">発注書の作業を完了するためのモバイル デバイスのメニュー項目の設定</span><span class="sxs-lookup"><span data-stu-id="8cec4-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8cec4-104">この手順では、モバイル デバイスのメニュー項目の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="8cec4-105">この例では、メニュー項目は、発注書タイプの作業を実行するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="8cec4-106">メニュー項目に関連付けられている作業クラスにより、有効な作業が決まります。</span><span class="sxs-lookup"><span data-stu-id="8cec4-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="8cec4-107">デモ データの会社 USMF でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="8cec4-108">この手順は通常、倉庫マネージャーによって実施されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="8cec4-109">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="8cec4-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="8cec4-110">[モバイル デバイスのメニュー] 項目に移動します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="8cec4-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-111">Click New.</span></span>
3. <span data-ttu-id="8cec4-112">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="8cec4-113">固有値を入力してください。</span><span class="sxs-lookup"><span data-stu-id="8cec4-113">Enter a unique value.</span></span> <span data-ttu-id="8cec4-114">たとえば、「POMove」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-114">For example, you could type POMove.</span></span> <span data-ttu-id="8cec4-115">この値は後で必要になるので、記憶します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="8cec4-116">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="8cec4-117">これは、モバイル デバイスに表示されるタイトルです。</span><span class="sxs-lookup"><span data-stu-id="8cec4-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="8cec4-118">たとえば、「PO Move」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="8cec4-119">[モード] フィールドで [作業] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="8cec4-120">[既存の作業を使用] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="8cec4-121">このモバイル デバイスのメニュー項目は、既存の作業を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="8cec4-122">したがってこの値を [はい] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cec4-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="8cec4-123">[在庫状態の表示] フィールドは、モバイル デバイス上の倉庫の作業者に、手持在庫の在庫のステータスが表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="8cec4-124">[指示者] フィールドで [システム グループ化] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="8cec4-125">[指示者] フィールドから何かを選択すると、このページの [概要] セクションに追加のフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="8cec4-126">表示されるフィールドは選択内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8cec4-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="8cec4-127">[システム グループ化] を選択すると、新しいフィールドが 2 つ追加されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="8cec4-128">これらについて以下に詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-128">These are explained below.</span></span>  
8. <span data-ttu-id="8cec4-129">[システム グループ化] フィールドで [WorkPoolId] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="8cec4-130">倉庫作業者が、このメニュー項目を開くと、[作業プール ID] をスキャンするように求められます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="8cec4-131">この [作業プール ID] を使用するワーク オーダーすべてと、このメニュー項目に追加された作業クラスの 1 つを使用するオープン ワーク オーダー明細行が、ユーザーにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="8cec4-132">[システム グループ化ラベル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="8cec4-133">これが、モバイル デバイスのユーザーに表示されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="8cec4-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="8cec4-134">たとえば、「Work pool」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="8cec4-135">[プット中のライセンス プレートの上書き] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="8cec4-136">このオプションにより、倉庫作業者はライセンス プレートにより制御されている場所に品目を降ろすときに、ターゲットのライセンス プレートを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="8cec4-137">[グループ プット アウェイ] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="8cec4-138">ワーク オーダーのプット明細行すべてが同じ場所を共有している場合、すべての明細行に対して 1 つの組み合わされたプットの指示が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="8cec4-139">監査テンプレート ID: 作業監査テンプレートを使用すると、別の操作を実行できるように、中断する必要があるメニュー項目の作業プロセスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="8cec4-140">たとえば、このメニュー項目が入荷作業用の場合、監査テンプレートは、作業者が温度を確認するように要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8cec4-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="8cec4-141">プロセスが中断される時点は、たとえば、作業の開始や完了の時点、またはそのステータスが変化した時点などで、監査テンプレートで指定されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="8cec4-142">作業クラスのセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="8cec4-143">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-143">Click New.</span></span>
14. <span data-ttu-id="8cec4-144">[作業クラス ID] フィールドで [購入] を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="8cec4-145">作業プールは、メニュー項目が使用できる作業を制限します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="8cec4-146">この場合、購買作業クラス ID があるオープン ワーク オーダー明細行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="8cec4-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="8cec4-148">作業確認の設定</span><span class="sxs-lookup"><span data-stu-id="8cec4-148">Set up work confirmation</span></span>
1. <span data-ttu-id="8cec4-149">[作業確認の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="8cec4-150">[作業タイプ] フィールドで [ピック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="8cec4-151">[自動確定] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="8cec4-152">作業の種類の選択と作業指示は、自動で確認されます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="8cec4-153">この指示は、ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="8cec4-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="8cec4-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-154">Click New.</span></span>
5. <span data-ttu-id="8cec4-155">[ワーク タイプ] フィールドで [プット] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="8cec4-156">[場所の確認] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="8cec4-157">品目を降ろすときに、倉庫作業者は場所の確認スキャンを実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="8cec4-158">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-158">Click Save.</span></span>
8. <span data-ttu-id="8cec4-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-159">Close the page.</span></span>
9. <span data-ttu-id="8cec4-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="8cec4-161">モバイル デバイス メニューへのメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="8cec4-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="8cec4-162">[モバイル デバイス] メニューに移動します。</span><span class="sxs-lookup"><span data-stu-id="8cec4-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="8cec4-163">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-163">Click Edit.</span></span>
3. <span data-ttu-id="8cec4-164">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8cec4-165">たとえば、「inbound」という値を含む [名前] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="8cec4-166">入荷メニュー項目で使用するメニューを検索するとします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="8cec4-167">USMF では、これは [入荷] と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="8cec4-168">ツリーで、「a value」を選択します</span><span class="sxs-lookup"><span data-stu-id="8cec4-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="8cec4-169">右を指している矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="8cec4-170">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cec4-170">Click Save.</span></span>
7. <span data-ttu-id="8cec4-171">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8cec4-171">Close the page.</span></span>


