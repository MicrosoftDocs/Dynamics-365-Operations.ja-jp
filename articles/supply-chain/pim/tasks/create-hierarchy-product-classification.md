---
title: 製品分類の階層の作成
description: この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431965"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="9fc4e-103">製品分類の階層の作成</span><span class="sxs-lookup"><span data-stu-id="9fc4e-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fc4e-104">この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="9fc4e-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9fc4e-106">この手順は、カテゴリ マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="9fc4e-107">新しいカテゴリ階層の作成</span><span class="sxs-lookup"><span data-stu-id="9fc4e-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="9fc4e-108">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 設定 > カテゴリと属性 > カテゴリ階層** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="9fc4e-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-109">Click **New**.</span></span>
3. <span data-ttu-id="9fc4e-110">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="9fc4e-111">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9fc4e-112">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="9fc4e-113">階層の構築</span><span class="sxs-lookup"><span data-stu-id="9fc4e-113">Build the hierarchy</span></span>
1. <span data-ttu-id="9fc4e-114">**新規** カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-114">Click **New** category node.</span></span>
2. <span data-ttu-id="9fc4e-115">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="9fc4e-116">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="9fc4e-117">**フレンドリ名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="9fc4e-118">**新規** カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-118">Click **New** category node.</span></span>
6. <span data-ttu-id="9fc4e-119">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="9fc4e-120">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="9fc4e-121">**フレンドリ名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="9fc4e-122">**新規** カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-122">Click **New** category node.</span></span>
10. <span data-ttu-id="9fc4e-123">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="9fc4e-124">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="9fc4e-125">**フレンドリ名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="9fc4e-126">**新規** カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-126">Click **New** category node.</span></span>
14. <span data-ttu-id="9fc4e-127">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="9fc4e-128">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="9fc4e-129">**フレンドリ名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="9fc4e-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="9fc4e-131">階層の分類</span><span class="sxs-lookup"><span data-stu-id="9fc4e-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="9fc4e-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="9fc4e-133">**アクション ウィンドウ** で、**カテゴリ階層** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="9fc4e-134">**階層タイプの関連付け** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="9fc4e-135">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-135">Click **New**.</span></span>
5. <span data-ttu-id="9fc4e-136">**カテゴリ階層タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="9fc4e-137">**製品分類で商品コードのカテゴリ階層タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="9fc4e-138">**カテゴリ階層** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9fc4e-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9fc4e-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9fc4e-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9fc4e-141">Close the page.</span></span>

