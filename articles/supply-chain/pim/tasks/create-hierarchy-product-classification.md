---
title: 製品分類の階層の作成
description: この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faf43eb15283ffd7e36ad38728f166884dddcd85
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844828"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="c28cb-103">製品分類の階層の作成</span><span class="sxs-lookup"><span data-stu-id="c28cb-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c28cb-104">この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="c28cb-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c28cb-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c28cb-106">この手順は、カテゴリ マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="c28cb-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="c28cb-107">新しいカテゴリ階層の作成</span><span class="sxs-lookup"><span data-stu-id="c28cb-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="c28cb-108">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 設定 > カテゴリと属性 > カテゴリ階層**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="c28cb-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-109">Click **New**.</span></span>
3. <span data-ttu-id="c28cb-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="c28cb-111">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c28cb-112">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="c28cb-113">階層の構築</span><span class="sxs-lookup"><span data-stu-id="c28cb-113">Build the hierarchy</span></span>
1. <span data-ttu-id="c28cb-114">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-114">Click **New** category node.</span></span>
2. <span data-ttu-id="c28cb-115">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="c28cb-116">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="c28cb-117">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="c28cb-118">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-118">Click **New** category node.</span></span>
6. <span data-ttu-id="c28cb-119">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="c28cb-120">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="c28cb-121">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="c28cb-122">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-122">Click **New** category node.</span></span>
10. <span data-ttu-id="c28cb-123">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="c28cb-124">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="c28cb-125">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="c28cb-126">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-126">Click **New** category node.</span></span>
14. <span data-ttu-id="c28cb-127">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="c28cb-128">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="c28cb-129">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="c28cb-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c28cb-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="c28cb-131">階層の分類</span><span class="sxs-lookup"><span data-stu-id="c28cb-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="c28cb-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="c28cb-133">**アクション ウィンドウ**で、**カテゴリ階層**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="c28cb-134">**階層タイプの関連付け**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="c28cb-135">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-135">Click **New**.</span></span>
5. <span data-ttu-id="c28cb-136">**カテゴリ階層タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="c28cb-137">**製品分類で商品コードのカテゴリ階層タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="c28cb-138">**カテゴリ階層**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c28cb-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c28cb-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c28cb-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c28cb-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c28cb-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c28cb-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c28cb-141">Close the page.</span></span>

