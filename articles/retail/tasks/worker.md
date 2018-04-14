--- 
title: "作業者のコンフィギュレーション"
description: "この手順では、POSの販売手数料が適用される販売員としての小売従事者を環境設定する方法を示します。"
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5e168c4d0b4e48b73d4a31ca8525e2aeb288846c
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="325e3-103">作業者のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="325e3-103">Configure a worker</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="325e3-104">この手順では、POSの販売手数料が適用される販売員としての小売従事者を環境設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="325e3-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="325e3-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="325e3-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="325e3-106">作業者向け委託販売グループを作成する</span><span class="sxs-lookup"><span data-stu-id="325e3-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="325e3-107">[販売とマーケティング] > [コミッション] > [販売グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="325e3-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="325e3-108">作業者は複数の販売グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="325e3-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="325e3-109">POSで、店舗のアドレス帳記載の作業者を含む販売グループを選択できます。</span><span class="sxs-lookup"><span data-stu-id="325e3-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="325e3-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-110">Click New.</span></span>
3. <span data-ttu-id="325e3-111">[グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="325e3-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="325e3-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="325e3-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="325e3-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-113">Click Save.</span></span>
6. <span data-ttu-id="325e3-114">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="325e3-115">[販売担当者] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-115">Click Sales rep.</span></span>
    * <span data-ttu-id="325e3-116">販売グループには複数の作業者を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="325e3-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="325e3-117">手数料は、その分配方法に基づき作業者間で分配することができます。</span><span class="sxs-lookup"><span data-stu-id="325e3-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="325e3-118">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="325e3-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="325e3-119">[手数料分配] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="325e3-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="325e3-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-120">Click Save.</span></span>
11. <span data-ttu-id="325e3-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="325e3-121">Close the page.</span></span>
12. <span data-ttu-id="325e3-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="325e3-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="325e3-123">作業者を既定の販売グループに割り当てる</span><span class="sxs-lookup"><span data-stu-id="325e3-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="325e3-124">[小売りとコマース] > [従業員] > [作業者] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="325e3-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="325e3-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="325e3-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="325e3-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="325e3-127">[小売] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="325e3-128">作業者は、既定の販売グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="325e3-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="325e3-129">既定の販売グループは、店舗の機能プロファイルでオプションが有効になっていればPOSの販売明細行に自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="325e3-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="325e3-130">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-130">Click Edit.</span></span>
6. <span data-ttu-id="325e3-131">[既定のグループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="325e3-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="325e3-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="325e3-132">Click Save.</span></span>


