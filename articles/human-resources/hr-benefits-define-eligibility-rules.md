---
title: 給付金の適格性ルールおよびポリシーの定義
description: この記事では、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113229"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="267dc-103">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="267dc-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="267dc-104">このトピックでは、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="267dc-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="267dc-105">給付金の適格性ポリシー ルールのタイプを作成する</span><span class="sxs-lookup"><span data-stu-id="267dc-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="267dc-106">**人事管理 > 給付金 > 適格性 > 給付金の適格性ポリシー タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="267dc-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="267dc-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-107">Select **New**.</span></span>
3. <span data-ttu-id="267dc-108">**ルール名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="267dc-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="267dc-109">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="267dc-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="267dc-110">**クエリ名** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="267dc-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="267dc-111">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="267dc-112">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-112">Select **Save**.</span></span>
8. <span data-ttu-id="267dc-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="267dc-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="267dc-114">給付金の適格性ポリシー</span><span class="sxs-lookup"><span data-stu-id="267dc-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="267dc-115">**人事管理 > 給付金 > 適格性 > 給付金の適格性ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="267dc-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="267dc-116">既存の給付金のポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="267dc-117">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="267dc-118">**ポリシーの組織** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="267dc-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="267dc-119">ここでポリシーに追加する組織を追加・削除できます。</span><span class="sxs-lookup"><span data-stu-id="267dc-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="267dc-120">**ポリシー ルール** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="267dc-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="267dc-121">一覧で、以前に作成したポリシー ルールを検索します。</span><span class="sxs-lookup"><span data-stu-id="267dc-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="267dc-122">**ポリシー ルールの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="267dc-123">**有効日** フィールドに、有効にするポリシーの有効日を入力します。</span><span class="sxs-lookup"><span data-stu-id="267dc-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="267dc-124">有効な終了日を設定することで、将来的にポリシールールを変更することができるため、変更を有効にしたいときにポリシーへの変更を行う手間が省かれます。</span><span class="sxs-lookup"><span data-stu-id="267dc-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="267dc-125">必要に応じて、**条件の追加** フィールドに 「where 句」 を追加します。</span><span class="sxs-lookup"><span data-stu-id="267dc-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="267dc-126">たとえば、営業マネージャーのみにルールを適用したい場合は、where 句を作成して次のように記述します : Where ポジションの説明がセールスマネージャーと等しい。</span><span class="sxs-lookup"><span data-stu-id="267dc-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="267dc-127">ルール内で複数の where 条件をまとめて追加することができます。</span><span class="sxs-lookup"><span data-stu-id="267dc-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="267dc-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-128">Select **OK**.</span></span>
11. <span data-ttu-id="267dc-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="267dc-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="267dc-130">ルールに寄付金を割り当てる</span><span class="sxs-lookup"><span data-stu-id="267dc-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="267dc-131">**人事管理 > 福利厚生 > 福利厚生** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="267dc-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="267dc-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="267dc-133">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="267dc-134">**適格性ルール** のセクションを展開、または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="267dc-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="267dc-135">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-135">Select **Edit**.</span></span>
6. <span data-ttu-id="267dc-136">**適格性** フィールドで、ルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="267dc-137">**ルール タイプ** フィールドで、以前に作成したルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="267dc-138">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="267dc-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="267dc-139">Select **Save**.</span></span>
11. <span data-ttu-id="267dc-140">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="267dc-140">Close the form.</span></span>

