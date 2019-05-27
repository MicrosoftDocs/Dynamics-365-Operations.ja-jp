---
title: 連続スケジュールの定義
description: このトピックでは、連続プログラム (それ以外の場合は、繰り返し注文とも呼ばれます) の設定について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd70780927bb9aaa19c196705d6e8fa1c247ea66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559235"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="faf20-103">連続スケジュールの定義</span><span class="sxs-lookup"><span data-stu-id="faf20-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="faf20-104">このトピックでは、連続プログラム (それ以外の場合は、繰り返し注文とも呼ばれます) の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="faf20-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="faf20-105">このトピックでは、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="faf20-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="faf20-106">連続プログラムの作成</span><span class="sxs-lookup"><span data-stu-id="faf20-106">Create continuity program</span></span>
1. <span data-ttu-id="faf20-107">[小売りとコマース] > [連続] > [連続 プログラム] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="faf20-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="faf20-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-108">Click New.</span></span>
3. <span data-ttu-id="faf20-109">スケジュール ID フィールドで、[連続スケジュール ID] と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="faf20-110">[注文の開始] フィールドで、「最初のイベント」を選択します。</span><span class="sxs-lookup"><span data-stu-id="faf20-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="faf20-111">顧客が連続プログラムの新しい注文を配置する場合は、どの製品を出荷するかについて 2 つのオプションがあります: 1。</span><span class="sxs-lookup"><span data-stu-id="faf20-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="faf20-112">最初のイベント: 連続プログラムで最初の製品を出荷します。</span><span class="sxs-lookup"><span data-stu-id="faf20-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="faf20-113">2.</span><span class="sxs-lookup"><span data-stu-id="faf20-113">2.</span></span> <span data-ttu-id="faf20-114">現在のイベント: 現在の製品が出荷されます。</span><span class="sxs-lookup"><span data-stu-id="faf20-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="faf20-115">例えば、</span><span class="sxs-lookup"><span data-stu-id="faf20-115">For example.</span></span> <span data-ttu-id="faf20-116">3 か月間のプログラムで、顧客はプログラムの 3 番目を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="faf20-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="faf20-117">注文の開始日を確認するには、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="faf20-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="faf20-118">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-118">Click Add line.</span></span>
7. <span data-ttu-id="faf20-119">[品目番号] フィールドで、最初の品目番号 (0013) を入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="faf20-120">[CP] と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-120">Type 'CP'.</span></span>
9. <span data-ttu-id="faf20-121">最初の製品が注文できる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="faf20-122">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-122">Click Add line.</span></span>
11. <span data-ttu-id="faf20-123">[品目番号] フィールドで「0014」と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="faf20-124">日付間隔コードフィールドで、値をオフにすると、フィールドは空になります。</span><span class="sxs-lookup"><span data-stu-id="faf20-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="faf20-125">この手順で、日付範囲をオフにします。</span><span class="sxs-lookup"><span data-stu-id="faf20-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="faf20-126">最初の品目の増分日付として開始日付を設定します。</span><span class="sxs-lookup"><span data-stu-id="faf20-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="faf20-127">ここでは、製品を出荷する間隔を入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="faf20-128">タイプ「30」。</span><span class="sxs-lookup"><span data-stu-id="faf20-128">Type '30'.</span></span>
    * <span data-ttu-id="faf20-129">月ごとのプログラムの場合、間隔は 30 日と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="faf20-130">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-130">Click Add line.</span></span>
15. <span data-ttu-id="faf20-131">[品目番号] フィールドで「0015」と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="faf20-132">[終了] と入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-132">Type 'End'.</span></span>
17. <span data-ttu-id="faf20-133">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="faf20-134">連続品目に割り当てます</span><span class="sxs-lookup"><span data-stu-id="faf20-134">Assign to continuity item</span></span>
1. <span data-ttu-id="faf20-135">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="faf20-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="faf20-136">品目「0016」を選択します。</span><span class="sxs-lookup"><span data-stu-id="faf20-136">Select item '0016'.</span></span>
    * <span data-ttu-id="faf20-137">この手順では、品目番号 0016 を選択します。</span><span class="sxs-lookup"><span data-stu-id="faf20-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="faf20-138">通常、コール センターの販売注文時に適用される、追加の連続ビジネス ロジックがあるリリースされた製品を作成しています。</span><span class="sxs-lookup"><span data-stu-id="faf20-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="faf20-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="faf20-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-140">Click Edit.</span></span>
5. <span data-ttu-id="faf20-141">[販売] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="faf20-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="faf20-142">ここでは、この品目が示す連続プログラムを入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="faf20-143">前に作成したスケジュール ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="faf20-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="faf20-144">この品目がコールセンターで販売される場合、追加のビジネス ロジックは、選択した連続プログラムから適用されます。</span><span class="sxs-lookup"><span data-stu-id="faf20-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="faf20-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="faf20-145">Click Save.</span></span>

