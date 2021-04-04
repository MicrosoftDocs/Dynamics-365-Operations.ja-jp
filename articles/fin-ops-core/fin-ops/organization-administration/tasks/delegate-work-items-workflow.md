---
title: ワークフローの作業項目をデリゲート
description: 事務所を不在にする予定がある場合や、作業項目を処理できない場合は、自分の作業項目を他のユーザーに委任 (再割り当て) することができます。
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 054e183374d2b24f38b0f90ff90acfeeca013861
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560558"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="d9d6a-103">ワークフローの作業項目をデリゲート</span><span class="sxs-lookup"><span data-stu-id="d9d6a-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="d9d6a-104">作業項目の手動委任</span><span class="sxs-lookup"><span data-stu-id="d9d6a-104">Manually delegate a work item</span></span>

<span data-ttu-id="d9d6a-105">個別の作業項目を委任するには、**ワークフロー** メニューの **委任** オプションを選択し、コメントとともに委任されるユーザーを入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="d9d6a-106">これにより、作業項目がユーザーに再度割り当てられ、完了させることができます。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="d9d6a-107">複数の作業項目の手動委任</span><span class="sxs-lookup"><span data-stu-id="d9d6a-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="d9d6a-108">複数の作業項目を **自分に割り当てられた作業項目** ページから委任できます。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="d9d6a-109">一括委任の対象となるワークフロー タイプは、購買契約の承認ワークフロー、発注書ワークフロー、購買要求のレビュー、および仕入先請求書のワークフローです。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="d9d6a-110">**複数の作業項目の委任** 機能は既定で無効になっており、**ワークスペース > 機能管理** で有効にできます。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="d9d6a-111">この機能を有効にする方法については、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="d9d6a-112">**共通 > 共通 > 作業項目 > 自分自身に割り当てられた作業項目** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="d9d6a-113">委任する作業項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="d9d6a-114">**作業項目の委任** メニューをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="d9d6a-115">**ユーザー** フィールドで、作業項目を委任するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="d9d6a-116">**コメント** フィールドに、作業項目を委任する理由を説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="d9d6a-117">**作業項目の委任** ボタンをクリックして、作業項目の委任を完了します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="d9d6a-118">作業項目を自動的に委任</span><span class="sxs-lookup"><span data-stu-id="d9d6a-118">Automatically delegate work items</span></span>

<span data-ttu-id="d9d6a-119">不在であることを計画している場合、またはその他の方法で一定期間作業項目に対処できない場合、**ユーザー オプション** ページにて、他のユーザーに新しい作業項目を自動的に委任することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="d9d6a-120">自動委任の設定</span><span class="sxs-lookup"><span data-stu-id="d9d6a-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="d9d6a-121">**共通 > 設定 > ユーザー オプション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="d9d6a-122">**ワークフロー** タブをクリックします。通知セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="d9d6a-123">他のユーザーに作業項目を自動的に委任するようにシステムをコンフィギュレーションするには、委任ルールを作成して、特定のタイプの作業項目についてその委任条件を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="d9d6a-124">委任ルールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="d9d6a-125">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-125">Click **Add**.</span></span>
4. <span data-ttu-id="d9d6a-126">**スコープ** フィールドで、オプションを選択します :</span><span class="sxs-lookup"><span data-stu-id="d9d6a-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="d9d6a-127">[すべて] – 割り当てられているすべての作業項目を委任します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="d9d6a-128">[モジュール] – 特定のタイプのワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="d9d6a-129">このオプションを選択する場合は、**名前** フィールドでワークフローのタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="d9d6a-130">[ワークフロー] – 特定のワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="d9d6a-131">このオプションを選択する場合は、**名前**  フィールドでワークフローを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="d9d6a-132">**名前** フィールドで :</span><span class="sxs-lookup"><span data-stu-id="d9d6a-132">In the **Name** field:</span></span>
    - <span data-ttu-id="d9d6a-133">**モジュール** スコープで、対象のモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="d9d6a-134">**ワークフロー** スコープで、対象のワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="d9d6a-135">**デリゲート** フィールドで、作業項目をデリゲートするユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="d9d6a-136">作業項目が委任されるタイミングを自動的に指定するには、**開始日時** と **終了日時** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="d9d6a-137">**開始日時** フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="d9d6a-138">**終了日時** フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="d9d6a-139">**有効** チェック ボックスをオンにして、委任ルールを有効化します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="d9d6a-140">**コメント** フィールドに、作業項目を委任する理由を説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d6a-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]