---
title: Lifecycle Services (LCS) の監視および診断ツール
description: このトピックでは、管理する Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。
author: manalidongre
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c49ba3a1c3f6c69b3eed6b846d9c6f6f55372a66
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249065"
---
# <a name="monitoring-and-diagnostics-tools-in-lifecycle-services-lcs"></a><span data-ttu-id="2753e-103">Lifecycle Services (LCS) の監視および診断ツール</span><span class="sxs-lookup"><span data-stu-id="2753e-103">Monitoring and diagnostics tools in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2753e-104">このトピックでは、管理する Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2753e-104">This topic describes the various tools that Microsoft Dynamics Lifecycle Services (LCS) provides to help you monitor, diagnose, and analyze the health of the Finance and Operations environments that you manage.</span></span>

<span data-ttu-id="2753e-105">クラウド サービスへのオンボード エクスペリエンスを成功させるには、環境の状態を常に把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-105">To have a successful onboarding experience to the cloud service, you must know the health of your environments at all times.</span></span> <span data-ttu-id="2753e-106">発生するすべての正常性の問題をトラブルシューティングできることも必要です。</span><span class="sxs-lookup"><span data-stu-id="2753e-106">You must also be able to troubleshoot any health issues that occur.</span></span> <span data-ttu-id="2753e-107">管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2753e-107">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center, contains a collection of monitoring and diagnostics tools that can help to ensure that you have an accurate view of the environments that you manage.</span></span>

## <a name="telemetry-data"></a><span data-ttu-id="2753e-108">テレメトリ データ</span><span class="sxs-lookup"><span data-stu-id="2753e-108">Telemetry data</span></span>

<span data-ttu-id="2753e-109">LCS の監視および診断ポータルの基礎となるテレメトリ データには、監視、診断、分析の 3 つの主要なユース ケースがあります。</span><span class="sxs-lookup"><span data-stu-id="2753e-109">The telemetry data that is the basis of the Monitoring and diagnostics portal in LCS has three primary use cases: monitoring, diagnostics, and analytics.</span></span> 

<span data-ttu-id="2753e-110">[![モニタリング、診断、分析](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span><span class="sxs-lookup"><span data-stu-id="2753e-110">[![Monitoring, diagnostics, and analytics](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)</span></span>

### <a name="monitoring"></a><span data-ttu-id="2753e-111">監視</span><span class="sxs-lookup"><span data-stu-id="2753e-111">Monitoring</span></span>

<span data-ttu-id="2753e-112">業務運営ソフトウェアでは、環境が立ち上がっており実行中であるかどうか常に把握して、業務運営を実行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-112">In business operations software, you should always know whether your environment is up and running, so that it can perform business operations.</span></span> <span data-ttu-id="2753e-113">LCS を通じて環境の稼働状態を簡単に表示できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-113">You should also be able to easily view the health of the environment through LCS.</span></span> <span data-ttu-id="2753e-114">Microsoft は、2 種類の監視機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2753e-114">Microsoft supports two types of monitoring capabilities:</span></span>

- <span data-ttu-id="2753e-115">**可用性の監視** - このタイプの監視は、いつでも利用可能であることを確認するため、環境に対してチェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="2753e-115">**Availability monitoring** – This type of monitoring performs a check against the environment to make sure that it's available at all times.</span></span> <span data-ttu-id="2753e-116">チェックが失敗した場合、Microsoft サービス エンジニアリング チームにすぐに通知されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-116">If the check fails, the Microsoft Service Engineering team is immediately notified.</span></span>
- <span data-ttu-id="2753e-117">**稼働状態の監視** – 可用性チェックに加えて、基本的な正常性チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-117">**Health monitoring** – In addition to availability checks, some basic health checks must be performed.</span></span> <span data-ttu-id="2753e-118">これらのヘルス チェックは、アプリケーション オブジェクト サーバー (AOS)、バッチ フレームワーク、データ マネジメント フレームワーク、 Microsoft Azure SQL、Management Reporter などのさまざまなコンポーネントを対象としています。</span><span class="sxs-lookup"><span data-stu-id="2753e-118">These health checks span various components, such as Application Object Server (AOS), Batch Framework, Data Management Framework, Microsoft Azure SQL, and Management Reporter.</span></span> <span data-ttu-id="2753e-119">これらのチェックは、環境から収集されたテレメトリ、環境を継続的に監視するウォッチドッグ サービスにより実行されるチェック、環境が出力する CPU カウンターや他のシステム レベル カウンターなど、複数のデータ ソースに基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="2753e-119">These checks are done based on multiple data sources, such as the telemetry that is collected from the environments, checks that are done by a watchdog service that continuously monitors the environment, and CPU counters and other system-level counters that the environment emits.</span></span> <span data-ttu-id="2753e-120">いくつかのヘルス チェックは自動修復され、即座に軽減されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-120">Some health checks are self-healing and are mitigated immediately.</span></span> <span data-ttu-id="2753e-121">ただし、他のヘルス チェックは調査のための Microsoft サービス エンジニアリング チームに報告されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-121">However, other health checks are reported to the Microsoft Service Engineering team for investigation.</span></span>

### <a name="diagnostics"></a><span data-ttu-id="2753e-122">診断</span><span class="sxs-lookup"><span data-stu-id="2753e-122">Diagnostics</span></span>

<span data-ttu-id="2753e-123">ユーザーが問題を報告したとき、トラブルシューティングのために LCS にあるさまざまなツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-123">When a user reports an issue, you can use various tools in LCS for troubleshooting.</span></span> <span data-ttu-id="2753e-124">豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2753e-124">The rich set of telemetry data helps you build a storyboard view that shows what that user and other users were doing when the issue was reported.</span></span> <span data-ttu-id="2753e-125">ユーザーのアクティビティ追跡に加えて、豊富な SQL データがパフォーマンスのトラブルシューティングに使用できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-125">In addition to user activity tracking, a rich set of SQL data is available for performance troubleshooting.</span></span>

### <a name="analytics"></a><span data-ttu-id="2753e-126">分析</span><span class="sxs-lookup"><span data-stu-id="2753e-126">Analytics</span></span>

<span data-ttu-id="2753e-127">分析は収集されるテレメトリ データの別の重要なユース ケースです。</span><span class="sxs-lookup"><span data-stu-id="2753e-127">Analytics is another critical use case for the telemetry data that is collected.</span></span> <span data-ttu-id="2753e-128">現在のところ、Microsoft だけが分析を実行できるため、Microsoft Power BI を使用して機能の使用状況とパフォーマンスを測定し理解することができます。</span><span class="sxs-lookup"><span data-stu-id="2753e-128">Currently, only Microsoft can perform analytics, so that it can gauge and understand feature usage and performance through Microsoft Power BI.</span></span>

## <a name="responsibilities"></a><span data-ttu-id="2753e-129">職責</span><span class="sxs-lookup"><span data-stu-id="2753e-129">Responsibilities</span></span>

<span data-ttu-id="2753e-130">Finance and Operations などの管理されたクラウド サービスについては、Microsoft は常に実稼動環境の正常性をアクティブに監視する責任があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-130">For a managed cloud service such as Finance and Operations, Microsoft is responsible for actively monitoring the health of production environments at all times.</span></span> <span data-ttu-id="2753e-131">顧客の環境が問題によって影響を受ける場合、Microsoft サービス エンジニア リング チームにすぐに警告が通知されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-131">If a customer's environment is affected by an issue, the Microsoft Service Engineering team is immediately alerted.</span></span> <span data-ttu-id="2753e-132">チームは問題の調査を開始し、解決策を見つけるために協力します。</span><span class="sxs-lookup"><span data-stu-id="2753e-132">The team will start to investigate the issue and will work with you to find a resolution.</span></span> <span data-ttu-id="2753e-133">ただし、非実稼働環境の状態を事前または反応的に監視およびトラブルシューティングする責任はお客様にあります。</span><span class="sxs-lookup"><span data-stu-id="2753e-133">However, you're responsible for proactively or reactively monitoring and troubleshooting the health of non-production environments.</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="2753e-134">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="2753e-134">Access the Monitoring and diagnostics portal</span></span>

1. <span data-ttu-id="2753e-135">LCS を開き、適切なプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="2753e-135">Open LCS, and navigate to the appropriate project.</span></span>
2. <span data-ttu-id="2753e-136">**環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2753e-136">In the **Environments** section, select the environment to view, and then select **Full details**.</span></span>
3. <span data-ttu-id="2753e-137">環境の詳細ページで、**環境の監視**を選択して、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="2753e-137">On the environment details page, select **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> 

<span data-ttu-id="2753e-138">[![環境の詳細](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span><span class="sxs-lookup"><span data-stu-id="2753e-138">[![Environment details](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)</span></span>

## <a name="tools"></a><span data-ttu-id="2753e-139">ツール</span><span class="sxs-lookup"><span data-stu-id="2753e-139">Tools</span></span>

<span data-ttu-id="2753e-140">複数のツールとリソースが、監視および診断ポータルで利用できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-140">Several tools and resources are available in the Monitoring and diagnostics portal.</span></span> 

> [!NOTE]
> <span data-ttu-id="2753e-141">すべての環境に、すべてのツールが含まれるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="2753e-141">Not all environments contain all the tools.</span></span> <span data-ttu-id="2753e-142">次のテーブルに、各タイプの環境で使用できるツールを示します。</span><span class="sxs-lookup"><span data-stu-id="2753e-142">The following table shows the tools that are available for each type of environment.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2753e-143">環境タイプ</span><span class="sxs-lookup"><span data-stu-id="2753e-143">Environment type</span></span></th>
<th><span data-ttu-id="2753e-144">ツール</span><span class="sxs-lookup"><span data-stu-id="2753e-144">Tools</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2753e-145">生産システム</span><span class="sxs-lookup"><span data-stu-id="2753e-145">Production systems</span></span></td>
<td><ul>
<li><span data-ttu-id="2753e-146">活動の監視</span><span class="sxs-lookup"><span data-stu-id="2753e-146">Activity monitoring</span></span></li>
<li><span data-ttu-id="2753e-147">環境の監視</span><span class="sxs-lookup"><span data-stu-id="2753e-147">Environment monitoring</span></span></li>
<li><span data-ttu-id="2753e-148">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="2753e-148">SQL insights</span></span></li>
<li><span data-ttu-id="2753e-149">システム診断</span><span class="sxs-lookup"><span data-stu-id="2753e-149">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2753e-150">ユーザー受け入れテスト (UAT)/サンドボックス</span><span class="sxs-lookup"><span data-stu-id="2753e-150">User acceptance testing (UAT)/sandbox</span></span></td>
<td><ul>
<li><span data-ttu-id="2753e-151">活動の監視</span><span class="sxs-lookup"><span data-stu-id="2753e-151">Activity monitoring</span></span></li>
<li><span data-ttu-id="2753e-152">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="2753e-152">SQL insights</span></span></li>
<li><span data-ttu-id="2753e-153">システム診断</span><span class="sxs-lookup"><span data-stu-id="2753e-153">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2753e-154">デモ/ビルド</span><span class="sxs-lookup"><span data-stu-id="2753e-154">Demo/build</span></span></td>
<td><ul>
<li><span data-ttu-id="2753e-155">活動の監視</span><span class="sxs-lookup"><span data-stu-id="2753e-155">Activity monitoring</span></span></li>
<li><span data-ttu-id="2753e-156">システム診断</span><span class="sxs-lookup"><span data-stu-id="2753e-156">System diagnostics</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="2753e-157">顧客/パートナー サブスクリプションに配置される環境</span><span class="sxs-lookup"><span data-stu-id="2753e-157">Environments deployed in customer/partner subscriptions</span></span></td>
<td><ul>
<li><span data-ttu-id="2753e-158">システム診断</span><span class="sxs-lookup"><span data-stu-id="2753e-158">System diagnostics</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="monitoring-dashboard"></a><span data-ttu-id="2753e-159">ダッシュボードの監視</span><span class="sxs-lookup"><span data-stu-id="2753e-159">Monitoring dashboard</span></span>

<span data-ttu-id="2753e-160">**環境の監視**ページで、**正常性指標** タブを選択して、**監視**ダッシュボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2753e-160">On the **Environment monitoring** page, select the **Health metrics** tab to view the **Monitoring** dashboard.</span></span> <span data-ttu-id="2753e-161">すべてのマシンおよびコンポーネントの正常性指標が収集されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-161">Health metrics are collected for every machine and component.</span></span> <span data-ttu-id="2753e-162">これらの正常性メトリックには、CPU 使用率、使用可能なメモリ、1 秒あたりに記録されるエラー、バッチ ハートビートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2753e-162">These health metrics include CPU usage, available memory, errors logged per second, and batch heartbeat.</span></span> <span data-ttu-id="2753e-163">指標の異常に関する警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-163">You're alerted about any abnormalities in the metrics.</span></span> <span data-ttu-id="2753e-164">いくつかの警告は自動修復されますが、Microsoft サービス エンジニアリング チームは他の警告の原因を調査し、それらを軽減するアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="2753e-164">Although some alerts are self-healing, the Microsoft Service Engineering team will investigate the cause of other alerts and then take action to mitigate them.</span></span> <span data-ttu-id="2753e-165">特定の領域で何が発生しているかを確認するために正常性モニターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2753e-165">You can view the health monitors for a specific area to see what is occurring.</span></span>

### <a name="activity-monitoring"></a><span data-ttu-id="2753e-166">活動の監視</span><span class="sxs-lookup"><span data-stu-id="2753e-166">Activity monitoring</span></span>

<span data-ttu-id="2753e-167">**環境の監視**ページで、**活動**タブを選択して、活動監視ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="2753e-167">On the **Environment monitoring** page, select the **Activity** tab to use the Activity monitoring tool.</span></span> <span data-ttu-id="2753e-168">このツールは、お客様または別のユーザーが特定の期間に実行する内容を表示するストーリー ボード ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="2753e-168">This tool provides a storyboard view that shows what you or another user was doing during a specific period.</span></span> 

<span data-ttu-id="2753e-169">[![活動タブ](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span><span class="sxs-lookup"><span data-stu-id="2753e-169">[![Activity tab](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)</span></span>

- <span data-ttu-id="2753e-170">**ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。</span><span class="sxs-lookup"><span data-stu-id="2753e-170">The **User interaction** chart shows a user's activities on various machines in the environment and the SQL utilization trend.</span></span>
- <span data-ttu-id="2753e-171">**ユーザー負荷** セクションは、すべてのシステム ユーザーを示しています。</span><span class="sxs-lookup"><span data-stu-id="2753e-171">The **User load** section shows all the system users.</span></span> <span data-ttu-id="2753e-172">各グラフには、ユーザーが特定のマシンに費やした時間が示されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-172">Each chart shows the time that the user spent on a specific machine.</span></span>
- <span data-ttu-id="2753e-173">**活動負荷** セクションには、各コンピューターで実行された活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-173">The **Activity load** section shows the activities that were performed on each machine.</span></span> <span data-ttu-id="2753e-174">活動の上にマウス ポインターを移動すると、タプルとして Form:Control:Action が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-174">If you hover over an activity, you see the Form:Control:Action as a tuple.</span></span> <span data-ttu-id="2753e-175">たとえば、このセクションで LedgerJournal:New:Click を見ている場合、そのユーザー A が、新しい仕訳帳入力を作成するため **LedgerJournals** ページを開き**新規**ボタンを選択したのを表示できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-175">For example, if you look at LedgerJournal:New:Click in this section, you can see that user A opened the **LedgerJournals** page and selected the **New** button to create a new journal entry.</span></span>
- <span data-ttu-id="2753e-176">**ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2753e-176">The **User activity** grid shows the various activities that users performed, based on their session timestamp.</span></span>

<span data-ttu-id="2753e-177">情報ログを絞り込むには、このページで、フィルターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-177">You can use the filters on this page to narrow the information logs.</span></span> <span data-ttu-id="2753e-178">利用可能なフィルタを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2753e-178">Here are some of the filters that are available:</span></span>

- <span data-ttu-id="2753e-179">**期間** – 選択した日時から 60 分前に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2753e-179">**Time duration** – Go back 60 minutes from the selected date and time.</span></span>
- <span data-ttu-id="2753e-180">**ユーザー** – 特定のユーザーの活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="2753e-180">**User** – View a specific user's activities.</span></span>
- <span data-ttu-id="2753e-181">**検索用語** – 調査中の問題に基づいて検索を作成します。</span><span class="sxs-lookup"><span data-stu-id="2753e-181">**Search terms** – Create a search that is based on the issue that is being investigated.</span></span>

> [!NOTE]
> <span data-ttu-id="2753e-182">ページには、既定ではデータが読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="2753e-182">The page doesn't load data by default.</span></span> <span data-ttu-id="2753e-183">ページを表示するために必要なデータをロードするには、期間を選択し、**送信時刻**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2753e-183">To load the data that is required in order to show the page, you must select the time duration and then select **Submit time**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2753e-184">活動の監視ツールは 30 日間だけデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="2753e-184">The Activity monitoring tool retains data for only 30 days.</span></span>

### <a name="raw-information-logs"></a><span data-ttu-id="2753e-185">生の情報ログ</span><span class="sxs-lookup"><span data-stu-id="2753e-185">Raw information logs</span></span>

<span data-ttu-id="2753e-186">高度なトラブルシューティングでは、原情報ログを表示できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-186">For advanced troubleshooting, you can view raw information logs.</span></span> <span data-ttu-id="2753e-187">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="2753e-187">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="2753e-188">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="2753e-188">You can then export the logs to do more advanced analysis.</span></span> <span data-ttu-id="2753e-189">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2753e-189">The following types of queries are available:</span></span>

- <span data-ttu-id="2753e-190">速度の遅いクエリ</span><span class="sxs-lookup"><span data-stu-id="2753e-190">Slow queries</span></span>
- <span data-ttu-id="2753e-191">デッドロック</span><span class="sxs-lookup"><span data-stu-id="2753e-191">Deadlocks</span></span>
- <span data-ttu-id="2753e-192">クラッシュ</span><span class="sxs-lookup"><span data-stu-id="2753e-192">Crashes</span></span>
- <span data-ttu-id="2753e-193">財務諸表の問題</span><span class="sxs-lookup"><span data-stu-id="2753e-193">Financial reporting issues</span></span>

### <a name="sql-insights"></a><span data-ttu-id="2753e-194">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="2753e-194">SQL insights</span></span>

<span data-ttu-id="2753e-195">監視および診断ポータルには、パフォーマンスの分析を有効にする高度な SQL トラブルシューティングのツールも含まれます。</span><span class="sxs-lookup"><span data-stu-id="2753e-195">The Monitoring and diagnostics portal also includes advanced SQL troubleshooting tools to enable performance analysis.</span></span> <span data-ttu-id="2753e-196">これらのツールの一部は、Microsoft Dynamics AX 2012 での SQL トラブルシューティングに使用されていた DynPerf ツールと似ています。</span><span class="sxs-lookup"><span data-stu-id="2753e-196">Some of these tools are similar to the DynPerf tool that was used for SQL troubleshooting in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="2753e-197">詳細については、[Lifecycle Services (LCS) でツールを使用したパフォーマンスのトラブルシューティング](performancetroubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2753e-197">For more details, see [Performance troubleshooting using tools in Lifecycle Services (LCS)](performancetroubleshooting.md).</span></span>

## <a name="other-resources"></a><span data-ttu-id="2753e-198">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="2753e-198">Other resources</span></span>

- [<span data-ttu-id="2753e-199">環境監視未加工ログの使用方法</span><span class="sxs-lookup"><span data-stu-id="2753e-199">How to use Environment Monitoring View Raw Logs</span></span>](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)
