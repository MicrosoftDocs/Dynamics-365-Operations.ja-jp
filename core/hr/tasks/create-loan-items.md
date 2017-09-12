--- 
title: "貸与品目の作成"
description: "貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。"
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="ceb0c-103">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="ceb0c-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ceb0c-104">貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="ceb0c-105">個々の現物品目は、対応する貸与品目が必要です。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="ceb0c-106">各貸与品目のレコードに、貸与中の品目、貸与の責任者、および貸与可能な日数を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="ceb0c-107">キー、アクセス カード、制服などの複数の貸与品目を同時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="ceb0c-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="ceb0c-109">貸与タイプの作成</span><span class="sxs-lookup"><span data-stu-id="ceb0c-109">Create Loan types</span></span>
1. <span data-ttu-id="ceb0c-110">[人事管理] > [作業者] > [貸与品目] > [貸与タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="ceb0c-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-111">Click New.</span></span>
3. <span data-ttu-id="ceb0c-112">[貸与タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="ceb0c-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ceb0c-114">この貸与タイプに割り当てられた品目を延滞できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="ceb0c-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-115">Click Save.</span></span>
7. <span data-ttu-id="ceb0c-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-116">Close the page.</span></span>
8. <span data-ttu-id="ceb0c-117">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="ceb0c-118">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="ceb0c-118">Create Loan items</span></span>
1. <span data-ttu-id="ceb0c-119">[人事管理] > [作業者] > [貸与品目] > [貸与品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="ceb0c-120">[貸与品目の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-120">Click Create loan items.</span></span>
3. <span data-ttu-id="ceb0c-121">数量。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-121">In the Qty.</span></span> <span data-ttu-id="ceb0c-122">フィールドで番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-122">field, enter a number.</span></span>
4. <span data-ttu-id="ceb0c-123">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ceb0c-124">[貸与タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ceb0c-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ceb0c-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ceb0c-127">品目を貸与できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="ceb0c-128">[貸与設備] ページの [返却予定] フィールドの既定値は、現在の日付にこの数を加算して計算されます。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="ceb0c-129">[担当者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ceb0c-130">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-130">Click Select.</span></span>
11. <span data-ttu-id="ceb0c-131">[開始値] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="ceb0c-132">[間隔] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="ceb0c-133">[形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="ceb0c-134">たとえば、貸与品目の開始番号が 10 の場合、[形式] フィールドには 2 つの数値記号を入力します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="ceb0c-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-135">Click OK.</span></span>
15. <span data-ttu-id="ceb0c-136">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="ceb0c-136">Refresh the page.</span></span>


