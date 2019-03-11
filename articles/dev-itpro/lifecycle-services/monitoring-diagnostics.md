---
title: Lifecycle Services (LCS) の監視および診断ツール
description: このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。
author: manalidongre
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 581c671afd275b61c9b20f668429f445e700241d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368361"
---
# <a name="monitoring-and-diagnostics-tools-in-lifecycle-services-lcs"></a><span data-ttu-id="a7950-103">Lifecycle Services (LCS) の監視および診断ツール</span><span class="sxs-lookup"><span data-stu-id="a7950-103">Monitoring and diagnostics tools in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7950-104">このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a7950-104">This topic describes the various tools that Microsoft Dynamics Lifecycle Services (LCS) provides to help you monitor, diagnose, and analyze the health of the Microsoft Dynamics 365 for Finance and Operations environments that you manage.</span></span>

<span data-ttu-id="a7950-105">Microsoft Dynamics 365 for Finance and Operations のクラウド サービスへのオンボード エクスペリエンスを成功させるには、環境の状態を常に把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-105">To have a successful onboarding experience to the cloud service for Microsoft Dynamics 365 for Finance and Operations, you must know the health of your environments at all times.</span></span> <span data-ttu-id="a7950-106">発生するすべての正常性の問題をトラブルシューティングできることも必要です。</span><span class="sxs-lookup"><span data-stu-id="a7950-106">You must also be able to troubleshoot any health issues that occur.</span></span> <span data-ttu-id="a7950-107">Dynamics 365 for Finance and Operations の管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a7950-107">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center for Dynamics 365 for Finance and Operations, contains a collection of monitoring and diagnostics tools that can help to ensure that you have an accurate view of the environments that you manage.</span></span>

## <a name="telemetry-data"></a><span data-ttu-id="a7950-108">テレメトリ データ</span><span class="sxs-lookup"><span data-stu-id="a7950-108">Telemetry data</span></span>
<span data-ttu-id="a7950-109">LCS の監視および診断ポータルの基礎となるテレメトリ データには、監視、診断、分析の 3 つの主要なユース ケースがあります。</span><span class="sxs-lookup"><span data-stu-id="a7950-109">The telemetry data that is the basis of the Monitoring and diagnostics portal in LCS has three primary use cases: monitoring, diagnostics, and analytics.</span></span> <span data-ttu-id="a7950-110">[![monitoringanddiagnostics01](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span><span class="sxs-lookup"><span data-stu-id="a7950-110">[![monitoringanddiagnostics01](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span></span>

### <a name="monitoring"></a><span data-ttu-id="a7950-111">監視</span><span class="sxs-lookup"><span data-stu-id="a7950-111">Monitoring</span></span>

<span data-ttu-id="a7950-112">業務運営ソフトウェアでは、環境が立ち上がっており実行中であるかどうか常に把握して、業務運営を実行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-112">In business operations software, you should always know whether your environment is up and running, so that it can perform business operations.</span></span> <span data-ttu-id="a7950-113">LCS を通じて環境の稼働状態を簡単に表示できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-113">You should also be able to easily view the health of the environment through LCS.</span></span> <span data-ttu-id="a7950-114">Microsoft は、2 種類の監視機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a7950-114">Microsoft supports two types of monitoring capabilities:</span></span>

-   <span data-ttu-id="a7950-115">**可用性の監視** - このタイプの監視は、いつでも利用可能であることを確認するため、環境に対してチェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="a7950-115">**Availability monitoring** – This type of monitoring performs a check against the environment to make sure that it's available at all times.</span></span> <span data-ttu-id="a7950-116">チェックが失敗した場合、Microsoft サービス エンジニアリング チームにすぐに通知されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-116">If the check fails, the Microsoft Service Engineering team is immediately notified.</span></span>
-   <span data-ttu-id="a7950-117">**稼働状態の監視** – 可用性チェックに加えて、基本的な正常性チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-117">**Health monitoring** – In addition to availability checks, some basic health checks must be performed.</span></span> <span data-ttu-id="a7950-118">これらの基本的な正常性チェックには、CPU レベル、コンピューターのメモリ消費量、および 5 分間の合計デッドロック数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a7950-118">These basic health checks include CPU level, memory consumption of the machines, and the total number of deadlocks in a five-minute period.</span></span> <span data-ttu-id="a7950-119">Microsoft テレメトリ インフラストラクチャは、環境から多くの正常性指標を収集します。</span><span class="sxs-lookup"><span data-stu-id="a7950-119">Microsoft Telemetry Infrastructure collects lots of health metrics from the environments.</span></span> <span data-ttu-id="a7950-120">メトリックがしきい値を超えている場合は、Microsoft サービス エンジニアリング チームに警告が表示され、問題を調査できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-120">If a metric crosses a threshold value, the Microsoft Service Engineering term is alerted so that it can investigate the issue.</span></span>

### <a name="diagnostics"></a><span data-ttu-id="a7950-121">診断</span><span class="sxs-lookup"><span data-stu-id="a7950-121">Diagnostics</span></span>

<span data-ttu-id="a7950-122">ユーザーが問題を報告したとき、トラブルシューティングのために LCS にあるさまざまなツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-122">When a user reports an issue, you can use various tools in LCS for troubleshooting.</span></span> <span data-ttu-id="a7950-123">豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a7950-123">The rich set of telemetry data helps you build a storyboard view that shows what that user and other users were doing when the issue was reported.</span></span> <span data-ttu-id="a7950-124">ユーザーのアクティビティ追跡に加えて、豊富な SQL データがパフォーマンスのトラブルシューティングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-124">In addition to user activity tracking, a rich set of SQL data is available for performance troubleshooting.</span></span>

### <a name="analytics"></a><span data-ttu-id="a7950-125">分析</span><span class="sxs-lookup"><span data-stu-id="a7950-125">Analytics</span></span>

<span data-ttu-id="a7950-126">分析は収集されるテレメトリ データの別の重要なユース ケースです。</span><span class="sxs-lookup"><span data-stu-id="a7950-126">Analytics is another critical use case for the telemetry data that is collected.</span></span> <span data-ttu-id="a7950-127">現在のところ、Microsoft だけが分析を実行できるため、Microsoft Power BI を使用して機能の使用状況とパフォーマンスを測定し理解することができます。</span><span class="sxs-lookup"><span data-stu-id="a7950-127">Currently, only Microsoft can perform analytics, so that it can gauge and understand feature usage and performance through Microsoft Power BI.</span></span>

## <a name="responsibilities"></a><span data-ttu-id="a7950-128">職責</span><span class="sxs-lookup"><span data-stu-id="a7950-128">Responsibilities</span></span>
<span data-ttu-id="a7950-129">Dynamics 365 for Finance and Operations などの管理されたクラウド サービスについては、Microsoft は常に実稼動環境の正常性をアクティブに監視する責任があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-129">For a managed cloud service such as Dynamics 365 for Finance and Operations, Microsoft is responsible for actively monitoring the health of production environments at all times.</span></span> <span data-ttu-id="a7950-130">顧客の環境が問題によって影響を受ける場合、Microsoft サービス エンジニア リング チームにすぐに警告が通知されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-130">If a customer's environment is affected by an issue, the Microsoft Service Engineering team is immediately alerted.</span></span> <span data-ttu-id="a7950-131">チームは問題の調査を開始し、解決策を見つけるために協力します。</span><span class="sxs-lookup"><span data-stu-id="a7950-131">The team will start to investigate the issue and will work with you to find a resolution.</span></span> <span data-ttu-id="a7950-132">ただし、非実稼働環境の状態を事前または反応的に監視およびトラブルシューティングする責任はお客様にあります。</span><span class="sxs-lookup"><span data-stu-id="a7950-132">However, you're responsible for proactively or reactively monitoring and troubleshooting the health of non-production environments.</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="a7950-133">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a7950-133">Access the Monitoring and diagnostics portal</span></span>
1.  <span data-ttu-id="a7950-134">LCS を開き、適切なプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="a7950-134">Open LCS, and navigate to the appropriate project.</span></span>
2.  <span data-ttu-id="a7950-135">**環境** セクションで、表示する**環境**を選択してから **完全な詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7950-135">In the **Environments** section, select the **environment** to view, and then click **Full details**.</span></span>
3.  <span data-ttu-id="a7950-136">**環境の詳細**ページで、**環境の監視**をクリックして、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7950-136">On the **Environment details** page, click **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> <span data-ttu-id="a7950-137">[![howtogettoenvmonitoring](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span><span class="sxs-lookup"><span data-stu-id="a7950-137">[![howtogettoenvmonitoring](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span></span>

## <a name="tools"></a><span data-ttu-id="a7950-138">ツール</span><span class="sxs-lookup"><span data-stu-id="a7950-138">Tools</span></span>
<span data-ttu-id="a7950-139">複数のツールとリソースが、監視および診断ポータルで利用できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-139">Several tools and resources are available in the Monitoring and diagnostics portal.</span></span> 

> [!NOTE]
> <span data-ttu-id="a7950-140">すべての環境に、すべてのツールが含まれるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a7950-140">Not all environments contain all the tools.</span></span> <span data-ttu-id="a7950-141">次のテーブルに、各タイプの環境で使用できるツールを示します。</span><span class="sxs-lookup"><span data-stu-id="a7950-141">The following table shows the tools that are available for each type of environment.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7950-142">環境タイプ</span><span class="sxs-lookup"><span data-stu-id="a7950-142">Environment type</span></span></th>
<th><span data-ttu-id="a7950-143">ツール</span><span class="sxs-lookup"><span data-stu-id="a7950-143">Tools</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7950-144">生産システム</span><span class="sxs-lookup"><span data-stu-id="a7950-144">Production systems</span></span></td>
<td><ul>
<li><span data-ttu-id="a7950-145">活動の監視</span><span class="sxs-lookup"><span data-stu-id="a7950-145">Activity monitoring</span></span></li>
<li><span data-ttu-id="a7950-146">環境の監視</span><span class="sxs-lookup"><span data-stu-id="a7950-146">Environment monitoring</span></span></li>
<li><span data-ttu-id="a7950-147">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="a7950-147">SQL insights</span></span></li>
<li><span data-ttu-id="a7950-148">システム診断</span><span class="sxs-lookup"><span data-stu-id="a7950-148">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7950-149">ユーザー受け入れテスト (UAT)/サンドボックス</span><span class="sxs-lookup"><span data-stu-id="a7950-149">User acceptance testing (UAT)/sandbox</span></span></td>
<td><ul>
<li><span data-ttu-id="a7950-150">活動の監視</span><span class="sxs-lookup"><span data-stu-id="a7950-150">Activity monitoring</span></span></li>
<li><span data-ttu-id="a7950-151">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="a7950-151">SQL insights</span></span></li>
<li><span data-ttu-id="a7950-152">システム診断</span><span class="sxs-lookup"><span data-stu-id="a7950-152">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7950-153">デモ/ビルド</span><span class="sxs-lookup"><span data-stu-id="a7950-153">Demo/build</span></span></td>
<td><ul>
<li><span data-ttu-id="a7950-154">活動の監視</span><span class="sxs-lookup"><span data-stu-id="a7950-154">Activity monitoring</span></span></li>
<li><span data-ttu-id="a7950-155">システム診断</span><span class="sxs-lookup"><span data-stu-id="a7950-155">System diagnostics</span></span></li>
</ul></td>
</tr>
 <tr class="even">
<td><span data-ttu-id="a7950-156">顧客/パートナー サブスクリプションに配置される環境</span><span class="sxs-lookup"><span data-stu-id="a7950-156">Environments deployed in customer/partner subscriptions</span></span></td>
<td><ul>
<li><span data-ttu-id="a7950-157">システム診断</span><span class="sxs-lookup"><span data-stu-id="a7950-157">System diagnostics</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="monitoring-dashboard"></a><span data-ttu-id="a7950-158">ダッシュボードの監視</span><span class="sxs-lookup"><span data-stu-id="a7950-158">Monitoring dashboard</span></span>

<span data-ttu-id="a7950-159">監視および診断ポータルで、監視ダッシュボードを表示するには**環境**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7950-159">In the Monitoring and diagnostics portal, click the **Environment** tab to view the Monitoring dashboard.</span></span> <span data-ttu-id="a7950-160">ダッシュ ボードで、緑のチェック マークは、事業運営を実行できる環境があることを示します。</span><span class="sxs-lookup"><span data-stu-id="a7950-160">On the dashboard, a green check marks indicate that the environment is available to perform business operations.</span></span> <span data-ttu-id="a7950-161">すべてのマシンおよびコンポーネントの正常性指標が収集されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-161">Health metrics are collected for every machine and component.</span></span> <span data-ttu-id="a7950-162">これらの正常性メトリックには、CPU 使用率、1 秒あたりに記録されるエラー、バッチ ハートビートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a7950-162">These health metrics include CPU usage, errors logged per second, and batch heartbeat.</span></span> <span data-ttu-id="a7950-163">一部のメトリックでは、Microsoft にはしきい値の設定があります。</span><span class="sxs-lookup"><span data-stu-id="a7950-163">For some metrics, Microsoft has set up threshold values.</span></span> <span data-ttu-id="a7950-164">メトリックがしきい値を超えた場合に警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="a7950-164">If a metric crosses the threshold, an alert is triggered.</span></span> <span data-ttu-id="a7950-165">たとえば、CPU 使用率が 70% を超えた場合、警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="a7950-165">For example, an alert is triggered if CPU usage exceeds 70 percent.</span></span> <span data-ttu-id="a7950-166">特定の領域で何が発生しているかを確認するために正常性モニターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a7950-166">You can view the health monitors for a specific area to see what is occurring.</span></span>

### <a name="activity-monitoring"></a><span data-ttu-id="a7950-167">活動の監視</span><span class="sxs-lookup"><span data-stu-id="a7950-167">Activity monitoring</span></span>

<span data-ttu-id="a7950-168">監視および診断ポータルで、アクティビティ監視ツールを使用するには**アクティビティ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7950-168">In the Monitoring and diagnostics portal, click the **Activity** tab to use the Activity monitoring tool.</span></span> <span data-ttu-id="a7950-169">このツールは、お客様または別のユーザーが特定の期間に実行する内容を表示するストーリー ボード ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="a7950-169">This tool provides a storyboard view that shows what you or another user was doing during a specific period.</span></span> <span data-ttu-id="a7950-170">[![activitymonitoringview](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span><span class="sxs-lookup"><span data-stu-id="a7950-170">[![activitymonitoringview](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span></span>

-   <span data-ttu-id="a7950-171">**ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。</span><span class="sxs-lookup"><span data-stu-id="a7950-171">The **User interaction** chart shows a user's activities on various machines in the environment and the SQL utilization trend.</span></span>
-   <span data-ttu-id="a7950-172">**ユーザー負荷** セクションは、すべてのシステム ユーザーを示しています。</span><span class="sxs-lookup"><span data-stu-id="a7950-172">The **User load** section shows all the system users.</span></span> <span data-ttu-id="a7950-173">各グラフには、ユーザーが特定のマシンに費やした時間が示されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-173">Each chart shows the time that the user spent on a specific machine.</span></span>
-   <span data-ttu-id="a7950-174">**活動負荷** セクションには、各コンピューターで実行された活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-174">The **Activity load** section shows the activities that were performed on each machine.</span></span> <span data-ttu-id="a7950-175">活動の上にマウス ポインターを移動すると、タプルとして Form:Control:Action が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-175">If you hover over an activity, you see the Form:Control:Action as a tuple.</span></span> <span data-ttu-id="a7950-176">たとえば、このセクションで LedgerJournal:New:Click を見ている場合、そのユーザー A が、新しい仕訳帳入力を作成するため **LedgerJournals** ページを開き**新規**ボタンをクリックしたのを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-176">For example, if you look at LedgerJournal:New:Click in this section, you can see that user A opened the **LedgerJournals** page and clicked the **New** button to create a new journal entry.</span></span>
-   <span data-ttu-id="a7950-177">**ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7950-177">The **User activity** grid shows the various activities that users performed, based on their session timestamp.</span></span>

<span data-ttu-id="a7950-178">情報ログを絞り込むには、このページで、フィルターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-178">You can use the filters on this page to narrow the information logs.</span></span> <span data-ttu-id="a7950-179">利用可能なフィルタを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a7950-179">Here are some of the filters that are available:</span></span>

-   <span data-ttu-id="a7950-180">**期間** – 選択した日時から 60 分前に戻ります。</span><span class="sxs-lookup"><span data-stu-id="a7950-180">**Time duration** – Go back 60 minutes from the selected date and time.</span></span>
-   <span data-ttu-id="a7950-181">**ユーザー** – 特定のユーザーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="a7950-181">**User** – View a specific user's activities.</span></span>
-   <span data-ttu-id="a7950-182">**検索用語** – 調査中の問題に基づいて検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="a7950-182">**Search terms** – Create a search that is based on the issue that is being investigated.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7950-183">活動の監視ツールは 30 日間だけデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="a7950-183">The Activity monitoring tool retains data for only 30 days.</span></span>

### <a name="raw-information-logs"></a><span data-ttu-id="a7950-184">生の情報ログ</span><span class="sxs-lookup"><span data-stu-id="a7950-184">Raw information logs</span></span>

<span data-ttu-id="a7950-185">高度なトラブルシューティングでは、原情報ログを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-185">For advanced troubleshooting, you can view raw information logs.</span></span> <span data-ttu-id="a7950-186">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="a7950-186">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="a7950-187">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a7950-187">You can then export the logs to do more advanced analysis.</span></span> <span data-ttu-id="a7950-188">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7950-188">The following types of queries are available:</span></span>

-   <span data-ttu-id="a7950-189">速度の遅いクエリ</span><span class="sxs-lookup"><span data-stu-id="a7950-189">Slow queries</span></span>
-   <span data-ttu-id="a7950-190">デッドロック</span><span class="sxs-lookup"><span data-stu-id="a7950-190">Deadlocks</span></span>
-   <span data-ttu-id="a7950-191">クラッシュ</span><span class="sxs-lookup"><span data-stu-id="a7950-191">Crashes</span></span>
-   <span data-ttu-id="a7950-192">財務諸表の問題</span><span class="sxs-lookup"><span data-stu-id="a7950-192">Financial reporting issues</span></span>

### <a name="sql-insights"></a><span data-ttu-id="a7950-193">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="a7950-193">SQL insights</span></span>

<span data-ttu-id="a7950-194">監視および診断ポータルには、パフォーマンスの分析を有効にする高度な SQL トラブルシューティングのツールも含まれます。</span><span class="sxs-lookup"><span data-stu-id="a7950-194">The Monitoring and diagnostics portal also includes advanced SQL troubleshooting tools to enable performance analysis.</span></span> <span data-ttu-id="a7950-195">これらのツールの一部は、Microsoft Dynamics AX 2012 での SQL トラブルシューティングに使用されていた DynPerf ツールと似ています。</span><span class="sxs-lookup"><span data-stu-id="a7950-195">Some of these tools are similar to the DynPerf tool that was used for SQL troubleshooting in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="a7950-196">詳細については、[Lifecycle Services (LCS) でツールを使用したパフォーマンスのトラブルシューティング](performancetroubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7950-196">For more details, see [Performance troubleshooting using tools in Lifecycle Services (LCS)](performancetroubleshooting.md).</span></span>


## <a name="other-resources"></a><span data-ttu-id="a7950-197">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="a7950-197">Other resources</span></span>

- [<span data-ttu-id="a7950-198">環境監視未加工ログの使用方法</span><span class="sxs-lookup"><span data-stu-id="a7950-198">How to use Environment Monitoring View Raw Logs</span></span>](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)

