--- 
title: "発注書に記載されている商品の受取の記録"
description: "この手順では、商品の受取を発注書に直接記録する方法を示します。"
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d8a47dac61705831b330f7b4939a18c865a8ace7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="3ff5a-103">発注書に記載されている商品の受取の記録</span><span class="sxs-lookup"><span data-stu-id="3ff5a-103">Record the receipt of goods on the purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ff5a-104">この手順では、商品の受取を発注書に直接記録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="3ff5a-105">製品の受領を倉庫に登録しておき、後で発注書に記録することもできます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="3ff5a-106">このタスクは通常は購買担当者または買掛金勘定コーディネーターが行います。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="3ff5a-107">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="3ff5a-108">この例には、タスク ガイドとして手順を行うことができるように簡単な発注書を作成するステップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="3ff5a-109">独自のデータでこの手順を使用している場合は、「商品の受取の記録」サブタスクから開始します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="3ff5a-110">商品の受取用の新しい発注書の準備</span><span class="sxs-lookup"><span data-stu-id="3ff5a-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="3ff5a-111">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="3ff5a-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-112">Click New.</span></span>
3. <span data-ttu-id="3ff5a-113">[仕入先] フィールドに「US-101」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="3ff5a-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-114">Click OK.</span></span>
5. <span data-ttu-id="3ff5a-115">[品目番号] フィールドに、「M0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="3ff5a-116">[数量] フィールドに「5」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="3ff5a-117">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="3ff5a-118">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="3ff5a-119">商品の受取の記録</span><span class="sxs-lookup"><span data-stu-id="3ff5a-119">Record receipt of goods</span></span>
1. <span data-ttu-id="3ff5a-120">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="3ff5a-121">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-121">Click Product receipt.</span></span>
    * <span data-ttu-id="3ff5a-122">[数量] フィールドでは、入庫する数量に対するさまざまなオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="3ff5a-123">たとえば、数量を事前に倉庫に登録した場合、[登録済数量] を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="3ff5a-124">この例では、[注文済数量] の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="3ff5a-125">[製品受領書] フィールドで、任意の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="3ff5a-126">このフィールドは製品受領書仕訳帳で伝票として使用される参照を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="3ff5a-127">[明細行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="3ff5a-128">数量を '4' に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="3ff5a-129">ここで、注文の行ごとに、入庫中の数量を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="3ff5a-130">[明細] セクションを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="3ff5a-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-131">Click OK.</span></span>
    * <span data-ttu-id="3ff5a-132">これで商品が発注書で入庫済みと記録され、これを反映して製品受領書仕訳帳がドキュメントとして作成されました。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="3ff5a-133">製品受領書のアクションを使用して発注書で作成された仕訳帳を表示し、受け取り製品、および受け取り時期を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3ff5a-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


