---
title: 貸与品目の作成
description: 貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178768"
---
# <a name="create-loan-items"></a><span data-ttu-id="4bbe2-103">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="4bbe2-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bbe2-104">貸与品目は、会社が作業者に貸与する電話やコンピューターを含む現物品目を追跡するのに役立つレコードです。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="4bbe2-105">個々の現物品目は、対応する貸与品目が必要です。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="4bbe2-106">各貸与品目のレコードに、貸与中の品目、貸与の責任者、および貸与可能な日数を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="4bbe2-107">キー、アクセス カード、制服などの複数の貸与品目を同時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="4bbe2-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="4bbe2-109">貸与タイプの作成</span><span class="sxs-lookup"><span data-stu-id="4bbe2-109">Create Loan types</span></span>
1. <span data-ttu-id="4bbe2-110">[人事管理] > [作業者] > [貸与品目] > [貸与タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="4bbe2-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-111">Click New.</span></span>
3. <span data-ttu-id="4bbe2-112">[貸与タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="4bbe2-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bbe2-114">この貸与タイプに割り当てられた品目を延滞できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="4bbe2-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-115">Click Save.</span></span>
7. <span data-ttu-id="4bbe2-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-116">Close the page.</span></span>
8. <span data-ttu-id="4bbe2-117">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="4bbe2-118">貸与品目の作成</span><span class="sxs-lookup"><span data-stu-id="4bbe2-118">Create Loan items</span></span>
1. <span data-ttu-id="4bbe2-119">[人事管理] > [作業者] > [貸与品目] > [貸与品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="4bbe2-120">[貸与品目の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-120">Click Create loan items.</span></span>
3. <span data-ttu-id="4bbe2-121">[数量] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="4bbe2-122">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bbe2-123">[貸与タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4bbe2-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4bbe2-125">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4bbe2-126">品目を貸与できる日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="4bbe2-127">[貸与設備] ページの [返却予定] フィールドの既定値は、現在の日付にこの数を加算して計算されます。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="4bbe2-128">[担当者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="4bbe2-129">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-129">Click Select.</span></span>
11. <span data-ttu-id="4bbe2-130">[開始値] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="4bbe2-131">[間隔] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="4bbe2-132">[形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="4bbe2-133">たとえば、貸与品目の開始番号が 10 の場合、[形式] フィールドには 2 つの数値記号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="4bbe2-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-134">Click OK.</span></span>
15. <span data-ttu-id="4bbe2-135">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="4bbe2-135">Refresh the page.</span></span>
