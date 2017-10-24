--- 
title: "固定資産の分解一覧の使用 (日本)"
description: "日本では、固定資産のコンポーネントを在庫に移転できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7248b789db5e396609ad155357feec065f3a1600
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="use-disassemble-list-for-fixed-assets-japan"></a><span data-ttu-id="28655-103">固定資産の分解一覧の使用 (日本)</span><span class="sxs-lookup"><span data-stu-id="28655-103">Use disassemble list for fixed assets (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28655-104">日本では、固定資産のコンポーネントを在庫に移転できます。</span><span class="sxs-lookup"><span data-stu-id="28655-104">In Japan, you can transfer a component of a fixed asset to inventory.</span></span> 



<span data-ttu-id="28655-105">このタスクでは、分解の一覧を使用して固定資産の評価減を行うと同時に、棚卸資産を作成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="28655-105">This task walks you through using the disassembly list to write down the fixed asset, and create the inventory at the same time.</span></span>



<span data-ttu-id="28655-106">このタスクを完了するには、先に「固定資産の組み立て一覧の使用」の作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28655-106">Before you can complete this task, you must complete the tasks in "Use assemble list of a fixed asset" first.</span></span> 



<span data-ttu-id="28655-107">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="28655-107">This task was created using the demo data company JPMF.</span></span>


## <a name="enter-the-disassembly-list"></a><span data-ttu-id="28655-108">分解リストを入力します。</span><span class="sxs-lookup"><span data-stu-id="28655-108">Enter the disassembly list</span></span>
1. <span data-ttu-id="28655-109">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="28655-109">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="28655-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="28655-110">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="28655-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-111">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="28655-112">[コンポーネント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-112">Click Components.</span></span>
5. <span data-ttu-id="28655-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="28655-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="28655-114">[分解リストに追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-114">Click Add to disassembly list.</span></span>
7. <span data-ttu-id="28655-115">[追加] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28655-115">In the Add field, enter a number.</span></span>
8. <span data-ttu-id="28655-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-116">Click OK.</span></span>
9. <span data-ttu-id="28655-117">[分解リスト] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-117">Click the Disassembly list tab.</span></span>
    * <span data-ttu-id="28655-118">レコードが分解の一覧に追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="28655-118">Verify that the record was added to the disassembly list.</span></span>  
    * <span data-ttu-id="28655-119">オプション: [追加] をクリックして、分解の一覧に品目を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="28655-119">Optional: You can also choose to add the item to disassembly list by clicking on the add button.</span></span>  
10. <span data-ttu-id="28655-120">[価格の計算] をクリックすると、ドロップ ダイアログが開きます</span><span class="sxs-lookup"><span data-stu-id="28655-120">Click Calculate prices to open the drop dialog.</span></span>
11. <span data-ttu-id="28655-121">[計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-121">Click Calculate.</span></span>
    * <span data-ttu-id="28655-122">原価が更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="28655-122">Verify that the costs are updated.</span></span>  
    * <span data-ttu-id="28655-123">市場価値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="28655-123">You can modify the market value.</span></span> <span data-ttu-id="28655-124">これは固定資産の評価減の貸方金額として仕訳帳に入力されます。</span><span class="sxs-lookup"><span data-stu-id="28655-124">It will be entered in the journal as the credit amount for the write down of the fixed asset.</span></span>  

## <a name="post-the-disassembly-list"></a><span data-ttu-id="28655-125">分解リストの転記</span><span class="sxs-lookup"><span data-stu-id="28655-125">Post the disassembly list</span></span>
1. <span data-ttu-id="28655-126">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="28655-126">Go to Fixed assets > ..</span></span> <span data-ttu-id="28655-127">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="28655-127">> Fixed assets journal.</span></span>
2. <span data-ttu-id="28655-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-128">Click New.</span></span>
3. <span data-ttu-id="28655-129">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28655-129">In the Name field, type a value.</span></span>
4. <span data-ttu-id="28655-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-130">Click Lines.</span></span>
5. <span data-ttu-id="28655-131">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="28655-131">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="28655-132">[トランザクション タイプ] フィールドで [評価減調整] を選択します。</span><span class="sxs-lookup"><span data-stu-id="28655-132">In the Transaction type field, select 'Write down adjustment'.</span></span>
7. <span data-ttu-id="28655-133">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="28655-133">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="28655-134">分解の一覧にある貸方金額が、原価として自動的に取得されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="28655-134">Verify that the credit amount is automatically retrieved as the cost from the disassembly list.</span></span>  
    * <span data-ttu-id="28655-135">貸方金額を変更できます。</span><span class="sxs-lookup"><span data-stu-id="28655-135">You can modify the credit amount.</span></span>  
8. <span data-ttu-id="28655-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28655-136">Click Post.</span></span>


