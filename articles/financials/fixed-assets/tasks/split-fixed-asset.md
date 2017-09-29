--- 
title: "固定資産の分割"
description: "このタスク ガイドでは、1 つの資産帳簿を新しい資産帳簿に分割します。"
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="a3394-103">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="a3394-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3394-104">このタスク ガイドでは、1 つの資産帳簿を新しい資産帳簿に分割します。</span><span class="sxs-lookup"><span data-stu-id="a3394-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="a3394-105">これは、経理担当ロールと USMF デモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3394-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="a3394-106">新しい固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="a3394-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="a3394-107">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3394-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="a3394-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-108">Click New.</span></span>
3. <span data-ttu-id="a3394-109">[固定資産グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="a3394-110">分割処理で使用する固定資産番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="a3394-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="a3394-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3394-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="a3394-112">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3394-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="a3394-113">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="a3394-113">Split a fixed asset</span></span>
1. <span data-ttu-id="a3394-114">一覧で、分割する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="a3394-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a3394-116">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-116">Click Books.</span></span>
    * <span data-ttu-id="a3394-117">新しい資産に分割する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="a3394-118">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-118">Click Functions.</span></span>
5. <span data-ttu-id="a3394-119">[固定資産価値の分割] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="a3394-120">[分割先固定資産] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="a3394-121">[次の帳簿まで] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a3394-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a3394-122">[トランザクション日付] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3394-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="a3394-123">[割合] フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="a3394-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="a3394-124">[仕訳帳名] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="a3394-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="a3394-126">仕訳帳トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="a3394-126">Post the journal transaction</span></span>
1. <span data-ttu-id="a3394-127">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3394-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="a3394-128">リストで、分割処理で作成された仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3394-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="a3394-129">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-129">Click Lines.</span></span>
    * <span data-ttu-id="a3394-130">作成した仕訳帳明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="a3394-130">Verify the journal lines created.</span></span>  <span data-ttu-id="a3394-131">取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a3394-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="a3394-132">取得トランザクションは、新しい資産に対して同じ金額で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a3394-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="a3394-133">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3394-133">Click Post.</span></span>


