---
title: 在庫ブロックの作成および管理
description: この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2408addea3615ffe6dbc4db8baecfdef6a65e839
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145827"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="1488b-103">在庫ブロックの作成および管理</span><span class="sxs-lookup"><span data-stu-id="1488b-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1488b-104">この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1488b-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="1488b-105">表示されているサンプル値を使用して、デモ データの会社 USMF の手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1488b-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="1488b-106">この手順を開始する前に、使用可能な現物手持在庫の品目を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1488b-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="1488b-107">在庫ブロックの作成</span><span class="sxs-lookup"><span data-stu-id="1488b-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="1488b-108">**ナビゲーション ウィンドウ**で、**モジュール > 在庫管理 > 定期処理 > 在庫ブロック**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1488b-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="1488b-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1488b-109">Click **New**.</span></span>
3. <span data-ttu-id="1488b-110">**品目番号**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1488b-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1488b-111">一覧で、目的の品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="1488b-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="1488b-112">ブロックする現物手持在庫の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="1488b-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="1488b-113">USMF を使用している場合、品目 M9201 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1488b-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="1488b-114">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1488b-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1488b-115">品目 M9201 を使用する場合、200 未満を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1488b-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="1488b-116">**在庫分析コード** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="1488b-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="1488b-117">**倉庫**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1488b-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1488b-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1488b-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="1488b-119">品目 M9201 を使用すると、倉庫 51 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1488b-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="1488b-120">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1488b-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="1488b-121">在庫ブロックの条件の更新</span><span class="sxs-lookup"><span data-stu-id="1488b-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="1488b-122">**一般**クイック タブの**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1488b-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="1488b-123">[在庫数量] フィールドを更新し、ブロックする数量を反映します。</span><span class="sxs-lookup"><span data-stu-id="1488b-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="1488b-124">**予定日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1488b-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="1488b-125">予定日を割り当てることにより、ブロックされた在庫の引当可能日を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1488b-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="1488b-126">入庫予定オプションが在庫ブロックに対して選択されている場合、既定通り、ブロックを手動で作成する場合、この日付は予想されるトランザクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1488b-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="1488b-127">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1488b-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="1488b-128">在庫ブロックの削除</span><span class="sxs-lookup"><span data-stu-id="1488b-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="1488b-129">**アクション ウィンドウ**で、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1488b-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="1488b-130">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1488b-130">Click **Yes**.</span></span>
3. <span data-ttu-id="1488b-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1488b-131">Close the page.</span></span>

