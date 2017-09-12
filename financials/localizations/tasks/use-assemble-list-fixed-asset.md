--- 
title: "固定資産の組み立て一覧の使用 (日本)"
description: "日本では、在庫品目を固定資産に移転できます。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b88c0a9fbcb4b28592b8d644f2705c6854b4365
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="use-assemble-list-for-fixed-assets-japan"></a><span data-ttu-id="db7ed-103">固定資産の組み立て一覧の使用 (日本)</span><span class="sxs-lookup"><span data-stu-id="db7ed-103">Use assemble list for fixed assets (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db7ed-104">日本では、在庫品目を固定資産に移転できます。</span><span class="sxs-lookup"><span data-stu-id="db7ed-104">In Japan, you can transfer an inventory item to a fixed asset.</span></span> 



<span data-ttu-id="db7ed-105">このタスクでは、組み立てリストを使用して在庫品目を使用すると同時に、固定資産を作成するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-105">This task walks you through using the assembly list to consume inventory items and create the fixed asset at the same time.</span></span>



<span data-ttu-id="db7ed-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="db7ed-106">This task was created using the demo data company JPMF.</span></span>


## <a name="assign-component-in-an-assembly-list"></a><span data-ttu-id="db7ed-107">組み立て一覧のコンポーネントの割り当て</span><span class="sxs-lookup"><span data-stu-id="db7ed-107">Assign component in an assembly list</span></span>
1. <span data-ttu-id="db7ed-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="db7ed-109">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-109">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="db7ed-110">組み立てリストを割り当てる固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-110">Select the fixed asset that you want to assign the assembly list to.</span></span>  
3. <span data-ttu-id="db7ed-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-111">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="db7ed-112">[コンポーネント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-112">Click Components.</span></span>
5. <span data-ttu-id="db7ed-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-113">Click Add.</span></span>
6. <span data-ttu-id="db7ed-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="db7ed-115">たとえば、「D0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-115">For example: enter 'D0001'</span></span>  
7. <span data-ttu-id="db7ed-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-116">Click Save.</span></span>

## <a name="use-the-assembly-list-to-post-a-fixed-asset-write-up-transaction"></a><span data-ttu-id="db7ed-117">組み立て一覧を使用した固定資産評価増トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="db7ed-117">Use the assembly list to post a fixed asset write-up transaction</span></span>
1. <span data-ttu-id="db7ed-118">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="db7ed-118">Go to Fixed assets > ..</span></span> <span data-ttu-id="db7ed-119">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="db7ed-119">> Fixed assets journal.</span></span>
2. <span data-ttu-id="db7ed-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-120">Click New.</span></span>
3. <span data-ttu-id="db7ed-121">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="db7ed-122">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-122">Click Lines.</span></span>
5. <span data-ttu-id="db7ed-123">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-123">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="db7ed-124">[トランザクション タイプ] フィールドで [評価増調整] を選択します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-124">In the Transaction type field, select 'Write up adjustment'.</span></span>
7. <span data-ttu-id="db7ed-125">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-125">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="db7ed-126">組み立てリストに割り当てた固定資産番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-126">Select the fixed asset number that you have assigned to the assembly list.</span></span>  
8. <span data-ttu-id="db7ed-127">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-127">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="db7ed-128">在庫品目の原価を入力します。</span><span class="sxs-lookup"><span data-stu-id="db7ed-128">Enter the cost of the inventory item.</span></span>  
9. <span data-ttu-id="db7ed-129">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db7ed-129">Click Post.</span></span>


