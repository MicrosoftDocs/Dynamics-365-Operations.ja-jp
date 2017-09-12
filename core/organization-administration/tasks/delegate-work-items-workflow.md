--- 
title: "ワークフローの作業項目をデリゲート"
description: "事務所を不在にする予定がある場合や、作業項目を処理できない場合は、自分の作業項目を他のユーザーに委任 (再割り当て) することができます。"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6483307ff89ce79a3ef16bb763e3124ac537a5d8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="57ceb-103">ワークフローの作業項目をデリゲート</span><span class="sxs-lookup"><span data-stu-id="57ceb-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57ceb-104">事務所を不在にする予定がある場合や、作業項目を処理できない場合は、自分の作業項目を他のユーザーに委任 (再割り当て) することができます。</span><span class="sxs-lookup"><span data-stu-id="57ceb-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="57ceb-105">この手順により、別のユーザーに作業項目を自動的に委任するシステムの構成が容易になります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="57ceb-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="57ceb-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="57ceb-107">自動委任の設定</span><span class="sxs-lookup"><span data-stu-id="57ceb-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="57ceb-108">[共通] > [設定] > [ユーザー オプション] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="57ceb-109">[ワークフロー] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ceb-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="57ceb-110">[デリゲート] セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="57ceb-111">他のユーザーに作業項目を自動的に委任するようにシステムをコンフィギュレーションするには、委任ルールを作成して、特定のタイプの作業項目についてその委任条件を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="57ceb-112">委任ルールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="57ceb-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="57ceb-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="57ceb-113">Click Add.</span></span>
4. <span data-ttu-id="57ceb-114">[スコープ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="57ceb-115">[すべて] – 割り当てられているすべての作業項目を委任します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="57ceb-116">[モジュール] – 特定のタイプのワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="57ceb-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="57ceb-117">このオプションを選択する場合は、[名前] フィールドでワークフローのタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="57ceb-118">[ワークフロー] – 特定のワークフローに関連する作業項目のみをデリゲートします。</span><span class="sxs-lookup"><span data-stu-id="57ceb-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="57ceb-119">このオプションを選択する場合は、[名前] フィールドでワークフローを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="57ceb-120">[デリゲート] フィールドで、作業項目をデリゲートするユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="57ceb-121">作業項目をいつ委任するかを指定するためには [開始日時] と [終了日時] フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="57ceb-122">[開始日時] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="57ceb-123">[終了日時] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="57ceb-124">[有効] チェック ボックスをオンにして、委任ルールを有効化します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="57ceb-125">モジュールを範囲として選択した場合は、[名前] フィールドでモジュールを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="57ceb-126">ワークフローを範囲として選択した場合は、特定のワークフローを選択して [名前] フィールドでデリゲートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57ceb-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="57ceb-127">[コメント] フィールドに、作業項目を委任する理由を説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="57ceb-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


