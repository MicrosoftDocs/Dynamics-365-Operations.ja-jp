--- 
title: "貸与品目の作成"
description: "貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。"
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 950237499441e7f1d5b9e3355c4bd9513ad3783e
ms.openlocfilehash: aa5824a7a56136b6d09860f2ff493359dbeab9f9
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="9b18d-103">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="9b18d-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b18d-104">貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。</span><span class="sxs-lookup"><span data-stu-id="9b18d-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="9b18d-105">個々の現物品目は、対応する貸与品目が必要です。</span><span class="sxs-lookup"><span data-stu-id="9b18d-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="9b18d-106">各貸与品目のレコードに、貸与中の品目、貸与の責任者、および貸与可能な日数を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b18d-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="9b18d-107">キー、アクセス カード、制服などの複数の貸与品目を同時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="9b18d-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="9b18d-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9b18d-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="9b18d-109">貸与タイプの作成</span><span class="sxs-lookup"><span data-stu-id="9b18d-109">Create Loan types</span></span>
1. <span data-ttu-id="9b18d-110">[人事管理] > [作業者] > [貸与品目] > [貸与タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="9b18d-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-111">Click New.</span></span>
3. <span data-ttu-id="9b18d-112">[貸与タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="9b18d-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b18d-114">この貸与タイプに割り当てられた品目を延滞できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="9b18d-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-115">Click Save.</span></span>
7. <span data-ttu-id="9b18d-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9b18d-116">Close the page.</span></span>
8. <span data-ttu-id="9b18d-117">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="9b18d-118">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="9b18d-118">Create Loan items</span></span>
1. <span data-ttu-id="9b18d-119">[人事管理] > [作業者] > [貸与品目] > [貸与品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="9b18d-120">[貸与品目の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-120">Click Create loan items.</span></span>
3. <span data-ttu-id="9b18d-121">[数量] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="9b18d-122">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b18d-123">[貸与タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b18d-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b18d-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b18d-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b18d-126">品目を貸与できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="9b18d-127">[貸与設備] ページの [返却予定] フィールドの既定値は、現在の日付にこの数を加算して計算されます。</span><span class="sxs-lookup"><span data-stu-id="9b18d-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="9b18d-128">[担当者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b18d-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9b18d-129">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-129">Click Select.</span></span>
11. <span data-ttu-id="9b18d-130">[開始値] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="9b18d-131">[間隔] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="9b18d-132">[形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="9b18d-133">たとえば、貸与品目の開始番号が 10 の場合、[形式] フィールドには 2 つの数値記号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-133">For example, if the starting number for a loan item is 10, enter two number symbols in the Format field.</span></span>  
14. <span data-ttu-id="9b18d-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b18d-134">Click OK.</span></span>
15. <span data-ttu-id="9b18d-135">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="9b18d-135">Refresh the page.</span></span>


