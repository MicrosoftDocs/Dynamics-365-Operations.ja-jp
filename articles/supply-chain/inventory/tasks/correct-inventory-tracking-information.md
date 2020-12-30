---
title: 在庫追跡情報の修正
description: この手順は、在庫追跡情報を修正するための在庫振替仕訳帳の作成および転記プロセスについて説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432231"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="19080-103">在庫追跡情報の修正</span><span class="sxs-lookup"><span data-stu-id="19080-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19080-104">この手順は、在庫追跡情報を修正するための在庫振替仕訳帳の作成および転記プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="19080-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="19080-105">この例では、間違って登録したバッチを別のバッチに変更することにより、バッチ管理されている品目の情報が更新されます。</span><span class="sxs-lookup"><span data-stu-id="19080-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="19080-106">デモ データ会社 USPI または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="19080-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="19080-107">独自のデータを使用する場合、バッチ対応の品目が必要であり、場所により制御されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="19080-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="19080-108">在庫振替用に在庫仕訳帳名を設定してある必要もあります。</span><span class="sxs-lookup"><span data-stu-id="19080-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="19080-109">通常、これらのタスクを実施するのは、倉庫の従業員です。</span><span class="sxs-lookup"><span data-stu-id="19080-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="19080-110">在庫振替仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="19080-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="19080-111">[移動] に移動します。</span><span class="sxs-lookup"><span data-stu-id="19080-111">Go to Transfer.</span></span>
2. <span data-ttu-id="19080-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-112">Click New.</span></span>
3. <span data-ttu-id="19080-113">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="19080-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="19080-115">仕訳帳明細行の作成</span><span class="sxs-lookup"><span data-stu-id="19080-115">Create journal lines</span></span>
1. <span data-ttu-id="19080-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-116">Click New.</span></span>
2. <span data-ttu-id="19080-117">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="19080-118">USPI を使用する場合は、 品目 M5003 を選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="19080-119">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19080-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="19080-120">[在庫分析コード] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="19080-121">[バッチ番号] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="19080-122">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="19080-123">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="19080-124">[バッチ番号] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="19080-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="19080-125">仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="19080-125">Post the journal</span></span>
1. <span data-ttu-id="19080-126">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-126">Click Post.</span></span>
2. <span data-ttu-id="19080-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="19080-128">追跡情報の確認</span><span class="sxs-lookup"><span data-stu-id="19080-128">Check tracing information</span></span>
1. <span data-ttu-id="19080-129">[在庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-129">Click Inventory.</span></span>
2. <span data-ttu-id="19080-130">[追跡] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-130">Click Trace.</span></span>
3. <span data-ttu-id="19080-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-131">Click OK.</span></span>
    * <span data-ttu-id="19080-132">この追跡情報を使用して、在庫を修正したバッチを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="19080-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="19080-133">また、[品目追跡] ページを使用して、この情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="19080-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="19080-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="19080-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="19080-135">在庫トランザクションの確認</span><span class="sxs-lookup"><span data-stu-id="19080-135">Check inventory transactions</span></span>
1. <span data-ttu-id="19080-136">[在庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-136">Click Inventory.</span></span>
2. <span data-ttu-id="19080-137">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="19080-137">Click Transactions.</span></span>
    * <span data-ttu-id="19080-138">ここで、仕訳帳の転記時に作成されたトランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="19080-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

