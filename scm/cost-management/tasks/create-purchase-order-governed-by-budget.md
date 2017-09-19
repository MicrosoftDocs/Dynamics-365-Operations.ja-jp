--- 
title: "予算に基づく発注書の作成"
description: "この手順を使用して、利用可能な予算の確認をする発注書を作成します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cc024caa54db6629a1e573df295fe8333996647
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="9ffd9-103">予算に基づく発注書の作成</span><span class="sxs-lookup"><span data-stu-id="9ffd9-103">Create a purchase order governed by budget</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ffd9-104">この手順を使用して、利用可能な予算の確認をする発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="9ffd9-105">この記録では、USMF デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="9ffd9-106">予算管理コンフィギュレーションを確認する</span><span class="sxs-lookup"><span data-stu-id="9ffd9-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="9ffd9-107">[予算作成] > [設定] > [予算管理] > [予算管理コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="9ffd9-108">[利用可能な予算財源] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="9ffd9-109">[伝票と仕訳帳] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="9ffd9-110">[予算管理ルールの定義] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="9ffd9-111">[予算グループの定義] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="9ffd9-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="9ffd9-113">発注ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="9ffd9-113">Create the purchase order header</span></span>
1. <span data-ttu-id="9ffd9-114">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9ffd9-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-115">Click New.</span></span>
3. <span data-ttu-id="9ffd9-116">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="9ffd9-117">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-117">Expand the General section.</span></span>
5. <span data-ttu-id="9ffd9-118">[転記日] フィールドで、日付を「2016-01-01」に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="9ffd9-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="9ffd9-120">発注明細行の追加</span><span class="sxs-lookup"><span data-stu-id="9ffd9-120">Add a purchase order line</span></span>
1. <span data-ttu-id="9ffd9-121">[調達カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="9ffd9-122">[数量] を「2」に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="9ffd9-123">[単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="9ffd9-124">[単価] を「10000」に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="9ffd9-125">[財務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-125">Click Financials.</span></span>
6. <span data-ttu-id="9ffd9-126">[金額の配分] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="9ffd9-127">[勘定科目] フィールドで、値「601300-001-023--」を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="9ffd9-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="9ffd9-129">予算確認の実行</span><span class="sxs-lookup"><span data-stu-id="9ffd9-129">Perform budget checking</span></span>
1. <span data-ttu-id="9ffd9-130">[財務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-130">Click Financials.</span></span>
2. <span data-ttu-id="9ffd9-131">[予算確認の実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="9ffd9-132">[財務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-132">Click Financials.</span></span>
4. <span data-ttu-id="9ffd9-133">[予算確認のエラーまたは警告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="9ffd9-134">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9ffd9-134">Click Close.</span></span>

