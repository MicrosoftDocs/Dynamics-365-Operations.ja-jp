---
title: "要員管理の概要"
description: "このトピックでは、店舗マネージャーが要員を容易に管理できるように、よく知られた管理販売時点管理 (POS) クライアント、Modern POS、クラウド POSを活用して要員管理 (WFM) サービスをどのように使用するかを説明しています。"
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a><span data-ttu-id="abf79-103">要員管理の概要</span><span class="sxs-lookup"><span data-stu-id="abf79-103">Workforce management overview</span></span>

[!include[banner](includes/banner.md)]
    
<span data-ttu-id="abf79-104">店舗マネージャーが要員を容易に管理できるように、よく知られた管理販売時点管理 (POS) クライアント、Modern POS、クラウド POSを活用して要員管理 (WFM) サービスを活用します。</span><span class="sxs-lookup"><span data-stu-id="abf79-104">The Workforce management (WFM) service takes advantage of the familiar point of sale (POS) clients, Modern POS and Cloud POS, to let store managers easily manage their workforce.</span></span> <span data-ttu-id="abf79-105">ワイヤ フレーム サービスは POS に関連するパッケージをダウンロードするために、拡張フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="abf79-105">The WFM service uses the extension framework to download the relevant packages in the POS.</span></span> <span data-ttu-id="abf79-106">POSを終了し、再オープンする際にそれらのパッケージがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="abf79-106">These packages are downloaded when the POS is closed and reopened.</span></span> <span data-ttu-id="abf79-107">したがって、Microsoft からのワイヤ フレームの新機能のリリース時に、POSのアプリケーションを終了し、再オープンしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="abf79-107">Therefore, when Microsoft releases new features for WFM, the POS app must be closed and reopened.</span></span>

<span data-ttu-id="abf79-108">このサービスを使用すると、店舗マネージャーは店舗の週ごとの勤務スケジュールの作成および公開が簡単に行えます。</span><span class="sxs-lookup"><span data-stu-id="abf79-108">By using this service, store managers can easily create and publish weekly work schedule for their stores.</span></span> <span data-ttu-id="abf79-109">店舗の作業者は自分と同僚のスケジュールをすばやく表示することができます。</span><span class="sxs-lookup"><span data-stu-id="abf79-109">Store workers can then quickly view their own schedules and the schedules of their colleagues.</span></span> <span data-ttu-id="abf79-110">この方法で、割り当てられたシフトで誰と働くかがわかります。</span><span class="sxs-lookup"><span data-stu-id="abf79-110">In that way, they can learn who will be working with them during the assigned shifts.</span></span> <span data-ttu-id="abf79-111">店舗の作業者は、休暇、同僚とのシフト交換、シフト提示の要求も作成できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-111">Store workers can also create requests for absence, shift swap, and shift offer.</span></span> <span data-ttu-id="abf79-112">これらすべての要求は定義されたワークフローをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="abf79-112">All these requests trigger a defined workflow.</span></span>

<span data-ttu-id="abf79-113">シフト中に、店舗の作業者は POS クライアントに組み込まれている出勤と退勤の機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-113">During a shift, store workers can take advantage of the clock-in and clock-out feature that is built into the POS clients.</span></span> <span data-ttu-id="abf79-114">給与処理のため、データは本社 (HQ) に送信されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-114">The data is then sent to the headquarters (HQ) for payroll processing.</span></span> <span data-ttu-id="abf79-115">出勤と退勤の機能は、POSの既存の機能です。</span><span class="sxs-lookup"><span data-stu-id="abf79-115">The clock-in and clock-out feature is an existing capability of the POS.</span></span> <span data-ttu-id="abf79-116">設定およびサポートされているシナリオの詳細については、[出勤および退勤](retail-time-attendance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abf79-116">For more information about the setup and supported scenarios, see [Clock in and clock out](retail-time-attendance.md).</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="abf79-117">サポートされているシナリオ</span><span class="sxs-lookup"><span data-stu-id="abf79-117">Supported scenarios</span></span>
<span data-ttu-id="abf79-118">このセクションでは、サポートされるシナリオの詳細を取り上げます。</span><span class="sxs-lookup"><span data-stu-id="abf79-118">This section provides more information about the supported scenarios.</span></span>

- <span data-ttu-id="abf79-119">**スケジュールの作成および公開** – ワイヤ フレーム サービスは、作業者が店舗マネージャー特権を持つかどうかを決定するために HQ でコンフィギュレーションされている POS のアクセス許可を使用します。</span><span class="sxs-lookup"><span data-stu-id="abf79-119">**Create and publish schedules** – The WFM service uses the POS permissions that are configured in the HQ to determine whether a worker has store manager privileges.</span></span> <span data-ttu-id="abf79-120">店舗マネージャーのみ、スケジュール管理オペレーションを使用してスケジュールを作成、公開できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-120">Only store managers can create and publish schedules by using the Schedule management operation.</span></span> <span data-ttu-id="abf79-121">1 人の作業者から別の作業者へ既存の作業シフトをコピー アンド ペーストすることによりスケジュールをすばやく作成できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-121">They can quickly create a schedule by copying and pasting an existing work shift from one worker to another worker.</span></span> <span data-ttu-id="abf79-122">先週のスケジュールから今週のスケジュールにインポートすることによってもスケジュールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-122">They can also create a schedule by importing the schedule from any previous week to the current week.</span></span>

    <span data-ttu-id="abf79-123">スケジュールが公開されていない場合、スケジュールはドラフト状態にあり、公開されたスケジュールとは異なる状態にあります。</span><span class="sxs-lookup"><span data-stu-id="abf79-123">If a schedule isn't published, it's in a draft state and looks different than a published schedule.</span></span> <span data-ttu-id="abf79-124">店舗のマネージャーは任意の週の [**公開**] ボタンをクリックしてスケジュールを公開することができます。</span><span class="sxs-lookup"><span data-stu-id="abf79-124">Store managers can publish a schedule by clicking the **Publish** button for any week.</span></span> <span data-ttu-id="abf79-125">1週間のスケジュールが公開されると、加えられる変更は自動的に公開されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-125">After the schedule is published for a week, any changes are automatically published.</span></span> <span data-ttu-id="abf79-126">変更例として、勤務シフトまたは休暇の追加や削除、また勤務シフトまたは休暇の編集があります。</span><span class="sxs-lookup"><span data-stu-id="abf79-126">Examples of changes include the addition or deletion of work shifts or absences, or edits to work shifts or absences.</span></span> <span data-ttu-id="abf79-127">店舗の作業者は、各週に対して公開されたスケジュールのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-127">Store workers can view only schedules that have been published for various weeks.</span></span>
    
- <span data-ttu-id="abf79-128">**要求の作成および承認** – 店舗の作業者は 3 つのタイプの要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-128">**Create and approve requests** – Store workers can create three types of request:</span></span>

    - <span data-ttu-id="abf79-129">休暇要求</span><span class="sxs-lookup"><span data-stu-id="abf79-129">Request absence</span></span>
    - <span data-ttu-id="abf79-130">シフト交換の要求</span><span class="sxs-lookup"><span data-stu-id="abf79-130">Request shift swap</span></span>
    - <span data-ttu-id="abf79-131">シフト提示の要求</span><span class="sxs-lookup"><span data-stu-id="abf79-131">Request shift offer</span></span>

    <span data-ttu-id="abf79-132">スケジュール要求の工程を使用して、これらの要求を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="abf79-132">These requests can be created by using the Schedule requests operation.</span></span> <span data-ttu-id="abf79-133">各要求は定義されているワークフローに従い、作業者は各自の要求の現在の状態を簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="abf79-133">Each request follows a defined workflow, and workers can easily see the current status of their requests.</span></span>
    
    <span data-ttu-id="abf79-134">休暇要求は、承認のために店舗マネージャーに自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-134">Absence requests are automatically sent to the store manager for approval.</span></span> <span data-ttu-id="abf79-135">店舗マネージャーが複数の場合は、すべてのマネージャーが要求を見ることができますが、ひとりのマネージャーのみが承認と拒否を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="abf79-135">If there are multiple store managers, all managers can view a given request, but only one manager can approve or reject it.</span></span> <span data-ttu-id="abf79-136">**小売**モジュールの [**休暇のタイプ**] ページを使用して Retail HQ で休暇のタイプがコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="abf79-136">The absence types are configured in the retail HQ by using the **Leave and absence types** page in the **Retail** module.</span></span> <span data-ttu-id="abf79-137">店舗のマネージャーが要求を承認または拒否した後、その要求はスケジュール要求の工程の [**履歴**] タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="abf79-137">After the store manager approves or rejects a request, it's moved to the **History** tab for the Schedule requests operation.</span></span>
    
    <span data-ttu-id="abf79-138">シフト交換やシフト提示の要求は、要求が送信された作業者に最初に送られます。</span><span class="sxs-lookup"><span data-stu-id="abf79-138">A shift swap or shift offer request first goes to the worker that the request was sent to.</span></span> <span data-ttu-id="abf79-139">この作業者が承認した後にのみ、店舗のマネージャーは要求を表示できます。</span><span class="sxs-lookup"><span data-stu-id="abf79-139">The store manager can view the request only after this worker has approved it.</span></span> <span data-ttu-id="abf79-140">したがって、作業者がシフト交換やシフト提示の要求を拒否した場合、マネージャーはその要求を表示できません。</span><span class="sxs-lookup"><span data-stu-id="abf79-140">Therefore, if the worker rejects the shift swap or shift offer request, the manager can't view it.</span></span> <span data-ttu-id="abf79-141">要求を作成した作業者も、マネージャーがその要求を承認または拒否する前にキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="abf79-141">The worker who created the request can also cancel it before the manager approves or denies it.</span></span>

- <span data-ttu-id="abf79-142">**スケジュール ビューで有効な店舗の作業者の表示** – 例えば、作業者を店舗の従業員アドレス帳に関連付けることによって、作業者が店舗に追加された時、ワイヤ フレーム サービスでスケジューリングが可能になります。</span><span class="sxs-lookup"><span data-stu-id="abf79-142">**Show the active store workers in the schedule view** – When a worker is added to a store by, for example, associating him or her with the store's employee address book, the worker becomes available for scheduling in the WFM service.</span></span> <span data-ttu-id="abf79-143">**要員管理のプロセス ワーカー データ**と呼ばれる定期的なバッチ ジョブが HQ で実行されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-143">A recurring batch job that is named **Process worker data for workforce management** is run in the HQ.</span></span> <span data-ttu-id="abf79-144">このジョブは、Common Data Service (CDS) に送信される店舗作業者アソシエーションを準備します。</span><span class="sxs-lookup"><span data-stu-id="abf79-144">This job prepares the store-worker associations that will be sent to the Common Data Service (CDS).</span></span>

    <span data-ttu-id="abf79-145">店舗から作業者が削除されるとき、同じプロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-145">The same process is used when a worker is removed from a store.</span></span> <span data-ttu-id="abf79-146">ただし、削除された作業者に有効な作業シフトもしくは休暇が割り当てられている場合、その作業者は、過去、現在、そして今後の週にも引き続き表示されます。</span><span class="sxs-lookup"><span data-stu-id="abf79-146">However, the worker who is removed is still shown for past, current, and future weeks if an active work shift or absence is assigned to that worker.</span></span> <span data-ttu-id="abf79-147">したがって、これらの作業シフトと休暇が削除されない限り、削除された作業者は引き続きこれらの週に表示され続けます。</span><span class="sxs-lookup"><span data-stu-id="abf79-147">Therefore, unless these work shifts and absences are deleted, the removed worker will continue to be shown for these weeks.</span></span>

