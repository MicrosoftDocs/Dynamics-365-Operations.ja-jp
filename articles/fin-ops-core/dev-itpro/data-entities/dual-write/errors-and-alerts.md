---
title: エラー管理と警告通知
description: このトピックでは、問題のトラブルシューティングに役立つエラー ログと警告通知について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1c77f6b26f98ddfb35b97fbb17e9966a28d958a
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279119"
---
# <a name="error-management-and-alert-notifications"></a><span data-ttu-id="1f9bb-103">エラー管理と警告通知</span><span class="sxs-lookup"><span data-stu-id="1f9bb-103">Error management and alert notifications</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1f9bb-104">Microsoft は、エラーに強い二重書き込みを実現するために、多くの時間と労力を費やしてきました。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-104">Microsoft has invested lots of time and effort into making dual-write resilient to errors.</span></span> <span data-ttu-id="1f9bb-105">ただし、二重書き込み用のエンティティ マップを有効にしている間または後に、問題が発生した場合は、特定のエンティティ マップを選択して、それらのすべてのアクティビティとエラーの統合ビューを取得できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-105">However, if you encounter an issue while or after you enable entity maps for dual-write, you can select specific entity maps to get a consolidated view of all the activities and errors for them.</span></span> <span data-ttu-id="1f9bb-106">この統合ビューには、エラー ログが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-106">This consolidated view includes error logs.</span></span> <span data-ttu-id="1f9bb-107">目標は、エンティティ マップのアクティビティの単一ビューを提供することにより、トラブルシューティング中に支援することです。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-107">The goal is to help you during troubleshooting by providing a single view of the activities for an entity map.</span></span>

## <a name="consolidated-error-management"></a><span data-ttu-id="1f9bb-108">統合されたエラー管理</span><span class="sxs-lookup"><span data-stu-id="1f9bb-108">Consolidated error management</span></span>

<span data-ttu-id="1f9bb-109">アクティビティ ログは、特定のエンティティ マップが **実行していません** 状態から **実行中** 状態に移行するイベントの時系列一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-109">The activity log provides a chronological list of events that a specific entity map goes through from the **Not Running** status to the **Running** status.</span></span> <span data-ttu-id="1f9bb-110">たとえば、一覧には、作成されたマッピング、フィールド マッピングの更新、実行されたマッピングを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-110">For example, the list can include mappings that are created, updates of field mappings, and mappings that are run.</span></span> <span data-ttu-id="1f9bb-111">さらに、エラーが発生した場合は、ログをダウンロードして、次のレベルの詳細を取得できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-111">Additionally, if errors occur, you can download the logs to get the next level of details.</span></span>

![アクティビティ ログの表示](media/activity-log.png)

<span data-ttu-id="1f9bb-113">Finance and Operations アプリ と Common Data Service の間で既存のデータをコピーしているときに問題が発生した場合、**初回同期の詳細** タブにエラー数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-113">If you encounter issues while you copy pre-existing data between Finance and Operations apps and Common Data Service, the **Initial sync details** tab provides a count of the errors.</span></span> <span data-ttu-id="1f9bb-114">また、原因となっているエラーを修正した後、実行を再実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-114">It also lets you rerun the execution after you fix the underlying errors.</span></span>

![エラーの修正と再実行](media/fix-error-rerun.png)

<span data-ttu-id="1f9bb-116">さらにドリル ダウンして、エラーが発生した同期の方向を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-116">You can drill down further to view the synchronization direction where the error occurred.</span></span> <span data-ttu-id="1f9bb-117">この情報は、トラブルシューティングの範囲を絞り込むのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-117">This information can help you narrow down the scope for troubleshooting.</span></span>

![同期方向エラーの表示](media/sync-direction-error.png)

<span data-ttu-id="1f9bb-119">同様に、**キャッチ アップ エラー** タブは、一時停止状態から再開したときの問題のトラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-119">In a similar way, the **Catch-up errors** tab can help you troubleshoot issues when you resume from a paused state.</span></span>

## <a name="alert-notifications"></a><span data-ttu-id="1f9bb-120">警告の通知</span><span class="sxs-lookup"><span data-stu-id="1f9bb-120">Alert notifications</span></span>

<span data-ttu-id="1f9bb-121">管理者は、1 つ以上の警告設定を作成して、計画的または計画外のメンテナンスのケースを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-121">As an admin, you can create one or more alert settings to handle cases of planned or unplanned maintenance.</span></span> <span data-ttu-id="1f9bb-122">たとえば、ネットワーク エラーなどが原因で特定のエラーしきい値に達した場合に、電子メールで通知するように、二重書き込みシステムを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-122">For example, you can set up the dual-write system to notify you by email if a specific error threshold is reached because of, for example, network errors.</span></span> <span data-ttu-id="1f9bb-123">二重書き込みシステムは、ユーザーの代わりにアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-123">The dual-write system can also take action on your behalf.</span></span> <span data-ttu-id="1f9bb-124">たとえば、二重書き込みを一時停止または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-124">For example, it can pause or stop dual-write.</span></span>

<span data-ttu-id="1f9bb-125">次の図は、**アプリケーション エラー** タイプのエラーが 15 分以内に 10 回発生した場合に、二重書き込みが一時停止する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-125">The following illustration shows an example where dual-write will be paused if 10 errors of the **Application error** type occur within 15 minutes.</span></span>

![1 つ以上の警告設定の作成](media/create-alert-settings.png)

<span data-ttu-id="1f9bb-127">**警告設定の作成** を選択することにより、追加の警告を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-127">By selecting **Create alert settings**, you can create more alerts.</span></span> <span data-ttu-id="1f9bb-128">また、個人またはグループのどちらに通知を送信するかを選択したり、二重書き込みシステムがユーザーに代わりにアクションを実行するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-128">You can also select whether notifications should be sent to an individual or a group, and whether the dual-write system should take any action on your behalf.</span></span>

![警告の作成と通知の送信](media/create-alert-notification.png)

<span data-ttu-id="1f9bb-130">この機能は、計画外のメンテナンスがある場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-130">This feature is especially useful if there is unplanned maintenance.</span></span> <span data-ttu-id="1f9bb-131">たとえば、アプリの 1 つが使用できなくなり、定義したしきい値に基づいて、二重書き込みが一時停止状態になり、すべての新しい要求がキューに入れられるます (つまり、それらは失われません)。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-131">For example, one of the apps becomes unavailable and, based on your defined thresholds, dual-write goes into a paused state where all new requests are queued (that is, they aren't lost).</span></span> <span data-ttu-id="1f9bb-132">基になる問題を修正し、両方のアプリが正常に実行されたら、一時停止状態から再開できます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-132">After you fix the underlying issue, and both apps are running smoothly, you can resume from the paused state.</span></span> <span data-ttu-id="1f9bb-133">更新はキューから読み戻され、復元されたアプリに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="1f9bb-133">The updates will then be read back from the queue and written to the recovered app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1f9bb-134">次のステップ</span><span class="sxs-lookup"><span data-stu-id="1f9bb-134">Next steps</span></span>

[<span data-ttu-id="1f9bb-135">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="1f9bb-135">Application lifecycle management</span></span>](app-lifecycle-management.md)
