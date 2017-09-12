---
title: "在庫ブロックの作成および管理"
description: "この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。"
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="32dae-103">在庫ブロックの作成および管理</span><span class="sxs-lookup"><span data-stu-id="32dae-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32dae-104">この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="32dae-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="32dae-105">表示されているサンプル値を使用して、デモ データの会社 USMF の手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="32dae-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="32dae-106">この手順を開始する前に、使用可能な現物手持在庫の品目を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32dae-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="32dae-107">在庫ブロックの作成</span><span class="sxs-lookup"><span data-stu-id="32dae-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="32dae-108">[在庫管理] > [定期処理タスク] > [在庫ブロック] に移動します。</span><span class="sxs-lookup"><span data-stu-id="32dae-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="32dae-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32dae-109">Click New.</span></span>
3. <span data-ttu-id="32dae-110">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32dae-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="32dae-111">一覧で、目的の品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="32dae-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="32dae-112">ブロックする現物手持在庫の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="32dae-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="32dae-113">USMF を使用している場合、品目「M9201」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="32dae-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="32dae-114">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32dae-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="32dae-115">品目「M9201」を使用する場合、200 より小さい品目を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32dae-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="32dae-116">[在庫分析コード] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="32dae-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="32dae-117">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32dae-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="32dae-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32dae-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32dae-119">品目「M9201」を使用すると、倉庫 51 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="32dae-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="32dae-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32dae-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="32dae-121">在庫ブロックの条件の更新</span><span class="sxs-lookup"><span data-stu-id="32dae-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="32dae-122">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32dae-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="32dae-123">[在庫数量] フィールドを更新し、ブロックする数量を反映します。</span><span class="sxs-lookup"><span data-stu-id="32dae-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="32dae-124">[予定日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="32dae-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="32dae-125">予定日を割り当てることにより、ブロックされた在庫の引当可能日を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="32dae-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="32dae-126">入庫予定オプションが在庫ブロックに対して選択されている場合、既定通り、ブロックを手動で作成する場合、この日付は予想されるトランザクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="32dae-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="32dae-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32dae-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="32dae-128">在庫ブロックの削除</span><span class="sxs-lookup"><span data-stu-id="32dae-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="32dae-129">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32dae-129">Click Delete.</span></span>
2. <span data-ttu-id="32dae-130">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32dae-130">Click Yes.</span></span>
3. <span data-ttu-id="32dae-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="32dae-131">Close the page.</span></span>

