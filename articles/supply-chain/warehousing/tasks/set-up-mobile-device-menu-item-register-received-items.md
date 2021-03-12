---
title: 入庫済品目を登録するためのモバイル デバイスのメニュー項目の設定
description: このトピックでは、モバイル デバイスのメニュー項目の設定を中心に説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6f9cf258a991b88faa0d2db90cd3c21f9703267
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976966"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a><span data-ttu-id="947e0-103">入庫済品目を登録するためのモバイル デバイスのメニュー項目の設定</span><span class="sxs-lookup"><span data-stu-id="947e0-103">Set up a mobile device menu item to register received items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="947e0-104">このトピックでは、モバイル デバイスのメニュー項目の設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="947e0-104">This topic focuses on the setup of a mobile device menu item.</span></span> <span data-ttu-id="947e0-105">このメニュー項目は、発注書によって注文された品目の入庫の登録のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="947e0-105">This menu item is used for registration of the receipt of items ordered via purchase orders.</span></span> 

<span data-ttu-id="947e0-106">デモ データの会社 USMF でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-106">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="947e0-107">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="947e0-107">This procedure is intended for the warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="947e0-108">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="947e0-108">Create a mobile device menu item</span></span>
1. <span data-ttu-id="947e0-109">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー品目** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="947e0-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="947e0-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-110">Select **New**.</span></span>
3. <span data-ttu-id="947e0-111">**メニュー項目名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="947e0-111">In the **Menu item name** field, type a value.</span></span> <span data-ttu-id="947e0-112">これは、このモバイル デバイスのメニュー項目の固有 ID です。</span><span class="sxs-lookup"><span data-stu-id="947e0-112">This is the unique identifier for this mobile device menu item.</span></span> <span data-ttu-id="947e0-113">たとえば、`My PO registration` と入力できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-113">For example, you could type `My PO registration`.</span></span>  
4. <span data-ttu-id="947e0-114">**タイトル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="947e0-114">In the **Title** field, type a value.</span></span> <span data-ttu-id="947e0-115">これは、モバイル デバイスのユーザーに表示されるタイトルです。</span><span class="sxs-lookup"><span data-stu-id="947e0-115">This is the title, which will be displayed to the user on the mobile device.</span></span> <span data-ttu-id="947e0-116">たとえば、`PO registration` と入力できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-116">For example, you could type `PO registration`.</span></span>  
5. <span data-ttu-id="947e0-117">**モード** フィールドで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-117">In the **Mode** field, select **Work**.</span></span> <span data-ttu-id="947e0-118">購買注文明細行に対して受領した手持数量の登録は、入庫エリアから在庫へと品目を移動する作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="947e0-118">Registration of on-hand quantities received for a purchase order line will create work to move the items from the receiving area into the inventory.</span></span> <span data-ttu-id="947e0-119">品目が登録されるまでは作業は作成されません。</span><span class="sxs-lookup"><span data-stu-id="947e0-119">Work isn't created until the items are registered.</span></span> <span data-ttu-id="947e0-120">そのため、**既存の作業を使用** オプションを **いいえ** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="947e0-120">Therefore, leave the **Use existing work** option set to **No**.</span></span>
6. <span data-ttu-id="947e0-121">**一般** セクションの **作業の作成プロセス** フィールドで、**発注書品目受取** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-121">In the **Work creation process** field of the **General** section, select **Purchase order item receiving**.</span></span>
    - <span data-ttu-id="947e0-122">購買注文明細行は、手持在庫が倉庫で登録される前に一意に識別される必要があります。</span><span class="sxs-lookup"><span data-stu-id="947e0-122">A purchase order line must be uniquely identified before on-hand can be registered in the warehouse.</span></span> <span data-ttu-id="947e0-123">このシナリオでは、モバイル デバイスは、発注書の番号および品目番号を登録します。これによりはシステムは購買注文明細行を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="947e0-123">In this scenario, the mobile device will register the purchase order number and item number, and this will allow the system to identify the PO line.</span></span> <span data-ttu-id="947e0-124">プット アウェイ作業が作成され、別の作業者が集荷することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="947e0-124">Put away work will be created and can be picked up by another worker.</span></span> <span data-ttu-id="947e0-125">選択した作業の作成方法は、**一般** クイック タブで、どのフィールドが利用可能になるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="947e0-125">The work creation method that you select determines which fields become available on the **General** FastTab.</span></span>  
    - <span data-ttu-id="947e0-126">**既定のデータの使用** オプションを選択すると、**既定のデータ** ボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="947e0-126">If you select the **Use default data** option, the **Default data** button is enabled.</span></span> <span data-ttu-id="947e0-127">ここで、作業者が毎日の作業で通常必要なデータを表示するようにフィールドを選択できます。これによりそれらの値がモバイル デバイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="947e0-127">Here you can select fields to display data that a worker typically needs in their daily work, so that these values are shown on the mobile device.</span></span>  
    - <span data-ttu-id="947e0-128">**ライセンス プレートのグループ化** パラメータは、受領された品目に割り当てられる単位順序グループと組み合わせて機能します。</span><span class="sxs-lookup"><span data-stu-id="947e0-128">The **License plate grouping** parameter works in combination with the unit sequence group that's assigned to the item that's being received.</span></span> <span data-ttu-id="947e0-129">1 つ以下または 1 つ以上のパレットの受入を 1 枚のライセンス プレートにグループ分けするか、または単位ごとのライセンス プレートに分割するのかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-129">You can specify whether receipts of less than or more than one pallet should be grouped into one license plate, or divided into a separate license plate for each unit.</span></span>  
    - <span data-ttu-id="947e0-130">**ライセンス プレートの生成** オプションを選択する場合、番号順序の選択に基づいて固有のライセンス プレート番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="947e0-130">If you select the **Generate license plate** option, this generates a unique license plate number based on the number sequence selection.</span></span>  
    - <span data-ttu-id="947e0-131">作業の作成時に使用するテンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-131">You can select the template that will be used when work is created.</span></span> <span data-ttu-id="947e0-132">たとえば、発注書の品目を登録する場合、プット アウェイ作業が作業テンプレートに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="947e0-132">For example, if you register an item for a purchase order, the put away work will be generated based on the work template.</span></span> <span data-ttu-id="947e0-133">ここで作業テンプレートを選択しないと、システムはテンプレートに関連するクエリ基準に基づいてテンプレートを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="947e0-133">If you don't select a work template here, the system will assign a template based on the query criteria that are associated with the templates.</span></span>  
    - <span data-ttu-id="947e0-134">廃棄コードがモバイル デバイスに表示されている場合、作業者は品目の状態や品質を評価し、適切なコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-134">If disposition codes are displayed on the mobile device, workers can evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="947e0-135">廃棄コードのルールによって、品目を他の倉庫プロセスで使用できるようにするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="947e0-135">The rules for the disposition code determine whether the items will be available to other warehouse processes.</span></span> <span data-ttu-id="947e0-136">このルールにより、作成された作業にどの場所ディレクティブが使用されるかも決定します。</span><span class="sxs-lookup"><span data-stu-id="947e0-136">The rules also determine which location directive is used for the work that's created.</span></span>   
    - <span data-ttu-id="947e0-137">**バッチ廃棄コード** オプションを選択している場合、作業者はバッチの状態や品質を評価して、適切な廃棄コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="947e0-137">If you select the **Batch disposition codes** option, workers can evaluate the status or quality of a batch, and select the appropriate disposition code.</span></span> <span data-ttu-id="947e0-138">バッチ廃棄コードに設定されているルールによって、バッチが他の倉庫プロセスで使用できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="947e0-138">The rules that are set on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span>  
    - <span data-ttu-id="947e0-139">**ラベルの印刷** オプションを選択した場合、ライセンス プレート ラベルは品目の入荷後自動的に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="947e0-139">If you select the **Print labels** option, a license plate label will be printed automatically when items are received.</span></span>  
7. <span data-ttu-id="947e0-140">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-140">Select **Save**.</span></span>
8. <span data-ttu-id="947e0-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="947e0-141">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="947e0-142">モバイル デバイス メニューへのメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="947e0-142">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="947e0-143">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > モバイル デバイス > モバイル デバイスのメニュー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="947e0-143">In the navigation pane, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
2. <span data-ttu-id="947e0-144">**クイック フィルター** を使用して、`inbound` の値で **名前** フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="947e0-144">Use the **Quick Filter** to filter on the **Name** field with a value of `inbound`.</span></span>
3. <span data-ttu-id="947e0-145">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-145">Select **Edit**.</span></span>
4. <span data-ttu-id="947e0-146">使用できるメニューと品目のツリーで、以前に作成したメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-146">In the Available menus and items tree, select the menu item that you created before.</span></span>
5. <span data-ttu-id="947e0-147">右を指している矢印を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-147">Select the arrow that points to the right.</span></span>
6. <span data-ttu-id="947e0-148">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="947e0-148">Select **Save**.</span></span>
7. <span data-ttu-id="947e0-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="947e0-149">Close the page.</span></span>

