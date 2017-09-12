--- 
title: "入庫済品目を登録するためのモバイル デバイスのメニュー項目の設定"
description: "このタスクでは、モバイル デバイスのメニュー項目の設定を中心に説明します。"
author: BibiSp
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
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: de976f6bafbb3d4e2915ab56cdff625877f754f7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a><span data-ttu-id="fdaf5-103">入庫済品目を登録するためのモバイル デバイスのメニュー項目の設定</span><span class="sxs-lookup"><span data-stu-id="fdaf5-103">Set up a mobile device menu item to register received items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fdaf5-104">このタスクでは、モバイル デバイスのメニュー項目の設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-104">This task focuses on the setup of a mobile device menu item.</span></span> <span data-ttu-id="fdaf5-105">このメニュー項目は、発注書によって注文された品目の入庫の登録のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-105">This menu item is used for registration of the receipt of items ordered via purchase orders.</span></span> 

<span data-ttu-id="fdaf5-106">デモ データの会社 USMF でこのガイドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-106">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="fdaf5-107">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-107">This procedure is intended for the warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="fdaf5-108">品目のモバイル デバイス メニューの作成</span><span class="sxs-lookup"><span data-stu-id="fdaf5-108">Create a mobile device menu item</span></span>
1. <span data-ttu-id="fdaf5-109">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-109">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="fdaf5-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-110">Click New.</span></span>
3. <span data-ttu-id="fdaf5-111">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-111">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="fdaf5-112">これは、このモバイル デバイスのメニュー項目の固有 ID です。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-112">This is the unique identifier for this mobile device menu item.</span></span> <span data-ttu-id="fdaf5-113">たとえば、「My PO registration (自分の発注書の登録)」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-113">For example, you could type 'My PO registration'.</span></span>  
4. <span data-ttu-id="fdaf5-114">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-114">In the Title field, type a value.</span></span>
    * <span data-ttu-id="fdaf5-115">これは、モバイル デバイスのユーザーに表示されるタイトルです。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-115">This is the title, which will be displayed to the user on the mobile device.</span></span> <span data-ttu-id="fdaf5-116">たとえば、「PO registration (発注書の登録)」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-116">For example, you could type 'PO registration'.</span></span>  
5. <span data-ttu-id="fdaf5-117">[モード] フィールドで [作業] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-117">In the Mode field, select 'Work'.</span></span>
    * <span data-ttu-id="fdaf5-118">購買注文明細行に対して受領した手持数量の登録は、入庫エリアから在庫へと品目を移動する作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-118">Registration of on-hand quantities received for a purchase order line will create work to move the items from the receiving area into the inventory.</span></span> <span data-ttu-id="fdaf5-119">品目が登録されるまでは作業は作成されません。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-119">Work isn’t created until the items are registered.</span></span>  <span data-ttu-id="fdaf5-120">そのため、[既存の作業を使用] オプションを [いいえ] に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-120">Therefore, leave the Use existing work option set to No.</span></span>  
6. <span data-ttu-id="fdaf5-121">[全般] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-121">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="fdaf5-122">[作業の作成プロセス] フィールドで、「発注書品目受取」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-122">In the Work creation process field, select 'Purchase order item receiving'.</span></span>
    * <span data-ttu-id="fdaf5-123">購買注文明細行は、手持在庫が倉庫で登録される前に一意に識別される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-123">A purchase order line must be uniquely identified before on-hand can be registered in the warehouse.</span></span> <span data-ttu-id="fdaf5-124">このシナリオでは、モバイル デバイスは、発注書の番号および品目番号を登録します。これによりはシステムは購買注文明細行を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-124">In this scenario, the mobile device will register the purchase order number and item number, and this will allow the system to identify the PO line.</span></span> <span data-ttu-id="fdaf5-125">プット アウェイ作業が作成され、別の作業者が集荷することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-125">Put away work will be created and can be picked up by another worker.</span></span>    <span data-ttu-id="fdaf5-126">選択した作業の作成方法は、[一般] クイック タブで、どのフィールドが利用可能になるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-126">The work creation method that you select determines which fields become available on the General fast tab.</span></span>  
    * <span data-ttu-id="fdaf5-127">[既定のデータの使用] オプションを選択すると、[既定のデータ] ボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-127">If you select the Use default data option, the Default data button is enabled.</span></span> <span data-ttu-id="fdaf5-128">ここで、作業者が毎日の作業で通常必要なデータを表示するようにフィールドを選択できます。これによりそれらの値がモバイル デバイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-128">Here you can select fields to display data that a worker typically needs in their daily work, so that these values are shown on the mobile device.</span></span>  
    * <span data-ttu-id="fdaf5-129">ライセンス プレートのグループ化パラメータは、受取中の品目に割り当てられる単位順序グループと組み合わせて機能します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-129">The License plate grouping parameter  works in combination with the unit sequence group that’s assigned to the item that’s being received.</span></span> <span data-ttu-id="fdaf5-130">1 つ以下または 1 つ以上のパレットの受入を 1 枚のライセンス プレートにグループ分けするか、または単位ごとのライセンス プレートに分割するのかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-130">You can specify whether receipts of less than or more than one pallet should be grouped into one license plate, or divided into a separate license plate for each unit.</span></span>  
    * <span data-ttu-id="fdaf5-131">[ライセンス プレートの生成] オプションを選択する場合、番号順序の選択に基づいて固有のライセンス プレート番号が生成されます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-131">If you select the Generate license plate  option, this generates a unique license plate number based on the number sequence selection.</span></span>   
    * <span data-ttu-id="fdaf5-132">作業の作成時に使用するテンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-132">You can select the template that will be used when work is created.</span></span> <span data-ttu-id="fdaf5-133">たとえば、発注書の品目を登録する場合、プット アウェイ作業が作業テンプレートに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-133">For example, if you register an item for a purchase order, the put away work will be generated based on the work template.</span></span> <span data-ttu-id="fdaf5-134">ここで作業テンプレートを選択しないと、システムはテンプレートに関連するクエリ基準に基づいてテンプレートを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-134">If you don’t select a work template here, the system will assign a template based on the query criteria that are associated with the templates.</span></span>  
    * <span data-ttu-id="fdaf5-135">廃棄コードがモバイル デバイスに表示されている場合、作業者は品目の状態や品質を評価し、適切なコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-135">If disposition codes are displayed on the mobile device, workers can evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="fdaf5-136">廃棄コードのルールによって、品目を他の倉庫プロセスで使用できるようにするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-136">The rules for  the disposition code determine whether the items will be available to other warehouse processes.</span></span> <span data-ttu-id="fdaf5-137">このルールにより、作成された作業に使用される場所のディレクティブも決定します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-137">The rules also determine which location directive is used for the work that’s created.</span></span>   
    * <span data-ttu-id="fdaf5-138">[バッチ廃棄コード] オプションを選択している場合、作業者はバッチの状態や品質を評価して、適切な廃棄コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-138">If you select the Batch disposition codes option, workers can evaluate the status or quality of a batch, and select the appropriate disposition code.</span></span>  <span data-ttu-id="fdaf5-139">バッチ廃棄コードに設定されているルールによって、バッチが他の倉庫プロセスで使用できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-139">The rules that are set on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span>  
    * <span data-ttu-id="fdaf5-140">[ラベルの印刷] オプションを選択した場合、ライセンス プレート ラベルは品目の入荷後自動的に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-140">If you select the Print labels option a license plate label will be printed automatically when items are received.</span></span>  
8. <span data-ttu-id="fdaf5-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-141">Click Save.</span></span>
9. <span data-ttu-id="fdaf5-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-142">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="fdaf5-143">モバイル デバイス メニューへのメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="fdaf5-143">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="fdaf5-144">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-144">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
2. <span data-ttu-id="fdaf5-145">クイック フィルターを使用して、「inbound」の値で [名前] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-145">Use the Quick Filter to filter on the Name field with a value of 'inbound'.</span></span>
3. <span data-ttu-id="fdaf5-146">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-146">Click Edit.</span></span>
4. <span data-ttu-id="fdaf5-147">ツリーで、「使用できるメニューと品目のツリーで、以前に作成したメニュー項目を選択する」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-147">In the tree, select 'In the Available menu's and items tree, select the menu item that you created before.'.</span></span>
    * <span data-ttu-id="fdaf5-148">以前に作成したメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-148">Select the menu item that you created before.</span></span>  
5. <span data-ttu-id="fdaf5-149">右を指している矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-149">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="fdaf5-150">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-150">Click Save.</span></span>
7. <span data-ttu-id="fdaf5-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fdaf5-151">Close the page.</span></span>


