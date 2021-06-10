---
title: 運用サポートと監視
description: このトピックでは、プロジェクトのライフサイクルに関連するサポートのタイプと、環境を監視するためのベスト プラクティスについて説明します。
author: PedroTubal
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: v-petbal
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 72b9dab03a28b73d81bd2e3999232da47d1604a8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018894"
---
# <a name="production-support-and-monitoring"></a><span data-ttu-id="45ad2-103">運用サポートと監視</span><span class="sxs-lookup"><span data-stu-id="45ad2-103">Production support and monitoring</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="45ad2-104">プロジェクトの実装中および Go-Live 後に適切な経験をするために、利用できるさまざまなタイプのサービスと、すべてのシナリオに対して正しいサポートを受ける方法を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="45ad2-104">To ensure a good experience during the implementation of a project and after go-live, it's important that you understand the different types of servicing that are available and how you can get the correct support for every scenario.</span></span> <span data-ttu-id="45ad2-105">このトピックでは、各タイプのサポートを手配する方法について説明し、および使用可能ないくつかのツールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-105">This topic explains how to engage each type of support and learn about some of the tools available.</span></span>

<span data-ttu-id="45ad2-106">Microsoft のツールおよびサポートは、インフラストラクチャとアプリケーションのサポートを提供することにより、環境の安定性および有効性に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-106">Microsoft tools and support help ensure the stability and effectiveness of your environment by providing infrastructure and application support.</span></span> <span data-ttu-id="45ad2-107">ただし、このサポートは、実装されているシステムとその環境をパートナーおよびクライアントが正しく開発、テスト、構成、管理、および監視している場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="45ad2-107">However, this support can be effective only if partners and clients correctly develop, test, configure, manage, and monitor the implemented system and its environments.</span></span>

![Microsoft が提供するサポート](./media/support-provided-microsoft.png)

## <a name="supporting-actions"></a><span data-ttu-id="45ad2-109">サポート アクション</span><span class="sxs-lookup"><span data-stu-id="45ad2-109">Supporting actions</span></span>

<span data-ttu-id="45ad2-110">サポート アクションは、次の 3 つのカテゴリにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-110">Supporting actions can be grouped into three categories:</span></span>

- <span data-ttu-id="45ad2-111">セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="45ad2-111">Self-service</span></span>
- <span data-ttu-id="45ad2-112">サービス要求</span><span class="sxs-lookup"><span data-stu-id="45ad2-112">Service request</span></span>
- <span data-ttu-id="45ad2-113">サポート 要求</span><span class="sxs-lookup"><span data-stu-id="45ad2-113">Support request</span></span>

<span data-ttu-id="45ad2-114">カテゴリに応じて、アクションはさまざまな方法でトリガーされ、異なるリード タイムを含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-114">Depending on the category, the actions are triggered in different ways and might involve different lead times.</span></span>

### <a name="self-service"></a><span data-ttu-id="45ad2-115">セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="45ad2-115">Self-service</span></span>

<span data-ttu-id="45ad2-116">セルフサービス アクションは、ユーザーがいつでもトリガーすることができ、リード タイムは含まれません。</span><span class="sxs-lookup"><span data-stu-id="45ad2-116">Self-service actions can be triggered by users at any time and involve no lead time.</span></span> <span data-ttu-id="45ad2-117">次にユーザーがセルフサービス アクションを開始するいくつかの理由を挙げます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-117">Here are some of the reasons why a user might initiate a self-service action:</span></span>

- <span data-ttu-id="45ad2-118">プロモーション コード (非運用環境で) 。</span><span class="sxs-lookup"><span data-stu-id="45ad2-118">Promote code (in non-production environments).</span></span>
- <span data-ttu-id="45ad2-119">[非運用環境間でのデータベースの移動](../../dev-itpro/database/dbmovement-operations.md).</span><span class="sxs-lookup"><span data-stu-id="45ad2-119">[Move databases between non-production environments](../../dev-itpro/database/dbmovement-operations.md).</span></span>
- <span data-ttu-id="45ad2-120">[運用環境でのアップグレード](../../dev-itpro/migration-upgrade/upgrade-latest-update.md)。</span><span class="sxs-lookup"><span data-stu-id="45ad2-120">[Upgrade a production environment](../../dev-itpro/migration-upgrade/upgrade-latest-update.md).</span></span>
- [<span data-ttu-id="45ad2-121">メンテナンス モードをオンまたはオフに切り替える</span><span class="sxs-lookup"><span data-stu-id="45ad2-121">Turn maintenance mode on or off</span></span>](../../dev-itpro/sysadmin/maintenance-mode.md)
- <span data-ttu-id="45ad2-122">今後のサービス更新の自動展開を一時停止します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-122">Pause upcoming automatic deployment of a service update.</span></span>
- <span data-ttu-id="45ad2-123">非運用環境でサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-123">Restart services in non-production environments.</span></span>
- <span data-ttu-id="45ad2-124">パフォーマンス アクションを完了します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-124">Complete performance actions.</span></span>

### <a name="service-request"></a><span data-ttu-id="45ad2-125">サービス要求</span><span class="sxs-lookup"><span data-stu-id="45ad2-125">Service request</span></span>

<span data-ttu-id="45ad2-126">通常、サービス要求は、サポート チケットの作成によってトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-126">Service requests are usually triggered by a creating a support ticket.</span></span> <span data-ttu-id="45ad2-127">これらには、Dynamics Service Engineering (DSE) チームの協力が含まれます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-127">They involve the cooperation of the Dynamics Service Engineering (DSE) team.</span></span> <span data-ttu-id="45ad2-128">各要求には、指定されたリード タイムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-128">Each request will involve designated lead time.</span></span> <span data-ttu-id="45ad2-129">たとえば、サービス要求は環境の配置を要求するために作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-129">A service request might be created to request environment deployment, for example.</span></span>

#### <a name="recommended-practices-for-working-with-the-dse-team"></a><span data-ttu-id="45ad2-130">DSE チームを使用するための推奨事項</span><span class="sxs-lookup"><span data-stu-id="45ad2-130">Recommended practices for working with the DSE team</span></span>

- <span data-ttu-id="45ad2-131">各タイプのサービス要求に対して、応答時間または Service Level Agreements (SLA) があることを考慮します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-131">Consider that there are turnaround times or Service Level Agreements (SLAs) for each type of service request.</span></span>
- <span data-ttu-id="45ad2-132">サポート要求の方がケースにより適している場合は、サービス要求を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="45ad2-132">Don't use a service request if a support request is more suitable for your case.</span></span>
- <span data-ttu-id="45ad2-133">適切なタイプの要求を作成していることを確認するには、[サービス要求タイプおよび SLA](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md#service-request-types-and-slas) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45ad2-133">To ensure that you make the correct type of request, see [Service request types and SLAs](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md#service-request-types-and-slas).</span></span>

### <a name="support-request"></a><span data-ttu-id="45ad2-134">サポート要求</span><span class="sxs-lookup"><span data-stu-id="45ad2-134">Support request</span></span>

<span data-ttu-id="45ad2-135">通常、その他のシナリオは、サポート要求を開始することで解決できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-135">Other scenarios can usually be resolved by opening a support request.</span></span> <span data-ttu-id="45ad2-136">これらの要求にはリード タイムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-136">These requests involve lead time.</span></span> <span data-ttu-id="45ad2-137">サポート要求を作成するいくつかの理由は以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="45ad2-137">Here are some of the reasons for creating a support request:</span></span>

- <span data-ttu-id="45ad2-138">Go-live 後の運用環境のポイントインタイム復元を行います。</span><span class="sxs-lookup"><span data-stu-id="45ad2-138">Do a point-in-time restore of a production environment after go-live.</span></span>
- <span data-ttu-id="45ad2-139">サービスの更新で回帰にフラグを立て、例外のオプトアウトを求めます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-139">Flag a regression in a service update, and ask for an exception opt-out.</span></span>
- <span data-ttu-id="45ad2-140">パフォーマンス関連の要求を行います (セルフサービスでは完了できないタスクのため)。</span><span class="sxs-lookup"><span data-stu-id="45ad2-140">Make performance-related requests (for tasks that can't be completed through self-service).</span></span>
- <span data-ttu-id="45ad2-141">フライティング機能 (たとえば、顧客と仕入先マスターのデータ共有) を有効にします。</span><span class="sxs-lookup"><span data-stu-id="45ad2-141">Activate a flighting feature (for example, customer and vendor master data sharing).</span></span>
- <span data-ttu-id="45ad2-142">運用環境のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-142">Resize a production environment.</span></span> <span data-ttu-id="45ad2-143">(最初に、Microsoft Dynamics Lifecycle Services \[LCS \] のサブスクリプション見積りツールで新しい使用状況プロファイルを更新およびアップロードする必要があります。)</span><span class="sxs-lookup"><span data-stu-id="45ad2-143">(You must first update and upload a new usage profile in the subscription estimator in Microsoft Dynamics Lifecycle Services \[LCS\].)</span></span>
- <span data-ttu-id="45ad2-144">同じテナントに追加の LCS プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-144">Create an additional LCS project in the same tenant.</span></span>
- <span data-ttu-id="45ad2-145">運用環境のテナントを移動します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-145">Move the tenant of production environments.</span></span>

## <a name="requesting-support"></a><span data-ttu-id="45ad2-146">サポートの依頼</span><span class="sxs-lookup"><span data-stu-id="45ad2-146">Requesting support</span></span>

<span data-ttu-id="45ad2-147">効果的なサポート プロセスを実行するには、明確なエスカレーション パスを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-147">An effective support process requires that a clear escalation path be defined.</span></span> <span data-ttu-id="45ad2-148">プロジェクト チーム (クライアントまたはパートナー) は環境テレメトリーの監視と読み取りを行なうことができ、また、必要な最初のトラブルシューティングに対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-148">Project teams (client or partner) should be able to monitor and read environment telemetry, and they should be capable of doing any initial troubleshooting that is required.</span></span>

<span data-ttu-id="45ad2-149">問題を明確に識別し、解決プロセスを明確に定義することにより、結果の有効性が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-149">A well-identified issue and a well-defined resolution process can make a difference in the effectiveness of the outcome.</span></span>

<span data-ttu-id="45ad2-150">有効なサポート要求には、次の詳細が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-150">An effective support request should include the following details:</span></span>

- <span data-ttu-id="45ad2-151">問題が発生した環境</span><span class="sxs-lookup"><span data-stu-id="45ad2-151">The environment where the issue occurs</span></span>
- <span data-ttu-id="45ad2-152">問題が識別されたプロセス</span><span class="sxs-lookup"><span data-stu-id="45ad2-152">The process that the issue was identified in</span></span>
- <span data-ttu-id="45ad2-153">問題が発生した場所を表示する再現可能な手順</span><span class="sxs-lookup"><span data-stu-id="45ad2-153">Reproducible steps to show where the issue occurred</span></span>
- <span data-ttu-id="45ad2-154">予想される結果と実際の結果</span><span class="sxs-lookup"><span data-stu-id="45ad2-154">The expected result and the actual result</span></span>
- <span data-ttu-id="45ad2-155">問題の事前調査</span><span class="sxs-lookup"><span data-stu-id="45ad2-155">Pre-investigation of the issue</span></span>
- <span data-ttu-id="45ad2-156">追加の要素 (エラー メッセージ、スクリーン ショット、セッション ID、追跡など)</span><span class="sxs-lookup"><span data-stu-id="45ad2-156">Additional elements (for example, the error message, screenshots, the session ID, and the trace)</span></span>

### <a name="high-severity-support-requests"></a><span data-ttu-id="45ad2-157">重要度の高いサポート要求</span><span class="sxs-lookup"><span data-stu-id="45ad2-157">High-severity support requests</span></span>

<span data-ttu-id="45ad2-158">重要度の高いサポート要求には、次の情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-158">A high-severity support request should include the following information:</span></span>

- <span data-ttu-id="45ad2-159">**ビジネスへの影響:** この問題はビジネス活動にどのような影響を及ぼすか?</span><span class="sxs-lookup"><span data-stu-id="45ad2-159">**Business impact:** How does the issue affect your business activities?</span></span>
- <span data-ttu-id="45ad2-160">**財務的影響:** この問題は財務レベルでビジネスにどのような影響を及ぼすか?</span><span class="sxs-lookup"><span data-stu-id="45ad2-160">**Financial impact:** How does the issue affect your business at a financial level?</span></span>

<span data-ttu-id="45ad2-161">レポートする前にそれぞれの問題を詳細に分析する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-161">A thorough analysis of each issue should be done before the issue is reported.</span></span> <span data-ttu-id="45ad2-162">サポート要求に詳細情報が含まれる場合や、使用可能なすべてのツールとテレメトリが使用されている場合は、インシデントの解決はより迅速になります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-162">The incident resolution will be much quicker if the support request includes detailed information, and if all available tools and telemetries have been used.</span></span> <span data-ttu-id="45ad2-163">サポート要求を送信する際に正しい情報をすべて含めることにより、問題を特定してレプリケートするために必要な前後の通信の量を減らします。</span><span class="sxs-lookup"><span data-stu-id="45ad2-163">By including all the correct information when you submit a support request, you reduce the amount of back-and-forth communication that is required to identify and replicate the issue.</span></span> <span data-ttu-id="45ad2-164">したがって、時間を大幅に節約できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-164">Therefore, you can save lots of time.</span></span>

<span data-ttu-id="45ad2-165">選択できる複数の[サポート計画](https://go.microsoft.com/fwlink/?LinkId=871952) があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-165">There are several [support plans](https://go.microsoft.com/fwlink/?LinkId=871952) to choose from.</span></span> <span data-ttu-id="45ad2-166">したがって、すべてのビジネスでは、そのニーズを満たす計画を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-166">Therefore, every business should be able to find a plan that meets its needs.</span></span>

<span data-ttu-id="45ad2-167">サポートを要求する前に、重要度の適切なレベルを選択することが重要です。</span><span class="sxs-lookup"><span data-stu-id="45ad2-167">Before you request support, it's important that you choose the correct level of severity.</span></span> <span data-ttu-id="45ad2-168">適切な重要度レベルを識別し、要求の最初の応答時間を見積もる方法の詳細については、[サポート概要](https://docs.microsoft.com/power-platform/admin/support-overview?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&amp;bc=/dynamics365/breadcrumb/toc.json#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request) および[業務停止のレポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45ad2-168">For information about how to identify the correct severity level and estimate the initial response time for your request, see [Support overview](https://docs.microsoft.com/power-platform/admin/support-overview?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&amp;bc=/dynamics365/breadcrumb/toc.json#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request) and [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span>

## <a name="monitoring-elements"></a><span data-ttu-id="45ad2-169">監視の要素</span><span class="sxs-lookup"><span data-stu-id="45ad2-169">Monitoring elements</span></span>

<span data-ttu-id="45ad2-170">LCS には、LCS プロジェクトの監視に使用できる統合されたツール セットがあります。</span><span class="sxs-lookup"><span data-stu-id="45ad2-170">LCS has an integrated set of tools that you can use to monitor LCS projects.</span></span>

### <a name="service-health-dashboard"></a><span data-ttu-id="45ad2-171">サービス ヘルス ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="45ad2-171">Service health dashboard</span></span>

<span data-ttu-id="45ad2-172">[サービス ヘルス ダッシュボード](https://portal.office.com/servicestatus) によって Office 365 サービスの正常性が示されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-172">The [Service health dashboard](https://portal.office.com/servicestatus) provides the health status for Office 365 services.</span></span>

<span data-ttu-id="45ad2-173">[Microsoft 365 管理センター](https://admin.microsoft.com) でサービスの正常性を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-173">You can also view the service health through the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="45ad2-174">**正常性** \> **サービスの正常性** に移動するか、または **ホーム** ダッシュボードの **サービスの正常性** カードを選択します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-174">Go to **Health** \> **Service health**, or select the **Service health** card on the **Home** dashboard.</span></span>

<span data-ttu-id="45ad2-175">既定では、**サービスの正常性** ページで **すべてのサービス** タブが選択されます。 </span><span class="sxs-lookup"><span data-stu-id="45ad2-175">By default, the **All services** tab is selected on the **Service health** page.</span></span> <span data-ttu-id="45ad2-176">すべてのサービスおよび現在の正常性の状態が示されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-176">It shows all services and their current health state.</span></span> <span data-ttu-id="45ad2-177">**ステータス** 列の記号と値は各サービスの状態を示します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-177">A symbol and a value in the **Status** column indicate the state of each service.</span></span>

<span data-ttu-id="45ad2-178">Microsoft 365 サービスの問題が発生しているのに、**サービスの正常性** ページに一覧表示されない場合、**問題の報告** を選択し、短いフォームに入力して Microsoft に通知します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-178">If you're experiencing an issue with a Microsoft 365 service, but it isn't listed on the **Service health** page, you can notify Microsoft by selecting **Report an issue** and completing a short form.</span></span>

<span data-ttu-id="45ad2-179">問題の報告は、問題および問題の広がり具合を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-179">The issue reporting will help to identify issues and how widespread they are.</span></span> <span data-ttu-id="45ad2-180">インシデントが識別された後、**サービスの正常性** の下のダッシュボードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-180">After incidents are identified, they will be shown on the dashboard under **service health**.</span></span>

<span data-ttu-id="45ad2-181">サイン アップして電子メール通信を受信することができます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-181">You can sign up to receive email communication.</span></span> <span data-ttu-id="45ad2-182">このようにして、テナント内で識別された問題とそのステータスの変更についての警告をすぐに受け取るようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-182">In this way, you can ensure that you're quickly alerted about issues that are identified in the tenant and their status change.</span></span>

### <a name="environment-monitoring"></a><span data-ttu-id="45ad2-183">環境の監視</span><span class="sxs-lookup"><span data-stu-id="45ad2-183">Environment monitoring</span></span>

<span data-ttu-id="45ad2-184">環境の監視とは、[LCS を経由した環境の正常性のトラブルシューティング](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/monitoring-diagnostics) と監視に役立つ一連のツールです。</span><span class="sxs-lookup"><span data-stu-id="45ad2-184">Environment monitoring is a set of tools that help you monitor and [troubleshoot the health of your environments through LCS](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/monitoring-diagnostics).</span></span>

<span data-ttu-id="45ad2-185">プロジェクトの特定の環境ページの **監視** セクションには、**環境監視ダッシュボード** に移動できる **環境の監視** リンクが含まれています 。</span><span class="sxs-lookup"><span data-stu-id="45ad2-185">On a specific environment page for a project, the **Monitoring** section includes a **Environment monitoring** link that will take you to the **Environment monitoring dashboard**.</span></span>

<span data-ttu-id="45ad2-186">次のサブセクションでは、使用可能なツールの一部について説明します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-186">The following subsections describe some of the tools that are available.</span></span>

#### <a name="overview"></a><span data-ttu-id="45ad2-187">概要</span><span class="sxs-lookup"><span data-stu-id="45ad2-187">Overview</span></span>

<span data-ttu-id="45ad2-188">**概要** セクションは、ほとんどの環境タイプで共通しています。</span><span class="sxs-lookup"><span data-stu-id="45ad2-188">The **Overview** section is common to most environment types.</span></span> <span data-ttu-id="45ad2-189">これにより、ユーザーの活動を追跡し、定義された期間中の活動による負荷を追跡するフィルター処理可能な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-189">It provides a filterable way to trace user activity and to trace load by activity during a defined period.</span></span>

#### <a name="activity"></a><span data-ttu-id="45ad2-190">活動</span><span class="sxs-lookup"><span data-stu-id="45ad2-190">Activity</span></span>

<span data-ttu-id="45ad2-191">**活動** タブでは、未加工のログをクエリできます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-191">The **Activity** tab lets you query raw logs.</span></span> <span data-ttu-id="45ad2-192">環境の監視に役立つ、最も一般的なイベントおよび指標に対する定義済みのクエリが提供されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-192">It provides predefined queries for the most common events and metrics to help you monitor your environment.</span></span> <span data-ttu-id="45ad2-193">使用可能な定義済みクエリの一部の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-193">Here are some examples of the predefined queries that are available:</span></span>

- <span data-ttu-id="45ad2-194">速度の遅いクエリ</span><span class="sxs-lookup"><span data-stu-id="45ad2-194">Slow queries</span></span>
- <span data-ttu-id="45ad2-195">デッドロック</span><span class="sxs-lookup"><span data-stu-id="45ad2-195">Deadlocks</span></span>
- <span data-ttu-id="45ad2-196">クラッシュ</span><span class="sxs-lookup"><span data-stu-id="45ad2-196">Crashes</span></span>
- <span data-ttu-id="45ad2-197">財務諸表の問題</span><span class="sxs-lookup"><span data-stu-id="45ad2-197">Financial reporting issues</span></span>
- <span data-ttu-id="45ad2-198">バッチ調整</span><span class="sxs-lookup"><span data-stu-id="45ad2-198">Batch throttle</span></span>
- <span data-ttu-id="45ad2-199">別個のユーザー セッション</span><span class="sxs-lookup"><span data-stu-id="45ad2-199">Distinct user sessions</span></span>

<span data-ttu-id="45ad2-200">さらに、独自のカスタム フィルターを追加し、分析のためにログをコンマ区切り値 (CSV) ファイルにエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-200">Additionally, you can add your own custom filters and export the logs to a comma-separated values (CSV) file for analysis.</span></span>

![活動タブ](./media/activity.png)

#### <a name="health-metrics"></a><span data-ttu-id="45ad2-202">正常性指標</span><span class="sxs-lookup"><span data-stu-id="45ad2-202">Health Metrics</span></span>

<span data-ttu-id="45ad2-203">**正常性指標** ダッシュボードでは、インスタンス (AOS または バッチ AOS) および時間枠でフィルターされた一連のライン チャートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-203">The **Health Metrics** dashboard provides a series of line charts that are filtered by instance (AOS or Batch AOS) and time frame.</span></span> <span data-ttu-id="45ad2-204">**AOS** タブでは、SQL の実行を監視できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-204">On the **AOS** tab, you can observe SQL execution.</span></span> <span data-ttu-id="45ad2-205">**システム** タブでは、システム メモリと CPU 使用率を時間の経過とともに監視できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-205">On the **System** tab, you can observe system memory and CPU utilization over time.</span></span> <span data-ttu-id="45ad2-206">このツールを使用すると、動作の変更を簡単に識別できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-206">This tool lets you easily identify behavioral changes.</span></span> <span data-ttu-id="45ad2-207">したがって、時間の経過に伴う問題やソリューション内の変更の影響を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-207">Therefore, it can help you trace issues over time and the impact of changes in the solution.</span></span>

#### <a name="sql-insights"></a><span data-ttu-id="45ad2-208">SQL インサイト</span><span class="sxs-lookup"><span data-stu-id="45ad2-208">SQL Insights</span></span>

<span data-ttu-id="45ad2-209">SQL インサイトは、パフォーマンス分析を有効にする高度な SQL トラブルシューティング ツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-209">SQL Insights provides advanced SQL troubleshooting tools that enable performance analysis.</span></span> <span data-ttu-id="45ad2-210">これらのツールの一部は、Microsoft Dynamics AX 2012 での SQL トラブルシューティングに使用されていた DynPerf ツールと類似しています。</span><span class="sxs-lookup"><span data-stu-id="45ad2-210">Some of these tools resemble the DynPerf tool that was used for SQL troubleshooting in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="45ad2-211">詳細については、 [Lifecycle Services (LCS) 内のツールを使用したパフォーマンスのトラブルシューティング](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/performancetroubleshooting) および[パフォーマンスのトラブルシューティング ツール TechTalk](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-performance-troubleshooting-tools-for-dynamics-365-12-14-18) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45ad2-211">For a more detailed explanation, see [Performance troubleshooting using tools in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/performancetroubleshooting) and watch the [Performance troubleshooting tools TechTalk](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-performance-troubleshooting-tools-for-dynamics-365-12-14-18).</span></span>

<span data-ttu-id="45ad2-212">SQL インサイトは、要求されるパフォーマンス測定方法を収集する信頼性の高い方法です。</span><span class="sxs-lookup"><span data-stu-id="45ad2-212">SQL Insights is a reliable way to collect performance metrics on demand.</span></span> <span data-ttu-id="45ad2-213">これにより、顧客やパートナーは、サンドボックスまたは生産環境での問題を軽減するために使用できる事前定義された一連のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-213">It lets customers and partners run a predefined set of actions that can be used to mitigate issues in a sandbox or production environment.</span></span> <span data-ttu-id="45ad2-214">これは直接 SQL Server をクエリするため、ほぼリアルタイムでクエリ ストア指標が取得されます。</span><span class="sxs-lookup"><span data-stu-id="45ad2-214">Because it queries SQL Server directly, you get query store metrics in near real time.</span></span>

<span data-ttu-id="45ad2-215">環境を監視することは重要ですが、常に監視している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="45ad2-215">Although it's important that you monitor your environments, you don't have to be on constant lookout.</span></span> <span data-ttu-id="45ad2-216">また Microsoft は、LCS 通知リストによって提供される電子メールを使用して、重要な問題や実行する必要のあるアクションについて警告し、実装自体に対する予防的ガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="45ad2-216">Microsoft also uses the emails that are provided in the LCS notification list to alert you about important issues and actions that you must take, and to provide preventive guidance for the implementation itself.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
