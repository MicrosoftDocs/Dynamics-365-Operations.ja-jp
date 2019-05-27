---
title: 倉庫の在庫レベルの調整 (基本倉庫)
description: この手順では、倉庫にある製品の在庫レベルを調整するために、在庫調整仕訳帳を作成して転記するプロセスを説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 330ebacf4a036b2df6ca22728477cae5b347354d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550096"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="2594e-103">倉庫の在庫レベルの調整 (基本倉庫)</span><span class="sxs-lookup"><span data-stu-id="2594e-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2594e-104">この手順では、倉庫にある製品の在庫レベルを調整するために、在庫調整仕訳帳を作成して転記するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="2594e-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="2594e-105">これを開始する前に、在庫調整用の在庫仕訳帳名を設定してある必要があります。</span><span class="sxs-lookup"><span data-stu-id="2594e-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="2594e-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="2594e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="2594e-107">通常、これらのタスクを実施するのは、倉庫の従業員です。</span><span class="sxs-lookup"><span data-stu-id="2594e-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="2594e-108">在庫調整仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="2594e-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="2594e-109">[在庫管理] > [仕訳入力] > [品目] > [在庫調整] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2594e-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="2594e-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-110">Click New.</span></span>
3. <span data-ttu-id="2594e-111">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2594e-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2594e-112">一覧で、使用する在庫調整仕訳帳の名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="2594e-113">他の一部のフィールドは、選択した在庫調整仕訳帳の名前の設定に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="2594e-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="2594e-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="2594e-115">仕訳帳明細行の作成</span><span class="sxs-lookup"><span data-stu-id="2594e-115">Create journal lines</span></span>
1. <span data-ttu-id="2594e-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-116">Click New.</span></span>
2. <span data-ttu-id="2594e-117">一覧で、品目番号フィールドをマークします。</span><span class="sxs-lookup"><span data-stu-id="2594e-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="2594e-118">[品目番号] フィールドで、品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="2594e-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="2594e-119">デモ データの会社 USMF を使用する場合は、「D0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="2594e-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="2594e-120">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2594e-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2594e-121">一覧でサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2594e-121">In the list, select a site.</span></span>
6. <span data-ttu-id="2594e-122">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2594e-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2594e-123">一覧で倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="2594e-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="2594e-124">必須分析コードとして場所を持つ品目を選択した場合は、ここで場所を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2594e-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="2594e-125">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2594e-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2594e-126">原価価格のフィールドには、在庫入庫用に単位あたりの原価を指定します。</span><span class="sxs-lookup"><span data-stu-id="2594e-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="2594e-127">品目番号に対して原価が指定されていない場合、または原価を手動で変更する場合は、ここでそれを行います。</span><span class="sxs-lookup"><span data-stu-id="2594e-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="2594e-128">在庫調整仕訳帳の検証および転記</span><span class="sxs-lookup"><span data-stu-id="2594e-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="2594e-129">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-129">Click Validate.</span></span>
2. <span data-ttu-id="2594e-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-130">Click OK.</span></span>
3. <span data-ttu-id="2594e-131">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-131">Click Post.</span></span>
    * <span data-ttu-id="2594e-132">この種の仕訳帳を転記すると、在庫入庫または在庫出庫が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="2594e-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="2594e-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2594e-133">Click OK.</span></span>
5. <span data-ttu-id="2594e-134">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2594e-134">Close the form.</span></span>
6. <span data-ttu-id="2594e-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2594e-135">Close the page.</span></span>

