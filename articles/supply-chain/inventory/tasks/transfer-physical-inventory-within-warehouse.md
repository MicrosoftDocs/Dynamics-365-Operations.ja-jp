---
title: 倉庫内の現物在庫の移動
description: この手順では、倉庫内の場所間で行われる品目の移動を登録する在庫振替仕訳帳を作成して転記するプロセスを説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cdb66620d5d57a42ce6a2dc443a9276a2e3ca0ae
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203989"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="809d2-103">倉庫内の現物在庫の移動</span><span class="sxs-lookup"><span data-stu-id="809d2-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="809d2-104">この手順では、倉庫内の場所間で行われる品目の移動を登録する在庫振替仕訳帳を作成して転記するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="809d2-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="809d2-105">これを開始する前に、在庫振替用の在庫仕訳帳名を設定してある必要があります。</span><span class="sxs-lookup"><span data-stu-id="809d2-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="809d2-106">この手順を確認するには、示されているサンプル値を使用してデモ データの会社 USMF を使用するか、製品と場所を設定済みの場合に独自のデータを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="809d2-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="809d2-107">通常、これらのタスクを実施するのは、倉庫の従業員です。</span><span class="sxs-lookup"><span data-stu-id="809d2-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="809d2-108">在庫振替仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="809d2-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="809d2-109">**ナビゲーション ウィンドウ**で、**在庫管理 > 仕訳入力 > 品目 > 転送**に移動します。</span><span class="sxs-lookup"><span data-stu-id="809d2-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="809d2-110">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-110">Click **New**.</span></span>
3. <span data-ttu-id="809d2-111">**名前**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="809d2-112">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-112">Click **OK**.</span></span> <span data-ttu-id="809d2-113">仕訳帳明細行ごとに、分析コードの [開始] および [終了] を指定するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="809d2-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="809d2-114">これらは、この仕訳帳タイプでは必須です。</span><span class="sxs-lookup"><span data-stu-id="809d2-114">These are essential for this journal type.</span></span> <span data-ttu-id="809d2-115">各種ルールを使用して複数の場所に品目を移動できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="809d2-116">この例では、同じ倉庫内のライセンス プレートにより制御される場所からライセンス プレートにより制御されない場所に項目を移動します。</span><span class="sxs-lookup"><span data-stu-id="809d2-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="809d2-117">仕訳帳明細行を作成します</span><span class="sxs-lookup"><span data-stu-id="809d2-117">Create journal lines</span></span>
1. <span data-ttu-id="809d2-118">**仕訳帳明細行クイック タブ**で、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="809d2-119">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="809d2-120">USMF を使用すると、'A0001' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="809d2-121">**移動元サイト** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="809d2-122">USMF を使用すると、'2' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="809d2-123">**移動先サイト** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="809d2-124">USMF を使用すると、'2' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="809d2-125">**移動元倉庫**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="809d2-126">USMF を使用すると、'24' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="809d2-127">**移動先倉庫**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="809d2-128">USMF を使用すると、'24' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="809d2-129">**移動元場所**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="809d2-130">USMF を使用すると、'FL-001' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="809d2-131">**移動先場所**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="809d2-132">USMF を使用すると、'BULK-001' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="809d2-133">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="809d2-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="809d2-134">**明細行の詳細**クイック タブで、**在庫分析コード** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="809d2-135">**開始在庫分析コード**、**ライセンス プレート** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809d2-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="809d2-136">USMF を使用すると、'24' を選択できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="809d2-137">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="809d2-138">在庫振替仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="809d2-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="809d2-139">**アクション ウィンドウ**で、**転記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="809d2-140">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="809d2-141">在庫トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="809d2-141">View inventory transactions</span></span>
1. <span data-ttu-id="809d2-142">**在庫**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="809d2-143">**トランザクション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809d2-143">Click **Transactions**.</span></span> <span data-ttu-id="809d2-144">ここで、仕訳帳の転記時に作成されたトランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="809d2-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

