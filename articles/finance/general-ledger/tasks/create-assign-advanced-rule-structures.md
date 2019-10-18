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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175515"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="5f51f-103">詳細ルール構造の作成と割り当て</span><span class="sxs-lookup"><span data-stu-id="5f51f-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f51f-104">このトピックでは、詳細なルール構造を作成して勘定構造に割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="5f51f-105">このガイドでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="5f51f-106">詳細なルール構造の作成</span><span class="sxs-lookup"><span data-stu-id="5f51f-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="5f51f-107">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 詳細なルール構造**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="5f51f-108">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="5f51f-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="5f51f-109">**詳細なルール構造**フィールドにルール構造を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="5f51f-110">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-110">Select **OK**.</span></span>
5. <span data-ttu-id="5f51f-111">**区分の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="5f51f-112">区分リストで、財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="5f51f-113">たとえば**店舗**です。</span><span class="sxs-lookup"><span data-stu-id="5f51f-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="5f51f-114">**区分の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="5f51f-115">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="5f51f-116">詳細ルール構造の勘定構造への適用</span><span class="sxs-lookup"><span data-stu-id="5f51f-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="5f51f-117">**ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="5f51f-118">一覧で、詳細ルールを適用する勘定構造を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="5f51f-119">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-119">Select **Edit**.</span></span> <span data-ttu-id="5f51f-120">**詳細ルール**を選択すると、勘定構造を**ドラフト モード**に設定するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="5f51f-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="5f51f-121">**詳細ルール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="5f51f-122">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="5f51f-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="5f51f-123">**詳細ルール** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="5f51f-124">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="5f51f-125">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-125">Select **Create**.</span></span>
9. <span data-ttu-id="5f51f-126">**新しい基準の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="5f51f-127">**適用箇所**フィールドで、主勘定または財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="5f51f-128">**演算子**フィールドで、**is between** や **includes** などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="5f51f-129">**値**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="5f51f-130">**終了日**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="5f51f-131">**追加**を選択してドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f51f-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="5f51f-132">一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="5f51f-133">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-133">Select **Add**.</span></span>
17. <span data-ttu-id="5f51f-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5f51f-134">Close the page.</span></span>
18. <span data-ttu-id="5f51f-135">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f51f-135">Select **Activate**.</span></span>

