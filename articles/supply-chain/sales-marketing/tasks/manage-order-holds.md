--- 
title: "注文保留の管理"
description: "この手順では、顧客の販売注文を保留に設定する方法、注文保留のチェックアウトの処理の方法、および注文保留の解除方法について説明します。"
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5e51cd1245c578762791e7fe023c36e6fd779086
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="manage-order-holds"></a><span data-ttu-id="88318-103">注文保留の管理</span><span class="sxs-lookup"><span data-stu-id="88318-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88318-104">この手順では、顧客の販売注文を保留に設定する方法、注文保留のチェックアウトの処理の方法、および注文保留の解除方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88318-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="88318-105">注文はさまざまな理由で保留に設定される場合があります。</span><span class="sxs-lookup"><span data-stu-id="88318-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="88318-106">たとえば、顧客の住所や支払方法が確認できるまで、またはマネージャーが顧客の与信限度額を確認できるまで、注文を保留にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="88318-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="88318-107">注文の保留中、倉庫では出荷の処理はできません。</span><span class="sxs-lookup"><span data-stu-id="88318-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="88318-108">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="88318-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="88318-109">注文保留の設定</span><span class="sxs-lookup"><span data-stu-id="88318-109">Set up order holds</span></span>
1. <span data-ttu-id="88318-110">[販売とマーケティング] > [設定] > [販売注文] > [注文保留コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88318-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="88318-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-111">Click New.</span></span>
3. <span data-ttu-id="88318-112">[保留コード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88318-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="88318-113">たとえば、コールバックを入力します。</span><span class="sxs-lookup"><span data-stu-id="88318-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="88318-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88318-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="88318-115">たとえば、顧客からのコールバック待ちの注文。</span><span class="sxs-lookup"><span data-stu-id="88318-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="88318-116">必要に応じて、この保留コードが追加されるときに注文から現物引当を削除するために、[引当の削除] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="88318-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="88318-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="88318-118">注文を保留</span><span class="sxs-lookup"><span data-stu-id="88318-118">Place order on hold</span></span>
1. <span data-ttu-id="88318-119">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88318-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="88318-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-120">Click New.</span></span>
3. <span data-ttu-id="88318-121">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88318-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="88318-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-122">Click OK.</span></span>
5. <span data-ttu-id="88318-123">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88318-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="88318-124">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88318-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="88318-125">アクション ウィンドウで、[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="88318-126">[注文保留] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-126">Click Order holds.</span></span>
9. <span data-ttu-id="88318-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-127">Click New.</span></span>
10. <span data-ttu-id="88318-128">[保留コード] フィールドで、前のサブタスクで作成したコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="88318-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="88318-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-129">Click Save.</span></span>
12. <span data-ttu-id="88318-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88318-130">Close the page.</span></span>
13. <span data-ttu-id="88318-131">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88318-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="88318-132">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88318-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="88318-133">現在保留中の注文は、「処理禁止」フィールドと「保留中」フィールドのマークが付きます。</span><span class="sxs-lookup"><span data-stu-id="88318-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="88318-134">アクション ウィンドウで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="88318-135">注文保留の管理</span><span class="sxs-lookup"><span data-stu-id="88318-135">Manage order holds</span></span>
1. <span data-ttu-id="88318-136">[販売とマーケティング] > [販売注文] > [オープン注文] > [注文保留] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88318-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="88318-137">注文保留ページはワークベンチとして機能し、このワークベンチで、現在の保留と処理済みの保留のすべての概要を取得して、それらおよび関連付けられている販売注文を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="88318-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="88318-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88318-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="88318-139">[アクション] ウィンドウで、[保留チェックアウト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="88318-140">[チェックアウト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-140">Click Check out.</span></span>
5. <span data-ttu-id="88318-141">一覧で、選択された行のマークを解除します。</span><span class="sxs-lookup"><span data-stu-id="88318-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="88318-142">[チェックアウト先] フィールドにユーザー ID が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="88318-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="88318-143">[チェックアウトをクリア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="88318-144">[アクション] ペインで、[保留の解除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="88318-145">保留の解除と、注文が次のフルフィルメント ステップに進む準備ができたら、保留を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88318-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="88318-146">注文に変更が必要がない場合は、[保留の解除] アクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88318-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="88318-147">ただし、保留を解除するときに注文を更新する必要がある場合、[アクションの解除と変更] アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="88318-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="88318-148">解除して送信のアクションは、コール センター機能を使用するときだけ適用可能です。</span><span class="sxs-lookup"><span data-stu-id="88318-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="88318-149">[保留の解除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88318-149">Click Clear holds.</span></span>
    * <span data-ttu-id="88318-150">注文から保留が解除され、有効な保留のリストから削除されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="88318-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="88318-151">特定の状態に基づいてすべての保留中またはされらのサブセットを表示するには、[表示] フィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="88318-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     


