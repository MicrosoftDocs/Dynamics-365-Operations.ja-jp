---
title: 発注書に記載されている商品の受取の記録
description: このトピックでは、商品の受取を発注書に直接記録する方法について説明します。
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa4043aca2e53eae32256a98d556c25b4ec1957
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454790"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="9ce94-103">発注書に記載されている商品の受取の記録</span><span class="sxs-lookup"><span data-stu-id="9ce94-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ce94-104">このトピックでは、商品の受取を発注書に直接記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="9ce94-105">製品の受領を倉庫に登録しておき、後で発注書に記録することもできます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="9ce94-106">このタスクは通常は購買担当者または買掛金勘定コーディネーターが行います。</span><span class="sxs-lookup"><span data-stu-id="9ce94-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="9ce94-107">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9ce94-108">この例には、タスク ガイドとして手順を行うことができるように簡単な発注書を作成するステップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ce94-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="9ce94-109">独自のデータでこの手順を使用している場合は、**商品の受取の記録**サブタスクから開始します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="9ce94-110">商品の受取用の新しい発注書の準備</span><span class="sxs-lookup"><span data-stu-id="9ce94-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="9ce94-111">**ナビゲーション ウィンドウ > モジュール > 調達 > 発注書 > すべての発注書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="9ce94-112">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-112">Select **New**.</span></span>
3. <span data-ttu-id="9ce94-113">**仕入先口座**フィールドに、`US-101` を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="9ce94-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-114">Select **OK**.</span></span>
5. <span data-ttu-id="9ce94-115">**品目番号**フィールドに、`M0001` を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="9ce94-116">**数量**フィールドに、`5` を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="9ce94-117">アクション ウィンドウで、**購買**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="9ce94-118">**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="9ce94-119">商品の受取の記録</span><span class="sxs-lookup"><span data-stu-id="9ce94-119">Record receipt of goods</span></span>
1. <span data-ttu-id="9ce94-120">アクション ウィンドウで、**入庫**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="9ce94-121">**製品受領書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-121">Select **Product receipt**.</span></span> <span data-ttu-id="9ce94-122">**数量**フィールドでは、入庫する数量に対するさまざまなオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="9ce94-123">たとえば、数量を事前に倉庫に登録した場合、**登録済数量**を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="9ce94-124">この例では、**注文済数量**の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="9ce94-125">**概要**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="9ce94-126">**製品受領書**フィールドで、任意の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="9ce94-127">このフィールドは製品受領書仕訳帳で伝票として使用される参照を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="9ce94-128">**明細行**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="9ce94-129">**数量**を「4」に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="9ce94-130">ここで、注文の行ごとに、入庫中の数量を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="9ce94-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ce94-131">Select **OK**.</span></span> <span data-ttu-id="9ce94-132">これで商品が発注書で入庫済みと記録され、これを反映して製品受領書仕訳帳がドキュメントとして作成されました。</span><span class="sxs-lookup"><span data-stu-id="9ce94-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="9ce94-133">製品受領書のアクションを使用して発注書で作成された仕訳帳を表示し、受け取り製品、および受け取り時期を確認できます。</span><span class="sxs-lookup"><span data-stu-id="9ce94-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

