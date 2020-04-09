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
ms.openlocfilehash: 4ac87356f46edc118a592acd393823603815917a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150118"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="8885c-103">製品分類の階層の作成</span><span class="sxs-lookup"><span data-stu-id="8885c-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8885c-104">この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8885c-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="8885c-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8885c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8885c-106">この手順は、カテゴリ マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="8885c-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="8885c-107">新しいカテゴリ階層の作成</span><span class="sxs-lookup"><span data-stu-id="8885c-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="8885c-108">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 設定 > カテゴリと属性 > カテゴリ階層**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8885c-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="8885c-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-109">Click **New**.</span></span>
3. <span data-ttu-id="8885c-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8885c-111">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8885c-112">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="8885c-113">階層の構築</span><span class="sxs-lookup"><span data-stu-id="8885c-113">Build the hierarchy</span></span>
1. <span data-ttu-id="8885c-114">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-114">Click **New** category node.</span></span>
2. <span data-ttu-id="8885c-115">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="8885c-116">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="8885c-117">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="8885c-118">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-118">Click **New** category node.</span></span>
6. <span data-ttu-id="8885c-119">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="8885c-120">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="8885c-121">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="8885c-122">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-122">Click **New** category node.</span></span>
10. <span data-ttu-id="8885c-123">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="8885c-124">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="8885c-125">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="8885c-126">**新規**カテゴリ ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-126">Click **New** category node.</span></span>
14. <span data-ttu-id="8885c-127">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="8885c-128">**コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="8885c-129">**フレンドリ名**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8885c-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="8885c-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8885c-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="8885c-131">階層の分類</span><span class="sxs-lookup"><span data-stu-id="8885c-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="8885c-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8885c-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="8885c-133">**アクション ウィンドウ**で、**カテゴリ階層**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="8885c-134">**階層タイプの関連付け**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="8885c-135">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-135">Click **New**.</span></span>
5. <span data-ttu-id="8885c-136">**カテゴリ階層タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8885c-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="8885c-137">**製品分類で商品コードのカテゴリ階層タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8885c-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="8885c-138">**カテゴリ階層**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8885c-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8885c-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8885c-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8885c-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8885c-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8885c-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8885c-141">Close the page.</span></span>

