---
title: 注文保留の管理
description: この手順では、顧客の販売注文を保留に設定する方法、注文保留のチェックアウトの処理の方法、および注文保留の解除方法について説明します。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb3c6941af132f9ea1bf9f52f94cd6acc008d6c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830059"
---
# <a name="manage-order-holds"></a><span data-ttu-id="77f45-103">注文保留の管理</span><span class="sxs-lookup"><span data-stu-id="77f45-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77f45-104">この手順では、顧客の販売注文を保留に設定する方法、注文保留のチェックアウトの処理の方法、および注文保留の解除方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="77f45-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="77f45-105">注文はさまざまな理由で保留に設定される場合があります。</span><span class="sxs-lookup"><span data-stu-id="77f45-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="77f45-106">たとえば、顧客の住所や支払方法が確認できるまで、またはマネージャーが顧客の与信限度額を確認できるまで、注文を保留にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="77f45-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="77f45-107">注文の保留中、倉庫では出荷の処理はできません。</span><span class="sxs-lookup"><span data-stu-id="77f45-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="77f45-108">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="77f45-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="77f45-109">注文保留の設定</span><span class="sxs-lookup"><span data-stu-id="77f45-109">Set up order holds</span></span>
1. <span data-ttu-id="77f45-110">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 設定 > 販売注文 > 注文保留コード**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="77f45-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="77f45-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-111">Click **New**.</span></span>
3. <span data-ttu-id="77f45-112">**保留コード**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77f45-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="77f45-113">たとえば、「コールバック」を入力します。</span><span class="sxs-lookup"><span data-stu-id="77f45-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="77f45-114">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77f45-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="77f45-115">たとえば、顧客からのコールバック待ちの注文。</span><span class="sxs-lookup"><span data-stu-id="77f45-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="77f45-116">必要に応じて、この保留コードが追加されるときに注文から現物引当を削除するために、**引当の削除**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="77f45-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="77f45-117">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="77f45-118">注文を保留</span><span class="sxs-lookup"><span data-stu-id="77f45-118">Place order on hold</span></span>
1. <span data-ttu-id="77f45-119">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 販売注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="77f45-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="77f45-120">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-120">Click **New**.</span></span>
3. <span data-ttu-id="77f45-121">**顧客口座**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="77f45-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="77f45-122">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-122">Click **OK**.</span></span>
5. <span data-ttu-id="77f45-123">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="77f45-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="77f45-124">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77f45-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="77f45-125">**アクション ペイン**で、**販売注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="77f45-126">**保留注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="77f45-127">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-127">Click **New**.</span></span>
10. <span data-ttu-id="77f45-128">**保留コード**フィールドで、前のサブタスクで作成したコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="77f45-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="77f45-129">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-129">Click **Save**.</span></span>
12. <span data-ttu-id="77f45-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="77f45-130">Close the page.</span></span>
13. <span data-ttu-id="77f45-131">**販売とマーケティング > 販売注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="77f45-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="77f45-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="77f45-132">In the list, mark the selected row.</span></span> <span data-ttu-id="77f45-133">現在保留中の注文は、「処理禁止」フィールドと「保留中」フィールドのマークが付きます。</span><span class="sxs-lookup"><span data-stu-id="77f45-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="77f45-134">アクション ウィンドウで、**ピッキングと梱包**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="77f45-135">注文保留の管理</span><span class="sxs-lookup"><span data-stu-id="77f45-135">Manage order holds</span></span>
1. <span data-ttu-id="77f45-136">**販売とマーケティング > 販売注文 > オープン注文 > 注文保留**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="77f45-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="77f45-137">**注文保留**ページはワークベンチとして機能し、このワークベンチで、現在の保留と処理済みの保留のすべての概要を取得して、それらおよび関連付けられている販売注文を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="77f45-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="77f45-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="77f45-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="77f45-139">**アクション ウィンドウ**で、**保留チェックアウト**クリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="77f45-140">**チェック アウト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-140">Click **Check out**.</span></span>
5. <span data-ttu-id="77f45-141">一覧で、選択された行のマークを解除します。</span><span class="sxs-lookup"><span data-stu-id="77f45-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="77f45-142">**チェック アウト先**フィールドにユーザー ID が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="77f45-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="77f45-143">**チェック アウトをクリア**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="77f45-144">**アクション ウィンドウ**で、**保留の解除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="77f45-145">保留の解除と、注文が次のフルフィルメント ステップに進む準備ができたら、保留を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77f45-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="77f45-146">注文に変更が必要がない場合は、[保留の解除] アクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="77f45-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="77f45-147">ただし、保留を解除するときに注文を更新する必要がある場合、[アクションの解除と変更] アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="77f45-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="77f45-148">**解除と送信**アクションは、コール センター機能を使用するときだけ適用可能です。</span><span class="sxs-lookup"><span data-stu-id="77f45-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="77f45-149">**保留の解除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77f45-149">Click **Clear holds**.</span></span> <span data-ttu-id="77f45-150">注文から保留が解除され、有効な保留のリストから削除されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="77f45-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="77f45-151">特定の状態に基づいてすべての保留中またはされらのサブセットを表示するには、[表示] フィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="77f45-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

