--- 
title: "製品分類の階層の作成"
description: "この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="6e5c6-103">製品分類の階層の作成</span><span class="sxs-lookup"><span data-stu-id="6e5c6-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e5c6-104">この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="6e5c6-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e5c6-106">この手順は、カテゴリ マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="6e5c6-107">新しいカテゴリ階層の作成</span><span class="sxs-lookup"><span data-stu-id="6e5c6-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="6e5c6-108">[製品情報管理] > [設定] > [カテゴリと属性] > [カテゴリ階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="6e5c6-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-109">Click New.</span></span>
3. <span data-ttu-id="6e5c6-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6e5c6-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6e5c6-112">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="6e5c6-113">階層の構築</span><span class="sxs-lookup"><span data-stu-id="6e5c6-113">Build the hierarchy</span></span>
1. <span data-ttu-id="6e5c6-114">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-114">Click New category node.</span></span>
2. <span data-ttu-id="6e5c6-115">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="6e5c6-116">[コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="6e5c6-117">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="6e5c6-118">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-118">Click New category node.</span></span>
6. <span data-ttu-id="6e5c6-119">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="6e5c6-120">[コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="6e5c6-121">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="6e5c6-122">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-122">Click New category node.</span></span>
10. <span data-ttu-id="6e5c6-123">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="6e5c6-124">[コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="6e5c6-125">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="6e5c6-126">[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-126">Click New category node.</span></span>
14. <span data-ttu-id="6e5c6-127">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="6e5c6-128">[コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="6e5c6-129">[フレンドリ名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="6e5c6-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="6e5c6-131">階層の分類</span><span class="sxs-lookup"><span data-stu-id="6e5c6-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="6e5c6-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="6e5c6-133">アクション ウィンドウで、[カテゴリ階層] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="6e5c6-134">[階層タイプの関連付け] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="6e5c6-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-135">Click New.</span></span>
5. <span data-ttu-id="6e5c6-136">[カテゴリ階層タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="6e5c6-137">製品分類で商品コードのカテゴリ階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="6e5c6-138">[カテゴリ階層] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6e5c6-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6e5c6-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6e5c6-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6e5c6-141">Close the page.</span></span>


