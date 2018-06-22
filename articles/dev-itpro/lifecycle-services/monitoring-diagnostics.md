---
title: "監視および診断 (Lifecycle Services、LCS)"
description: "このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。"
author: manalidongre
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9d3d84d7df8561f0193e0bb430405da534048e1d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="monitoring-and-diagnostics-lifecycle-services-lcs"></a><span data-ttu-id="7cc63-103">監視および診断 (Lifecycle Services、LCS)</span><span class="sxs-lookup"><span data-stu-id="7cc63-103">Monitoring and diagnostics (Lifecycle Services, LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cc63-104">このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-104">This topic describes the various tools that Microsoft Dynamics Lifecycle Services (LCS) provides to help you monitor, diagnose, and analyze the health of the Microsoft Dynamics 365 for Finance and Operations environments that you manage.</span></span>

<span data-ttu-id="7cc63-105">Microsoft Dynamics 365 for Finance and Operations のクラウド サービスへのオンボード エクスペリエンスを成功させるには、環境の状態を常に把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-105">To have a successful onboarding experience to the cloud service for Microsoft Dynamics 365 for Finance and Operations, you must know the health of your environments at all times.</span></span> <span data-ttu-id="7cc63-106">発生するすべての正常性の問題をトラブルシューティングできることも必要です。</span><span class="sxs-lookup"><span data-stu-id="7cc63-106">You must also be able to troubleshoot any health issues that occur.</span></span> <span data-ttu-id="7cc63-107">Dynamics 365 for Finance and Operations の管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cc63-107">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center for Dynamics 365 for Finance and Operations, contains a collection of monitoring and diagnostics tools that can help guarantee that you have an accurate view of the environments that you manage.</span></span>

## <a name="telemetry-data"></a><span data-ttu-id="7cc63-108">テレメトリ データ</span><span class="sxs-lookup"><span data-stu-id="7cc63-108">Telemetry data</span></span>
<span data-ttu-id="7cc63-109">LCS の監視および診断ポータルの基礎となるテレメトリ データには、監視、診断、分析の 3 つの主要なユース ケースがあります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-109">The telemetry data that is the basis of the Monitoring and diagnostics portal in LCS has three primary use cases: monitoring, diagnostics, and analytics.</span></span> <span data-ttu-id="7cc63-110">[![monitoringanddiagnostics01](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span><span class="sxs-lookup"><span data-stu-id="7cc63-110">[![monitoringanddiagnostics01](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span></span>

### <a name="monitoring"></a><span data-ttu-id="7cc63-111">監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-111">Monitoring</span></span>

<span data-ttu-id="7cc63-112">業務運営ソフトウェアでは、環境が立ち上がっており実行中であるかどうか常に把握して、業務運営を実行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-112">In business operations software, you should always know whether your environment is up and running, so that it can perform business operations.</span></span> <span data-ttu-id="7cc63-113">LCS を通じて環境の稼働状態を簡単に表示できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-113">You should also be able to easily view the health of the environment through LCS.</span></span> <span data-ttu-id="7cc63-114">Microsoft は、2 種類の監視機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-114">Microsoft supports two types of monitoring capabilities:</span></span>

-   <span data-ttu-id="7cc63-115">**可用性の監視** - このタイプの監視は、いつでも利用可能であることを確認するため、環境に対してチェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-115">**Availability monitoring** – This type of monitoring performs a check against the environment to make sure that it's available at all times.</span></span> <span data-ttu-id="7cc63-116">チェックが失敗した場合、Microsoft サービス エンジニアリング チームにすぐに通知されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-116">If the check fails, the Microsoft Service Engineering team is immediately notified.</span></span>
-   <span data-ttu-id="7cc63-117">**稼働状態の監視** – 可用性チェックに加えて、基本的な正常性チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-117">**Health monitoring** – In addition to availability checks, some basic health checks must be performed.</span></span> <span data-ttu-id="7cc63-118">これらの基本的な正常性チェックには、CPU レベル、仮想マシン (VM) のメモリ消費量、および 5 分間の合計デッドロック数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-118">These basic health checks include CPU level, memory consumption of the virtual machines (VMs), and the total number of deadlocks in a five-minute period.</span></span> <span data-ttu-id="7cc63-119">Microsoft テレメトリ インフラストラクチャは、環境から多くの正常性指標を収集します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-119">Microsoft Telemetry Infrastructure collects lots of health metrics from the environments.</span></span> <span data-ttu-id="7cc63-120">メトリックがしきい値を超えている場合は、Microsoft サービス エンジニアリング チームに警告が表示され、問題を調査できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-120">If a metric crosses a threshold value, the Microsoft Service Engineering term is alerted so that it can investigate the issue.</span></span>

### <a name="diagnostics"></a><span data-ttu-id="7cc63-121">診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-121">Diagnostics</span></span>

<span data-ttu-id="7cc63-122">ユーザーが問題を報告したとき、トラブルシューティングのために LCS にあるさまざまなツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-122">When a user reports an issue, you can use various tools in LCS for troubleshooting.</span></span> <span data-ttu-id="7cc63-123">豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-123">The rich set of telemetry data helps you build a storyboard view that shows what that user and other users were doing when the issue was reported.</span></span> <span data-ttu-id="7cc63-124">ユーザーのアクティビティ追跡に加えて、豊富な SQL データがパフォーマンスのトラブルシューティングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-124">In addition to user activity tracking, a rich set of SQL data is available for performance troubleshooting.</span></span>

### <a name="analytics"></a><span data-ttu-id="7cc63-125">分析</span><span class="sxs-lookup"><span data-stu-id="7cc63-125">Analytics</span></span>

<span data-ttu-id="7cc63-126">分析は収集されるテレメトリ データの別の重要なユース ケースです。</span><span class="sxs-lookup"><span data-stu-id="7cc63-126">Analytics is another critical use case for the telemetry data that is collected.</span></span> <span data-ttu-id="7cc63-127">現在のところ、Microsoft だけが分析を実行できるため、Microsoft Power BI を使用して機能の使用状況とパフォーマンスを測定し理解することができます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-127">Currently, only Microsoft can perform analytics, so that it can gauge and understand feature usage and performance through Microsoft Power BI.</span></span>

## <a name="responsibilities"></a><span data-ttu-id="7cc63-128">職責</span><span class="sxs-lookup"><span data-stu-id="7cc63-128">Responsibilities</span></span>
<span data-ttu-id="7cc63-129">Dynamics 365 for Finance and Operations などの管理されたクラウド サービスについては、Microsoft は常に製造環境の正常性をアクティブに監視する責任があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-129">For a managed cloud service such as Dynamics 365 for Finance and Operations, Microsoft is responsible for actively monitoring the health of production environments at all times.</span></span> <span data-ttu-id="7cc63-130">顧客の環境が問題によって影響を受ける場合、Microsoft サービス エンジニア リング チームにすぐに警告が通知されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-130">If a customer's environment is affected by an issue, the Microsoft Service Engineering team is immediately alerted.</span></span> <span data-ttu-id="7cc63-131">チームは問題の調査を開始し、解決策を見つけるために協力します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-131">The team will start to investigate the issue and will work with you to find a resolution.</span></span> <span data-ttu-id="7cc63-132">ただし、非実稼働環境の状態を事前または反応的に監視およびトラブルシューティングする責任はお客様にあります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-132">However, you're responsible for proactively or reactively monitoring and troubleshooting the health of non-production environments.</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="7cc63-133">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="7cc63-133">Access the Monitoring and diagnostics portal</span></span>
1.  <span data-ttu-id="7cc63-134">LCS を開き、適切なプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-134">Open LCS, and navigate to the appropriate project.</span></span>
2.  <span data-ttu-id="7cc63-135">**環境**セクションで、表示する環境を選択してから**完全な詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-135">In the **Environments** section, select the environment to view, and then click **Full details**.</span></span>
3.  <span data-ttu-id="7cc63-136">**環境の詳細**ページで、**環境の監視**をクリックして、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-136">On the **Environment details** page, click **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> <span data-ttu-id="7cc63-137">[![howtogettoenvmonitoring](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span><span class="sxs-lookup"><span data-stu-id="7cc63-137">[![howtogettoenvmonitoring](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span></span>

## <a name="tools"></a><span data-ttu-id="7cc63-138">ツール</span><span class="sxs-lookup"><span data-stu-id="7cc63-138">Tools</span></span>
<span data-ttu-id="7cc63-139">複数のツールとリソースが、監視および診断ポータルで利用できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-139">Several tools and resources are available in the Monitoring and diagnostics portal.</span></span> <span data-ttu-id="7cc63-140">**注記:** すべての環境に、すべてのツールが含まれるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7cc63-140">**Note:** Not all environments contain all the tools.</span></span> <span data-ttu-id="7cc63-141">次のテーブルに、各タイプの環境で使用できるツールを示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-141">The following table shows the tools that are available for each type of environment.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cc63-142">環境タイプ</span><span class="sxs-lookup"><span data-stu-id="7cc63-142">Environment type</span></span></th>
<th><span data-ttu-id="7cc63-143">ツール</span><span class="sxs-lookup"><span data-stu-id="7cc63-143">Tools</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cc63-144">生産システム</span><span class="sxs-lookup"><span data-stu-id="7cc63-144">Production systems</span></span></td>
<td><ul>
<li><span data-ttu-id="7cc63-145">活動の監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-145">Activity monitoring</span></span></li>
<li><span data-ttu-id="7cc63-146">環境の監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-146">Environment monitoring</span></span></li>
<li><span data-ttu-id="7cc63-147">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="7cc63-147">SQL insights</span></span></li>
<li><span data-ttu-id="7cc63-148">システム診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-148">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cc63-149">ユーザー受け入れテスト (UAT)/サンドボックス</span><span class="sxs-lookup"><span data-stu-id="7cc63-149">User acceptance testing (UAT)/sandbox</span></span></td>
<td><ul>
<li><span data-ttu-id="7cc63-150">活動の監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-150">Activity monitoring</span></span></li>
<li><span data-ttu-id="7cc63-151">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="7cc63-151">SQL insights</span></span></li>
<li><span data-ttu-id="7cc63-152">システム診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-152">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cc63-153">デモ/ビルド</span><span class="sxs-lookup"><span data-stu-id="7cc63-153">Demo/build</span></span></td>
<td><ul>
<li><span data-ttu-id="7cc63-154">活動の監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-154">Activity monitoring</span></span></li>
<li><span data-ttu-id="7cc63-155">システム診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-155">System diagnostics</span></span></li>
</ul></td>
</tr>
 <tr class="even">
<td><span data-ttu-id="7cc63-156">顧客/パートナー サブスクリプションに配置される環境</span><span class="sxs-lookup"><span data-stu-id="7cc63-156">Environments deployed in customer/partner subscriptions</span></span></td>
<td><ul>
<li><span data-ttu-id="7cc63-157">システム診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-157">System diagnostics</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="monitoring-dashboard"></a><span data-ttu-id="7cc63-158">ダッシュボードの監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-158">Monitoring dashboard</span></span>

<span data-ttu-id="7cc63-159">監視および診断ポータルで、監視ダッシュボードを表示するには**環境**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-159">In the Monitoring and diagnostics portal, click the **Environment** tab to view the Monitoring dashboard.</span></span> <span data-ttu-id="7cc63-160">ダッシュ ボードで、緑のチェック マークは、事業運営を実行できる環境があることを示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-160">On the dashboard, a green check marks indicate that the environment is available to perform business operations.</span></span> <span data-ttu-id="7cc63-161">すべてのマシンおよびコンポーネントの正常性指標が収集されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-161">Health metrics are collected for every machine and component.</span></span> <span data-ttu-id="7cc63-162">これらの正常性メトリックには、CPU 使用率、1 秒あたりに記録されるエラー、バッチ ハートビートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-162">These health metrics include CPU usage, errors logged per second, and batch heartbeat.</span></span> <span data-ttu-id="7cc63-163">一部のメトリックでは、Microsoft にはしきい値の設定があります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-163">For some metrics, Microsoft has set up threshold values.</span></span> <span data-ttu-id="7cc63-164">メトリックがしきい値を超えた場合に警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-164">If a metric crosses the threshold, an alert is triggered.</span></span> <span data-ttu-id="7cc63-165">たとえば、CPU 使用率が 70% を超えた場合、警告が発生します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-165">For example, an alert is triggered if CPU usage exceeds 70 percent.</span></span> <span data-ttu-id="7cc63-166">特定の領域で何が発生しているかを確認するために正常性モニターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-166">You can view the health monitors for a specific area to see what is occurring.</span></span>

### <a name="activity-monitoring"></a><span data-ttu-id="7cc63-167">活動の監視</span><span class="sxs-lookup"><span data-stu-id="7cc63-167">Activity monitoring</span></span>

<span data-ttu-id="7cc63-168">監視および診断ポータルで、アクティビティ監視ツールを使用するには**アクティビティ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-168">In the Monitoring and diagnostics portal, click the **Activity** tab to use the Activity monitoring tool.</span></span> <span data-ttu-id="7cc63-169">このツールは、お客様または別のユーザーが特定の期間に実行する内容を表示するストーリー ボード ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-169">This tool provides a storyboard view that shows what you or another user was doing during a specific period.</span></span> <span data-ttu-id="7cc63-170">[![activitymonitoringview](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span><span class="sxs-lookup"><span data-stu-id="7cc63-170">[![activitymonitoringview](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span></span>

-   <span data-ttu-id="7cc63-171">**ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。</span><span class="sxs-lookup"><span data-stu-id="7cc63-171">The **User interaction** chart shows a user's activities on various machines in the environment and the SQL utilization trend.</span></span>
-   <span data-ttu-id="7cc63-172">**ユーザー負荷** セクションは、すべてのシステム ユーザーを示しています。</span><span class="sxs-lookup"><span data-stu-id="7cc63-172">The **User load** section shows all the system users.</span></span> <span data-ttu-id="7cc63-173">各グラフには、ユーザーが特定のマシンに費やした時間が示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-173">Each chart shows the time that the user spent on a specific machine.</span></span>
-   <span data-ttu-id="7cc63-174">**活動負荷** セクションには、各コンピューターで実行された活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-174">The **Activity load** section shows the activities that were performed on each machine.</span></span> <span data-ttu-id="7cc63-175">活動の上にマウス ポインターを移動すると、タプルとして Form:Control:Action が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-175">If you hover over an activity, you see the Form:Control:Action as a tuple.</span></span> <span data-ttu-id="7cc63-176">たとえば、このセクションで LedgerJournal:New:Click を見ている場合、そのユーザー A が、新しい仕訳帳入力を作成するため **LedgerJournals** ページを開き**新規**ボタンをクリックしたのを表示できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-176">For example, if you look at LedgerJournal:New:Click in this section, you can see that user A opened the **LedgerJournals** page and clicked the **New** button to create a new journal entry.</span></span>
-   <span data-ttu-id="7cc63-177">**ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-177">The **User activity** grid shows the various activities that users performed, based on their session timestamp.</span></span>

<span data-ttu-id="7cc63-178">情報ログを絞り込むには、このページで、フィルターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-178">You can use the filters on this page to narrow the information logs.</span></span> <span data-ttu-id="7cc63-179">利用可能なフィルタを次に示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-179">Here are some of the filters that are available:</span></span>

-   <span data-ttu-id="7cc63-180">**期間** – 選択した日時から 60 分前に戻ります。</span><span class="sxs-lookup"><span data-stu-id="7cc63-180">**Time duration** – Go back 60 minutes from the selected date and time.</span></span>
-   <span data-ttu-id="7cc63-181">**ユーザー** – 特定のユーザーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-181">**User** – View a specific user's activities.</span></span>
-   <span data-ttu-id="7cc63-182">**検索用語** – 調査中の問題に基づいて検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-182">**Search terms** – Create a search that is based on the issue that is being investigated.</span></span>

<span data-ttu-id="7cc63-183">**重要:** 活動の監視ツールは 30 日間だけデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-183">**Important:** The Activity monitoring tool retains data for only 30 days.</span></span>

### <a name="raw-information-logs"></a><span data-ttu-id="7cc63-184">生の情報ログ</span><span class="sxs-lookup"><span data-stu-id="7cc63-184">Raw information logs</span></span>

<span data-ttu-id="7cc63-185">高度なトラブルシューティングでは、原情報ログを表示できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-185">For advanced troubleshooting, you can view raw information logs.</span></span> <span data-ttu-id="7cc63-186">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-186">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="7cc63-187">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-187">You can then export the logs to do more advanced analysis.</span></span> <span data-ttu-id="7cc63-188">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-188">The following types of queries are available:</span></span>

-   <span data-ttu-id="7cc63-189">速度の遅いクエリ</span><span class="sxs-lookup"><span data-stu-id="7cc63-189">Slow queries</span></span>
-   <span data-ttu-id="7cc63-190">デッドロック</span><span class="sxs-lookup"><span data-stu-id="7cc63-190">Deadlocks</span></span>
-   <span data-ttu-id="7cc63-191">クラッシュ</span><span class="sxs-lookup"><span data-stu-id="7cc63-191">Crashes</span></span>
-   <span data-ttu-id="7cc63-192">財務諸表の問題</span><span class="sxs-lookup"><span data-stu-id="7cc63-192">Financial reporting issues</span></span>

### <a name="sql-insights"></a><span data-ttu-id="7cc63-193">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="7cc63-193">SQL insights</span></span>

<span data-ttu-id="7cc63-194">監視および診断ポータルには、パフォーマンスの分析を有効にする高度な SQL トラブルシューティングのツールも含まれます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-194">The Monitoring and diagnostics portal also includes advanced SQL troubleshooting tools to enable performance analysis.</span></span> <span data-ttu-id="7cc63-195">これらのツールの一部は、SQL Microsoft Dynamics AX 2012 でのトラブルシューティングに使用されていた DynPerf ツールと似ています。</span><span class="sxs-lookup"><span data-stu-id="7cc63-195">Some of these tools resemble the DynPerf tool that was used for SQL troubleshooting in Microsoft Dynamics AX 2012.</span></span>

#### <a name="performance-metrics"></a><span data-ttu-id="7cc63-196">パフォーマンス メトリックス</span><span class="sxs-lookup"><span data-stu-id="7cc63-196">Performance metrics</span></span>

<span data-ttu-id="7cc63-197">**パフォーマンス メトリックス** ページには、論理入出力、実行カウント、期間、CPU 時間、および待機数に基づいて、選択した期間にシステムで実行された最もコストのかかったクエリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-197">The **Performance metrics** page shows the most expensive queries that were run in the system during the selected period, based on logical I/O, execution count, duration, CPU time, and wait count.</span></span> <span data-ttu-id="7cc63-198">このデータは SQL クエリ ストアからクエリされます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-198">This data is queried from the SQL query store.</span></span> <span data-ttu-id="7cc63-199">データは 30 日間保持され、ツールは毎日、協定世界時 (UTC) の午後 10 時にデータ収集を実行します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-199">The data is retained for 30 days, and the tool runs its data collection every day at 10 PM Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7cc63-200">[![sqlinsights](./media/sqlinsights-1024x512.jpg)](./media/sqlinsights.jpg) このツールを使用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7cc63-200">[![sqlinsights](./media/sqlinsights-1024x512.jpg)](./media/sqlinsights.jpg) To use the tool, follow these steps.</span></span>

1.  <span data-ttu-id="7cc63-201">過去 30 日間の期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-201">Select a period during the last 30 days.</span></span>
2.  <span data-ttu-id="7cc63-202">クエリ結果が表示されたら、期間グラフ内の 1 つ目のバーを選択して、クエリが他の基準に該当する場所を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-202">When the query results appear, select the first bar in the duration chart to highlight where the query falls on other metrics.</span></span>
3.  <span data-ttu-id="7cc63-203">**ステートメント**タブで、クエリを表示、またはクエリの実行計画をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-203">On the **Statement** tab, view the query, or download the query execution plan.</span></span>

#### <a name="sql-now-tool"></a><span data-ttu-id="7cc63-204">SQL now ツール</span><span class="sxs-lookup"><span data-stu-id="7cc63-204">SQL now tool</span></span>

<span data-ttu-id="7cc63-205">just-in-time 診断では、SQL now ツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-205">You can use the SQL now tool for just-in-time diagnostics.</span></span> <span data-ttu-id="7cc63-206">たとえば、レポートの実行が遅いと、任意のロック/ブロック問題があるか、およびバック グラウンドでどの SQL ステートメントが実行しているかを表示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-206">For example, a report is running slowly, and you want to see whether there are any locking/blocking issues and what SQL statements are running in the background.</span></span> <span data-ttu-id="7cc63-207">この場合、レポートの実行中にこのページを開いて更新できます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-207">In this case, you can open this page and refresh it while the report is being run.</span></span>

#### <a name="index-analysis"></a><span data-ttu-id="7cc63-208">インデックス分析</span><span class="sxs-lookup"><span data-stu-id="7cc63-208">Index analysis</span></span>

<span data-ttu-id="7cc63-209">インデックス分析ツールには、ユーザーのスキャン、ユーザーのシーク、ユーザーの更新プログラム、および行の数に基づいて、集計インデックスとテーブル情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7cc63-209">The Index analysis tool shows aggregated index and table information, based on user scans, user seeks, user updates, and row count.</span></span> <span data-ttu-id="7cc63-210">パフォーマンス測定基準と同様に、このツールは追加のテーブル メトリックスと共に選択したインデックスのトレンドを表示します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-210">Like performance metrics, this tool shows the trend for the selected index together with additional table metrics.</span></span>

### <a name="system-diagnostics"></a><span data-ttu-id="7cc63-211">システム診断</span><span class="sxs-lookup"><span data-stu-id="7cc63-211">System diagnostics</span></span>

<span data-ttu-id="7cc63-212">システム診断ツールは、環境に対して事前に定義されたルール セットを実行するルール ベースのフレームワークであり、ルールのステータスに関するレポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-212">The System diagnostic tool is a rule-based framework that runs a predefined set of rules against the environment and provides a report about the status of the rules.</span></span> <span data-ttu-id="7cc63-213">エラーが発生した場合、このツールは、問題に対処するための推奨事項を提供します。</span><span class="sxs-lookup"><span data-stu-id="7cc63-213">If failures occur, this tool provides recommendations for addressing the issue.</span></span> <span data-ttu-id="7cc63-214">システムの診断ツールを開始するには、LCSプロジェクト ダッシュ ボードで [ハンバーガー] アイコンをクリックし、**システム診断** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7cc63-214">To start the System diagnostics tool, on the LCS project dashboard, click the hamburger icon, and then click **System diagnostic**.</span></span>




