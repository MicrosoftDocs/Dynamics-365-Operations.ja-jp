---
title: 勘定構造の作成
description: このタスク ガイドでは、勘定構造の作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916233"
---
# <a name="create-account-structures"></a><span data-ttu-id="e4197-103">勘定構造の作成</span><span class="sxs-lookup"><span data-stu-id="e4197-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4197-104">このタスク ガイドでは、勘定構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4197-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="e4197-105">手順は、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4197-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="e4197-106">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4197-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="e4197-107">**アクション ウィンドウ**で、**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="e4197-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="e4197-108">**勘定構造**フィールドで、勘定構造の目的を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="e4197-109">**説明**フィールドで、勘定構造の目的を指定するための説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="e4197-110">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-110">Click **Create**.</span></span>
6. <span data-ttu-id="e4197-111">**区分および許可された値**で、**区分の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="e4197-112">分析コード リストで、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="e4197-113">リストの最後で、**区分の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="e4197-114">必要に応じて、手順 6 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e4197-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="e4197-115">**許可された値の情報**セクションで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="e4197-116">たとえば、**主勘定**フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="e4197-117">**演算子**フィールドで、is between や includes などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="e4197-118">**値**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="e4197-119">たとえば、600000 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-119">For example, 600000.</span></span>  
13. <span data-ttu-id="e4197-120">**終了日**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-120">In the **through** field, type a value.</span></span> <span data-ttu-id="e4197-121">たとえば、699999 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-121">For example, 699999.</span></span>  
14. <span data-ttu-id="e4197-122">**許可された値の情報**セクションで、**適用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="e4197-123">必要に応じて、手順 10 ～ 15 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e4197-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="e4197-124">**許可された値の情報**セクションで、**新しい基準の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="e4197-125">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="e4197-126">**値**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="e4197-127">たとえば、033 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-127">For example, 033.</span></span>  
19. <span data-ttu-id="e4197-128">**終了日**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-128">In the **through** field, type a value.</span></span> <span data-ttu-id="e4197-129">たとえば、034 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-129">For example, 034.</span></span>  
20. <span data-ttu-id="e4197-130">**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-130">Click **Apply**.</span></span>
21. <span data-ttu-id="e4197-131">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="e4197-132">たとえば、[減価部門] です。</span><span class="sxs-lookup"><span data-stu-id="e4197-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="e4197-133">**CostCenter フィールド**に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="e4197-134">たとえば、007..021 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="e4197-135">**区分および許可された値**で、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="e4197-136">**主勘定**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="e4197-137">たとえば、600000..699999</span><span class="sxs-lookup"><span data-stu-id="e4197-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="e4197-138">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4197-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="e4197-139">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="e4197-139">For example, Department.</span></span>  
26. <span data-ttu-id="e4197-140">[部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-140">In the Department field, type a value.</span></span> <span data-ttu-id="e4197-141">たとえば、032 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-141">For example, 032.</span></span>  
27. <span data-ttu-id="e4197-142">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4197-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="e4197-143">たとえば、086 です。</span><span class="sxs-lookup"><span data-stu-id="e4197-143">For example, 086.</span></span>  
28. <span data-ttu-id="e4197-144">**アクション ウィンドウ**で、**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="e4197-145">**アクション ウィンドウ**で、**有効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="e4197-146">**有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4197-146">Click **Activate**.</span></span>

