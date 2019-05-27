---
title: セルフサービス配置で配置された環境のトラブルシューティング
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の問題をトラブルシューティングおよび診断する方法について説明します。
author: manado
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 2f086e97f95f08c14cc439256bd1458fc9dc8298
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537060"
---
# <a name="troubleshoot-environments-deployed-through-self-service-deployment"></a><span data-ttu-id="0d047-103">セルフサービス配置で配置された環境のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="0d047-103">Troubleshoot environments deployed through self-service deployment</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="0d047-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境の問題をトラブルシューティングする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d047-104">This topic explains how you can troubleshoot issues on an environment that was deployed using the [self-service deployment](infrastructure-stack.md) experience.</span></span> <span data-ttu-id="0d047-105">ユーザーが問題を報告したとき、トラブルシューティングのために Lifecycle Services (LCS) にあるさまざまなツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d047-105">When a user reports an issue, you can use various tools in Lifecycle Services (LCS) for troubleshooting.</span></span> <span data-ttu-id="0d047-106">豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0d047-106">The rich set of telemetry data helps you build a storyboard view that shows what that user and other users were doing when the issue was reported.</span></span>

<span data-ttu-id="0d047-107">**環境監視** ダッシュボードを開くには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0d047-107">To open the **Environment Monitoring** dashboard, follow the steps listed below:</span></span>

1. <span data-ttu-id="0d047-108">LCS を開き、適切なプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="0d047-108">Open LCS and navigate to the appropriate project.</span></span>
2. <span data-ttu-id="0d047-109">**環境**セクションで、表示する環境を選択してから**完全な詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d047-109">In the **Environments** section, select the environment that you want to view, and then click **Full details**.</span></span>
3. <span data-ttu-id="0d047-110">**環境の詳細**ページで、**環境の監視**をクリックして、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d047-110">On the **Environment details** page, click **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span>

<span data-ttu-id="0d047-111">環境監視ダッシュボードに、**概要**および**活動**の 2 つのタブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-111">On the Environment Monitoring dashboard, you will see two tabs: **Overview** and **Activity**.</span></span>

<span data-ttu-id="0d047-112">[![問題を解決する](./media/DiagnoseIssues.jpg)](./media/DiagnoseIssues.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d047-112">[![Diagnose Issues](./media/DiagnoseIssues.jpg)](./media/DiagnoseIssues.jpg)</span></span>

## <a name="overview-tab"></a><span data-ttu-id="0d047-113">[概要] タブ</span><span class="sxs-lookup"><span data-stu-id="0d047-113">Overview tab</span></span>

<span data-ttu-id="0d047-114">**概要** タブには、特定の期間に環境がどのように使用されたかを表すストーリーボード ビューが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-114">The **Overview** tab provides a storyboard view that shows how the environment was being used during a specific period.</span></span> <span data-ttu-id="0d047-115">情報ログを絞り込むには、このページで、フィルターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d047-115">You can use the filters on this page to narrow the information logs.</span></span> <span data-ttu-id="0d047-116">利用可能なフィルタを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0d047-116">Here are some of the filters that are available:</span></span>

  - <span data-ttu-id="0d047-117">**期間**: 選択した日時から 60 分前に戻ります。</span><span class="sxs-lookup"><span data-stu-id="0d047-117">**Time duration**: Go back 60 minutes from the selected date and time.</span></span>
  - <span data-ttu-id="0d047-118">**ユーザー**: 特定のユーザーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="0d047-118">**User**: View a specific user's activities.</span></span>
  - <span data-ttu-id="0d047-119">**検索用語**: 調査中の問題に基づいて検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="0d047-119">**Search terms**: Create a search that is based on the issue that is being investigated.</span></span>

<span data-ttu-id="0d047-120">さらに、2 つのセクションも表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-120">In addition, you will also see two sections:</span></span>

  - <span data-ttu-id="0d047-121">**ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。</span><span class="sxs-lookup"><span data-stu-id="0d047-121">The **User interaction** chart shows a user's activities on various machines in the environment and the SQL utilization trend.</span></span>
  - <span data-ttu-id="0d047-122">**ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-122">The **User activity** grid shows the various activities that users performed, based on their session timestamp.</span></span> <span data-ttu-id="0d047-123">有効なセッションは、グリッドの左側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-123">The active sessions display on the left side of the grid.</span></span> <span data-ttu-id="0d047-124">セッションごとに、Form:Control:Command と、アクションが実行されたときの対応するタイムスタンプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-124">For each session, the Form:Control:Command and the corresponding timestamp show when the action was taken.</span></span> <span data-ttu-id="0d047-125">ユーザーがこのグリッドに表示される情報を実行した正確な手順を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="0d047-125">You can trace the exact steps that the user was taking in the information presented in this grid.</span></span>
  
 > [!IMPORTANT]
 > <span data-ttu-id="0d047-126">[概要] タブには、診断を支援する CPU とメモリの稼働状態メトリックも含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d047-126">The Overview tab will also include the CPU and memory health metrics to help with diagnostics.</span></span>  <span data-ttu-id="0d047-127">この機能は、現在は使用できませんが、すぐに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-127">This feature is currently not available but will be added soon.</span></span> 

## <a name="activity-tab"></a><span data-ttu-id="0d047-128">活動タブ</span><span class="sxs-lookup"><span data-stu-id="0d047-128">Activity tab</span></span>

<span data-ttu-id="0d047-129">**活動** タブには、高度なトラブルシューティングの事前に定義された一連のクエリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-129">The **Activity** tab shows a predefined set of queries for advanced troubleshooting.</span></span> <span data-ttu-id="0d047-130">これにより、生の情報ログにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d047-130">This gives you access to the raw information logs.</span></span> <span data-ttu-id="0d047-131">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d047-131">You can then export the logs to do more advanced analysis.</span></span> <span data-ttu-id="0d047-132">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d047-132">The following types of queries are available:</span></span>

  - <span data-ttu-id="0d047-133">ユーザー関連のエラー</span><span class="sxs-lookup"><span data-stu-id="0d047-133">User-related errors</span></span>
  - <span data-ttu-id="0d047-134">速度の遅いクエリ</span><span class="sxs-lookup"><span data-stu-id="0d047-134">Slow queries</span></span>
  - <span data-ttu-id="0d047-135">デッドロック</span><span class="sxs-lookup"><span data-stu-id="0d047-135">Deadlocks</span></span>
  - <span data-ttu-id="0d047-136">クラッシュ</span><span class="sxs-lookup"><span data-stu-id="0d047-136">Crashes</span></span>

> [!NOTE]
> <span data-ttu-id="0d047-137">**概要**および**活動**タブに表示されるデータは、30 日間だけ保持されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-137">The data shown on the **Overview** and **Activity** tabs is only retained for 30 days.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d047-138">環境監視には、パフォーマンスの問題を診断および軽減するための高度な SQL トラブルシューティングのツールも含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d047-138">The Environment monitoring will also include advanced SQL troubleshooting tools to diagnose and mitigate performance issues.</span></span> <span data-ttu-id="0d047-139">この機能は、現在は使用できませんが、すぐに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0d047-139">This feature is currently not available but will be added soon.</span></span> 


