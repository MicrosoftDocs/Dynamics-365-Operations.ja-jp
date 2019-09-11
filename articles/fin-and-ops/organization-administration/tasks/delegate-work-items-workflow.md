---
title: ワークフローの作業項目をデリゲート
description: 事務所を不在にする予定がある場合や、作業項目を処理できない場合は、自分の作業項目を他のユーザーに委任 (再割り当て) することができます。
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916418"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="15d09-103">ワークフローの作業項目をデリゲート</span><span class="sxs-lookup"><span data-stu-id="15d09-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="15d09-104">作業項目の手動委任</span><span class="sxs-lookup"><span data-stu-id="15d09-104">Manually delegate a work item</span></span>

<span data-ttu-id="15d09-105">個別の作業項目を委任するには、**ワークフロー**メニューの**委任**オプションを選択し、コメントとともに委任されるユーザーを入力します。</span><span class="sxs-lookup"><span data-stu-id="15d09-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="15d09-106">これにより、作業項目がユーザーに再度割り当てられ、完了させることができます。</span><span class="sxs-lookup"><span data-stu-id="15d09-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="15d09-107">作業項目を自動的に委任</span><span class="sxs-lookup"><span data-stu-id="15d09-107">Automatically delegate work items</span></span>

<span data-ttu-id="15d09-108">不在であることを計画している場合、またはその他の方法で一定期間作業項目に対処できない場合、**ユーザー オプション**ページにて、他のユーザーに新しい作業項目を自動的に委任することができます。</span><span class="sxs-lookup"><span data-stu-id="15d09-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="15d09-109">自動委任の設定</span><span class="sxs-lookup"><span data-stu-id="15d09-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="15d09-110">**共通 > 設定 > ユーザー オプション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="15d09-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="15d09-111">**ワークフロー** タブをクリックします。通知セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="15d09-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="15d09-112">他のユーザーに作業項目を自動的に委任するようにシステムをコンフィギュレーションするには、委任ルールを作成して、特定のタイプの作業項目についてその委任条件を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15d09-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="15d09-113">委任ルールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="15d09-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="15d09-114">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15d09-114">Click **Add**.</span></span>
4. <span data-ttu-id="15d09-115">**スコープ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="15d09-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="15d09-116">[すべて] – 割り当てられているすべての作業項目を委任します。</span><span class="sxs-lookup"><span data-stu-id="15d09-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="15d09-117">[モジュール] – 特定のタイプのワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="15d09-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="15d09-118">このオプションを選択する場合は、[名前] フィールドでワークフローのタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15d09-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="15d09-119">[ワークフロー] – 特定のワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="15d09-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="15d09-120">このオプションを選択する場合は、[名前] フィールドでワークフローを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15d09-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="15d09-121">**デリゲート** フィールドで、作業項目をデリゲートするユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="15d09-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="15d09-122">作業項目をいつ委任するかを指定するためには [開始日時] と [終了日時] フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="15d09-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="15d09-123">**開始日時**フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="15d09-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="15d09-124">**終了日時**フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="15d09-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="15d09-125">**有効**チェック ボックスをオンにして、委任ルールを有効化します。</span><span class="sxs-lookup"><span data-stu-id="15d09-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="15d09-126">**モジュール**を範囲として選択した場合は、名前フィールドでモジュールを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15d09-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="15d09-127">**ワークフロー**を範囲として選択した場合は、特定のワークフローを選択して名前フィールドでデリゲートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="15d09-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="15d09-128">**コメント** フィールドに、作業項目を委任する理由を説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="15d09-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

