---
title: 固定資産の分解一覧の使用
description: 日本では、固定資産のコンポーネントを在庫に移転できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetComponentList_JP, AssetComponentPriceCalcDropDialog_JP, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec5f2f12244499fb66a809f645144f7b16780f25
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408164"
---
# <a name="use-disassemble-list-for-fixed-assets"></a><span data-ttu-id="4f414-103">固定資産の分解一覧の使用</span><span class="sxs-lookup"><span data-stu-id="4f414-103">Use disassemble list for fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f414-104">日本では、固定資産のコンポーネントを在庫に移転できます。</span><span class="sxs-lookup"><span data-stu-id="4f414-104">In Japan, you can transfer a component of a fixed asset to inventory.</span></span> 



<span data-ttu-id="4f414-105">このタスクでは、分解の一覧を使用して固定資産の評価減を行うと同時に、棚卸資産を作成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="4f414-105">This task walks you through using the disassembly list to write down the fixed asset, and create the inventory at the same time.</span></span>



<span data-ttu-id="4f414-106">このタスクを完了するには、先に「固定資産の組み立て一覧の使用」の作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f414-106">Before you can complete this task, you must complete the tasks in "Use assemble list of a fixed asset" first.</span></span> 



<span data-ttu-id="4f414-107">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="4f414-107">This task was created using the demo data company JPMF.</span></span>


## <a name="enter-the-disassembly-list"></a><span data-ttu-id="4f414-108">分解リストを入力します。</span><span class="sxs-lookup"><span data-stu-id="4f414-108">Enter the disassembly list</span></span>
1. <span data-ttu-id="4f414-109">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f414-109">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="4f414-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4f414-110">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4f414-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-111">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="4f414-112">[コンポーネント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-112">Click Components.</span></span>
5. <span data-ttu-id="4f414-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4f414-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="4f414-114">[分解リストに追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-114">Click Add to disassembly list.</span></span>
7. <span data-ttu-id="4f414-115">[追加] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f414-115">In the Add field, enter a number.</span></span>
8. <span data-ttu-id="4f414-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-116">Click OK.</span></span>
9. <span data-ttu-id="4f414-117">[分解リスト] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-117">Click the Disassembly list tab.</span></span>
    * <span data-ttu-id="4f414-118">レコードが分解の一覧に追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f414-118">Verify that the record was added to the disassembly list.</span></span>  
    * <span data-ttu-id="4f414-119">オプション: [追加] をクリックして、分解の一覧に品目を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="4f414-119">Optional: You can also choose to add the item to disassembly list by clicking on the add button.</span></span>  
10. <span data-ttu-id="4f414-120">[価格の計算] をクリックすると、ドロップ ダイアログが開きます</span><span class="sxs-lookup"><span data-stu-id="4f414-120">Click Calculate prices to open the drop dialog.</span></span>
11. <span data-ttu-id="4f414-121">[計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-121">Click Calculate.</span></span>
    * <span data-ttu-id="4f414-122">原価が更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f414-122">Verify that the costs are updated.</span></span>  
    * <span data-ttu-id="4f414-123">市場価値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="4f414-123">You can modify the market value.</span></span> <span data-ttu-id="4f414-124">これは固定資産の評価減の貸方金額として仕訳帳に入力されます。</span><span class="sxs-lookup"><span data-stu-id="4f414-124">It will be entered in the journal as the credit amount for the write down of the fixed asset.</span></span>  

## <a name="post-the-disassembly-list"></a><span data-ttu-id="4f414-125">分解リストの転記</span><span class="sxs-lookup"><span data-stu-id="4f414-125">Post the disassembly list</span></span>
1. <span data-ttu-id="4f414-126">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="4f414-126">Go to Fixed assets > ..</span></span> <span data-ttu-id="4f414-127">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="4f414-127">> Fixed assets journal.</span></span>
2. <span data-ttu-id="4f414-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-128">Click New.</span></span>
3. <span data-ttu-id="4f414-129">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f414-129">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4f414-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-130">Click Lines.</span></span>
5. <span data-ttu-id="4f414-131">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f414-131">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="4f414-132">[トランザクション タイプ] フィールドで [評価減調整] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f414-132">In the Transaction type field, select 'Write down adjustment'.</span></span>
7. <span data-ttu-id="4f414-133">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f414-133">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="4f414-134">分解の一覧にある貸方金額が、原価として自動的に取得されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f414-134">Verify that the credit amount is automatically retrieved as the cost from the disassembly list.</span></span>  
    * <span data-ttu-id="4f414-135">貸方金額を変更できます。</span><span class="sxs-lookup"><span data-stu-id="4f414-135">You can modify the credit amount.</span></span>  
8. <span data-ttu-id="4f414-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f414-136">Click Post.</span></span>

