--- 
title: "連続プログラムの使用"
description: "この手順では、連続プログラムの販売と関連する販売注文の処理について説明します。"
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5d3b5690bfbd10b77e784d35d0c4f4518de58333
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="use-a-continuity-program"></a><span data-ttu-id="88ba0-103">連続プログラムの使用</span><span class="sxs-lookup"><span data-stu-id="88ba0-103">Use a continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="88ba0-104">この手順では、連続プログラムの販売と関連する販売注文の処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="88ba0-105">この手順を完了するには、コール センターのユーザーとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88ba0-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="88ba0-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="88ba0-107">[小売りとコマース] > [顧客] > [顧客サービス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="88ba0-108">[SearchText] フィールドに、「Karen」を入力し、[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="88ba0-109">高度な検索ダイアログがポップアップするはずです。</span><span class="sxs-lookup"><span data-stu-id="88ba0-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="88ba0-110">表示されない場合は、このフィールドの右側にある [検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="88ba0-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="88ba0-112">Karen Berg の表示は 1 行のみのはずです。</span><span class="sxs-lookup"><span data-stu-id="88ba0-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="88ba0-113">グリッドの左側のチェックマークの列をクリックして行を選択します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="88ba0-114">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-114">Click Select.</span></span>
5. <span data-ttu-id="88ba0-115">[新しい販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-115">Click New sales order.</span></span>
    * <span data-ttu-id="88ba0-116">販売注文番号を確認することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="88ba0-117">この手順の後半で、それが必要になります。</span><span class="sxs-lookup"><span data-stu-id="88ba0-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="88ba0-118">[品目番号] フィールドに、「88000」を入力し、[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="88ba0-119">これは、USRT デモ データの連続品目です。</span><span class="sxs-lookup"><span data-stu-id="88ba0-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="88ba0-120">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-120">Click Complete.</span></span>
8. <span data-ttu-id="88ba0-121">[支払方法] フィールドに、「Visa」を入力します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="88ba0-122">[クレジット カードの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-122">Click Add credit card.</span></span>
    * <span data-ttu-id="88ba0-123">このページに必須のクレジット カード情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="88ba0-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-124">Click OK.</span></span>
11. <span data-ttu-id="88ba0-125">[支払] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="88ba0-126">コール センター 注文を送信するには、注文の支払いを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88ba0-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="88ba0-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-127">Click OK.</span></span>
13. <span data-ttu-id="88ba0-128">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-128">Click Submit.</span></span>
    * <span data-ttu-id="88ba0-129">新しい連続注文が作成されています。</span><span class="sxs-lookup"><span data-stu-id="88ba0-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="88ba0-130">次に、連続オーダーを処理するのに使用される、2 つのバッチ処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="88ba0-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88ba0-131">Close the page.</span></span>
15. <span data-ttu-id="88ba0-132">[小売りとコマース] > [連続] > [連続の支払い] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="88ba0-133">[連続品目] フィールドに、「88000」を入力し、[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="88ba0-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-134">Click OK.</span></span>
18. <span data-ttu-id="88ba0-135">[小売りとコマース] > [連続] > [連続子注文の作成] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="88ba0-136">このプロセスは、連続プログラムの設定に基づいて新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="88ba0-137">[連続品目] フィールドに、「88000」を入力し、[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="88ba0-138">品目「88000」は、USRT デモ データの連続品目です。</span><span class="sxs-lookup"><span data-stu-id="88ba0-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="88ba0-139">[販売注文] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="88ba0-140">前の手順でメモした販売注文番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="88ba0-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="88ba0-141">これにより、この手順の処理時間は最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="88ba0-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="88ba0-142">[販売注文] フィールドはオプションです--いずれかのプログラムのすべての注文を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="88ba0-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="88ba0-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ba0-143">Click OK.</span></span>


