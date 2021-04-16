---
title: 勘定構造の作成
description: このタスク ガイドでは、勘定構造の作成について説明します。
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aece2b79633802d28ba3b4fd8b51788e26c17a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815167"
---
# <a name="create-account-structures"></a><span data-ttu-id="71a81-103">勘定構造の作成</span><span class="sxs-lookup"><span data-stu-id="71a81-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71a81-104">このタスク ガイドでは、勘定構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="71a81-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="71a81-105">手順は、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="71a81-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="71a81-106">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="71a81-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="71a81-107">**アクション ウィンドウ** で、**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="71a81-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="71a81-108">**勘定構造** フィールドで、勘定構造の目的を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="71a81-109">**説明** フィールドで、勘定構造の目的を指定するための説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="71a81-110">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-110">Click **Create**.</span></span>
6. <span data-ttu-id="71a81-111">**区分および許可された値** で、**区分の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="71a81-112">分析コード リストで、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="71a81-113">リストの最後で、**区分の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="71a81-114">必要に応じて、手順 6 ～ 9 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="71a81-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="71a81-115">**許可された値の情報** セクションで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="71a81-116">たとえば、**主勘定** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="71a81-117">**演算子** フィールドで、is between や includes などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="71a81-118">**値** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="71a81-119">たとえば、600000 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-119">For example, 600000.</span></span>  
13. <span data-ttu-id="71a81-120">**終了日** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-120">In the **through** field, type a value.</span></span> <span data-ttu-id="71a81-121">たとえば、699999 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-121">For example, 699999.</span></span>  
14. <span data-ttu-id="71a81-122">**許可された値の情報** セクションで、**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="71a81-123">必要に応じて、手順 10 ～ 15 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="71a81-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="71a81-124">**許可された値の情報** セクションで、**新しい基準の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="71a81-125">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="71a81-126">**値** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="71a81-127">たとえば、033 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-127">For example, 033.</span></span>  
19. <span data-ttu-id="71a81-128">**終了日** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-128">In the **through** field, type a value.</span></span> <span data-ttu-id="71a81-129">たとえば、034 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-129">For example, 034.</span></span>  
20. <span data-ttu-id="71a81-130">**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-130">Click **Apply**.</span></span>
21. <span data-ttu-id="71a81-131">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="71a81-132">たとえば、[減価部門] です。</span><span class="sxs-lookup"><span data-stu-id="71a81-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="71a81-133">**CostCenter フィールド** に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="71a81-134">たとえば、007..021 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="71a81-135">**区分および許可された値** で、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="71a81-136">**主勘定** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="71a81-137">たとえば、600000..699999</span><span class="sxs-lookup"><span data-stu-id="71a81-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="71a81-138">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="71a81-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="71a81-139">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="71a81-139">For example, Department.</span></span>  
26. <span data-ttu-id="71a81-140">[部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-140">In the Department field, type a value.</span></span> <span data-ttu-id="71a81-141">たとえば、032 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-141">For example, 032.</span></span>  
27. <span data-ttu-id="71a81-142">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="71a81-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="71a81-143">たとえば、086 です。</span><span class="sxs-lookup"><span data-stu-id="71a81-143">For example, 086.</span></span>  
28. <span data-ttu-id="71a81-144">**アクション ウィンドウ** で、**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="71a81-145">**アクション ウィンドウ** で、**有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="71a81-146">**有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71a81-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]