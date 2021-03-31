---
title: 詳細ルール構造の作成と割り当て
description: このトピックでは、詳細なルール構造を作成して勘定構造に割り当てる方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7b9d0c20a49996b4c8d45b030d9e587818de3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216548"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="b6008-103">詳細ルール構造の作成と割り当て</span><span class="sxs-lookup"><span data-stu-id="b6008-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6008-104">このトピックでは、詳細なルール構造を作成して勘定構造に割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6008-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="b6008-105">このガイドでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b6008-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="b6008-106">詳細なルール構造の作成</span><span class="sxs-lookup"><span data-stu-id="b6008-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="b6008-107">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 詳細なルール構造** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6008-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="b6008-108">**新規** を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b6008-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="b6008-109">**詳細なルール構造** フィールドにルール構造を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6008-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="b6008-110">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-110">Select **OK**.</span></span>
5. <span data-ttu-id="b6008-111">**区分の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="b6008-112">区分リストで、財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="b6008-113">たとえば **店舗** です。</span><span class="sxs-lookup"><span data-stu-id="b6008-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="b6008-114">**区分の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="b6008-115">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="b6008-116">詳細ルール構造の勘定構造への適用</span><span class="sxs-lookup"><span data-stu-id="b6008-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="b6008-117">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6008-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="b6008-118">一覧で、詳細ルールを適用する勘定構造を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="b6008-119">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-119">Select **Edit**.</span></span> <span data-ttu-id="b6008-120">**詳細ルール** を選択すると、勘定構造を **ドラフト モード** に設定するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="b6008-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="b6008-121">**詳細ルール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="b6008-122">**新規** を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b6008-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="b6008-123">**詳細ルール** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6008-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="b6008-124">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6008-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="b6008-125">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-125">Select **Create**.</span></span>
9. <span data-ttu-id="b6008-126">**新しい基準の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="b6008-127">**適用箇所** フィールドで、主勘定または財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="b6008-128">**演算子** フィールドで、**is between** や **includes** などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="b6008-129">**値** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6008-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="b6008-130">**終了日** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6008-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="b6008-131">**追加** を選択してドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6008-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="b6008-132">一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。</span><span class="sxs-lookup"><span data-stu-id="b6008-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="b6008-133">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-133">Select **Add**.</span></span>
17. <span data-ttu-id="b6008-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6008-134">Close the page.</span></span>
18. <span data-ttu-id="b6008-135">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6008-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]