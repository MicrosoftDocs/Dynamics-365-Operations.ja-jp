---
title: 優先順位に基づく調整に関する FAQ
description: このトピックでは、OData の優先度ベースのスロットリングとカスタムサービスベースの統合に関するよくある質問 (FAQ) に対する回答を提供します。
author: hasaid
ms.date: 05/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: b1826ba6e151925983beab63a93e723d838060f1
ms.sourcegitcommit: 633d51834d7d29b745824924315a3898dc471f1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2021
ms.locfileid: "6075130"
---
# <a name="priority-based-throttling-faq"></a><span data-ttu-id="d385d-103">優先順位に基づく調整に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="d385d-103">Priority-based throttling FAQ</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d385d-104">このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合に関する [優先順位に基づく調整](priority-based-throttling.md) に関するよく寄せられる質問 (FAQ) に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="d385d-104">This topic provides answers to some frequently asked questions about [priority-based throttling](priority-based-throttling.md) for Open Data Protocol (OData) and custom service-based integrations.</span></span>

## <a name="how-do-i-access-the-data-management-yammer-group"></a><span data-ttu-id="d385d-105">Yammer グループのデータ管理にどのようにアクセスできますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-105">How do I access the Data management Yammer group?</span></span>
<span data-ttu-id="d385d-106">データ管理 Yammer グループにアクセスするには、[データ管理 Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417) に移動します。</span><span class="sxs-lookup"><span data-stu-id="d385d-106">To access the Data management Yammer group, go to [Data management Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417).</span></span>

## <a name="when-will-throttling-be-enabled-by-default"></a><span data-ttu-id="d385d-107">調整はいつ既定で有効になりますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-107">When will throttling be enabled by default?</span></span>
<span data-ttu-id="d385d-108">調整機能は、Finance 10.0.13 以降にプレビューされており、バージョン 10.0.19 から既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="d385d-108">The throttling feature has been in preview since Finance 10.0.13 and will be enabled by default starting in version 10.0.19.</span></span> <span data-ttu-id="d385d-109">OData およびカスタム サービス リクエストの優先順位を設定することにより、環境に手動で調整をトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="d385d-109">You can manually trigger throttling in your environment by setting the priority for your OData and Custom service requests.</span></span> <span data-ttu-id="d385d-110">ただし、Finance 10.0.19 のリリース以降、優先順位を設定していなくても、調整は自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="d385d-110">However, starting with the release of Finance 10.0.19, throttling will be automatically enabled even if you haven't set priorities.</span></span>

<span data-ttu-id="d385d-111">Finance バージョン 10.0.19 は、2021 年 4 月後半にプレリリースされる予定で、通常は 2021 年 6 月に一般的に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="d385d-111">Finance version 10.0.19 will be available for pre-release in late April 2021 and will be generally available in June 2021.</span></span>

## <a name="will-a-retry-request-receive-preferential-treatment-over-a-new-request"></a><span data-ttu-id="d385d-112">再試行要求は新規要求より優先処理されますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-112">Will a retry request receive preferential treatment over a new request?</span></span>
<span data-ttu-id="d385d-113">いいえ。</span><span class="sxs-lookup"><span data-stu-id="d385d-113">No.</span></span>

## <a name="will-my-environment-be-subject-to-any-api-limits"></a><span data-ttu-id="d385d-114">私の環境は API の制限対象になりますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-114">Will my environment be subject to any API limits?</span></span>
<span data-ttu-id="d385d-115">いいえ。</span><span class="sxs-lookup"><span data-stu-id="d385d-115">No.</span></span> <span data-ttu-id="d385d-116">現時点では、環境は API の制限対象ではありません。</span><span class="sxs-lookup"><span data-stu-id="d385d-116">At this time, environments are not subject to any API limits.</span></span> 

<span data-ttu-id="d385d-117">環境全体にわたるワークロードの影響を評価するために、テレメトリ データが収集されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-117">Telemetry data is collected to assess the impact of the workloads across environments.</span></span> <span data-ttu-id="d385d-118">このデータは、使用状況に基づく制限の導入のロードマップを定義する場合に、API のベースライン制限を確立するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d385d-118">This data helps establish baseline API limits as we define a roadmap for introducing usage-based limits.</span></span>

## <a name="is-there-a-report-that-determines-when-throttling-might-occur"></a><span data-ttu-id="d385d-119">調整が発生する時を決定するレポートがありますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-119">Is there a report that determines when throttling might occur?</span></span>
<span data-ttu-id="d385d-120">はい。</span><span class="sxs-lookup"><span data-stu-id="d385d-120">Yes.</span></span> <span data-ttu-id="d385d-121">レポートは利用可能で、LCS の **環境の監視** ページの **未加工ログ** からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d385d-121">A report is available and can be accessed through the **Raw logs** on the **Environment monitoring** page in LCS.</span></span> <span data-ttu-id="d385d-122">このビューに一覧表示される要求は、Finance バージョン 10.0.19 以降、この機能が既定でオンになっている場合に調整される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d385d-122">The requests that are listed in this view are likely to be throttled when this feature is turned on by default starting in Finance version 10.0.19.</span></span>

## <a name="will-throttling-affect-the-data-importexport-framework-dixf-and-batch"></a><span data-ttu-id="d385d-123">調整はデータのインポート/エクスポート フレームワーク (DIXF) とバッチに影響しますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-123">Will throttling affect the Data Import/Export Framework (DIXF) and batch?</span></span>
<span data-ttu-id="d385d-124">No.</span><span class="sxs-lookup"><span data-stu-id="d385d-124">No.</span></span> <span data-ttu-id="d385d-125">調整は、Odata と カスタム サービス統合のためです。</span><span class="sxs-lookup"><span data-stu-id="d385d-125">Throttling is only for OData and custom service integrations.</span></span>

## <a name="is-throttling-available-for-on-premises-environments"></a><span data-ttu-id="d385d-126">オンプレミス環境で調整を使用できますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-126">Is throttling available for on-premises environments?</span></span>
<span data-ttu-id="d385d-127">いいえ。</span><span class="sxs-lookup"><span data-stu-id="d385d-127">No.</span></span> <span data-ttu-id="d385d-128">オンプレミス環境で調整は使用できません。</span><span class="sxs-lookup"><span data-stu-id="d385d-128">Throttling is not available for on-premises environments.</span></span>

## <a name="in-preview-will-my-requests-be-throttled-if-priorities-arent-configured"></a><span data-ttu-id="d385d-129">プレビューで、優先順位が構成されない場合、自分の要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-129">In Preview, will my requests be throttled if priorities aren't configured?</span></span>
<span data-ttu-id="d385d-130">いいえ、なぜならテレメトリのみが有効だからです。</span><span class="sxs-lookup"><span data-stu-id="d385d-130">No, because only the telemetry is available.</span></span> <span data-ttu-id="d385d-131">実際の調整は、優先順位を構成した場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-131">The actual throttling occurs if you configure priorities.</span></span> <span data-ttu-id="d385d-132">プレビュー期間中は、**非実稼働** 環境でこのアプローチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d385d-132">We recommend that you use this approach in **non-production** environments during the Preview period.</span></span>

## <a name="can-throttling-be-enabled-on-dev-boxes"></a><span data-ttu-id="d385d-133">開発ボックスで調整は有効にできますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-133">Can throttling be enabled on dev boxes?</span></span>
<span data-ttu-id="d385d-134">いいえ。</span><span class="sxs-lookup"><span data-stu-id="d385d-134">No.</span></span> <span data-ttu-id="d385d-135">優先順位を設定して、調整をトリガーできるのは、サンドボックス環境か実稼働環境のみです。</span><span class="sxs-lookup"><span data-stu-id="d385d-135">You can only set priority and trigger throttling in sandbox or production environments.</span></span>

## <a name="what-happens-to-requests-if-the-user-didnt-retry-a-throttled-request"></a><span data-ttu-id="d385d-136">ユーザーが調整された要求を再試行しなかった場合は、要求にどのような影響がありますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-136">What happens to requests if the user didn't retry a throttled request?</span></span>
<span data-ttu-id="d385d-137">現時点では、429 エラーが発生して要求が再度実行されない場合、要求は処理されません。</span><span class="sxs-lookup"><span data-stu-id="d385d-137">Currently, if a request isn't retried when a 429 error is received, the request won't be processed.</span></span>

## <a name="will-historic-throttling-information-be-used-to-advise-me-when-i-resize-environments"></a><span data-ttu-id="d385d-138">環境のサイズを変更した場合、履歴の調整情報を使用して通知することができますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-138">Will historic throttling information be used to advise me when I resize environments?</span></span>
<span data-ttu-id="d385d-139">はい。</span><span class="sxs-lookup"><span data-stu-id="d385d-139">Yes.</span></span> <span data-ttu-id="d385d-140">1 か月間、情報を Excel にエクスポートして、より詳細な分析やアーカイブを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d385d-140">For one month, you can export the information to Excel for more analysis and archiving.</span></span>

## <a name="is-throttling-functionality-version-specific-if-it-is-which-version-is-it-available-in"></a><span data-ttu-id="d385d-141">調整機能はバージョン固有ですか?</span><span class="sxs-lookup"><span data-stu-id="d385d-141">Is throttling functionality version-specific?</span></span> <span data-ttu-id="d385d-142">その場合、どのバージョンで利用できますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-142">If it is, which version is it available in?</span></span>
<span data-ttu-id="d385d-143">優先順位に基づく調整は、Finance and Operations アプリのバージョン 10.0.13 以降のプレビューでご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="d385d-143">Priority-based throttling will be available in Preview starting with the version 10.0.13 of Finance and Operations apps.</span></span>

## <a name="are-there-plans-to-provide-an-option-for-the-priority-mapping-grid-entry"></a><span data-ttu-id="d385d-144">優先順位マッピング グリッドのエントリにオプションを用意する計画はありますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-144">Are there plans to provide an option for the Priority mapping grid entry?</span></span>
<span data-ttu-id="d385d-145">この要求は、今後のリリースで考慮されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-145">Microsoft will consider this request in a future release.</span></span>

## <a name="will-the-requests-of-my-interactive-users-be-throttled"></a><span data-ttu-id="d385d-146">対話型ユーザーの要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-146">Will the requests of my interactive users be throttled?</span></span>
<span data-ttu-id="d385d-147">No.</span><span class="sxs-lookup"><span data-stu-id="d385d-147">No.</span></span> <span data-ttu-id="d385d-148">対話型 (オンライン) ユーザーの要求には影響しません。</span><span class="sxs-lookup"><span data-stu-id="d385d-148">There will be no impact on the requests of interactive (online) users.</span></span>

## <a name="if-i-experience-a-performance-issue-in-dynamics-365-finance-while-a-page-is-being-loaded-or-a-business-document-is-being-processed-how-does-that-performance-issue-differ-from-throttling"></a><span data-ttu-id="d385d-149">ページが読み込まれているとき、またはビジネス ドキュメントが処理されているときに Dynamics 365 Finance でパフォーマンスの問題が発生した場合、そのパフォーマンスの問題は、調整とどのように異なりますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-149">If I experience a performance issue in Dynamics 365 Finance while a page is being loaded or a business document is being processed, how does that performance issue differ from throttling?</span></span>
<span data-ttu-id="d385d-150">調整は、リソースの制約がある場合、システムを正常に管理する助けになります。</span><span class="sxs-lookup"><span data-stu-id="d385d-150">Throttling helps maintain a healthy system when there is a resource constraint.</span></span> <span data-ttu-id="d385d-151">ページ アクションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="d385d-151">It won't affect any page actions.</span></span>

## <a name="how-can-i-determine-the-wait-time-before-i-retry-a-throttled-request"></a><span data-ttu-id="d385d-152">調整された要求を再試行するまでの待機時間をどのようにして決定できますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-152">How can I determine the wait time before I retry a throttled request?</span></span>
<span data-ttu-id="d385d-153">要求が調整された場合、再試行ロジックで時間を含めた回答ヘッダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d385d-153">When a request is throttled, the response header includes a time that will be used in retry logic.</span></span> <span data-ttu-id="d385d-154">**再試行** HTTP ヘッダーを使用すると、秒単位で提供される値をでフェッチできます。</span><span class="sxs-lookup"><span data-stu-id="d385d-154">You can use the **Retry-After** HTTP header to fetch the value that will be provided in seconds.</span></span> <span data-ttu-id="d385d-155">たとえば、**再試行: 60**。</span><span class="sxs-lookup"><span data-stu-id="d385d-155">For example, **Retry-After: 60**.</span></span>

## <a name="what-is-the-message-that-is-shown-as-part-of-the-429-http-response"></a><span data-ttu-id="d385d-156">429 HTTP 応答の一部として表示されるメッセージは何ですか?</span><span class="sxs-lookup"><span data-stu-id="d385d-156">What is the message that is shown as part of the 429 HTTP response?</span></span>
<span data-ttu-id="d385d-157">次のメッセージが表示されます。「システムのリソース稼働率が高いため、現時点ではこのリクエストを処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="d385d-157">You will receive the message, "This request could not be processed at this time due to system experiencing high resource utilization.</span></span> <span data-ttu-id="d385d-158">要求を {0} 秒後に再試行します」。</span><span class="sxs-lookup"><span data-stu-id="d385d-158">Retry the request after {0} seconds".</span></span>
<span data-ttu-id="d385d-159">**{0}** には，動的に計算された再試行サイクル間隔があります。</span><span class="sxs-lookup"><span data-stu-id="d385d-159">Where **{0}** will have the dynamically calculated retry-after time interval.</span></span>

## <a name="does-throttling-apply-to-microsoft-services"></a><span data-ttu-id="d385d-160">調整は Microsoft サービスに適用されますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-160">Does throttling apply to Microsoft services?</span></span>
<span data-ttu-id="d385d-161">最初は除外される Microsoft サービスは次のサービスであり、調整はそのサービスには適用されません。</span><span class="sxs-lookup"><span data-stu-id="d385d-161">The following Microsoft services are initially exempt, and throttling doesn't apply to them:</span></span> 

   - <span data-ttu-id="d385d-162">ドキュメント回覧エージェント (DRA)</span><span class="sxs-lookup"><span data-stu-id="d385d-162">Document Routing Agent (DRA)</span></span>
   - <span data-ttu-id="d385d-163">倉庫モバイル (WHSMobile)</span><span class="sxs-lookup"><span data-stu-id="d385d-163">Warehouse Mobile (WHSMobile)</span></span>
   - <span data-ttu-id="d385d-164">RetailAPI</span><span class="sxs-lookup"><span data-stu-id="d385d-164">RetailAPI</span></span>
   - <span data-ttu-id="d385d-165">Office 統合</span><span class="sxs-lookup"><span data-stu-id="d385d-165">Office Integration</span></span>
   - <span data-ttu-id="d385d-166">データのインポート/エクスポート フレームワーク (DIXF)</span><span class="sxs-lookup"><span data-stu-id="d385d-166">Data Import/Export Framework (DIXF)</span></span>
   - <span data-ttu-id="d385d-167">データ インテグレーター</span><span class="sxs-lookup"><span data-stu-id="d385d-167">Data Integrator</span></span>
   - <span data-ttu-id="d385d-168">二重書き込み</span><span class="sxs-lookup"><span data-stu-id="d385d-168">Dual-write</span></span>
   - <span data-ttu-id="d385d-169">Finance and Operations アプリ- Power Platform 統合 (仮想エンティティ)</span><span class="sxs-lookup"><span data-stu-id="d385d-169">Finance and Operations apps - Power Platform Integration (Virtual Entities)</span></span>
   - <span data-ttu-id="d385d-170">Finance and Operations アプリケーション コネクタ</span><span class="sxs-lookup"><span data-stu-id="d385d-170">Finance and Operations apps Connector</span></span> 

<span data-ttu-id="d385d-171">これらのサービスは除外されますが、テレメトリはこれらのサービスがシステム全体の正常性に与える影響とパフォーマンスで収集されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-171">Though these services are exempt, telemetry is collected on the performance and impact of these services on the overall system health.</span></span> 

<span data-ttu-id="d385d-172">除外サービスの所有者は、2021 年度末までに 429 のハンドラーを実装することを優先しています。</span><span class="sxs-lookup"><span data-stu-id="d385d-172">The owners of the exempt services are prioritizing the implementation of 429 handlers by the end of 2021.</span></span> <span data-ttu-id="d385d-173">その時点で、サービスはもはや除外されず、調整が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-173">At that time, the services will no longer be exempt and throttling will apply.</span></span> <span data-ttu-id="d385d-174">これらの変更に先立って通知がなされ、ドキュメントが更新されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-174">Notification will be provided ahead of these changes, and the documentation will be updated.</span></span>

<span data-ttu-id="d385d-175">これらのサービスが独自のハンドラーを実装している場合でも、クライアント側の処理をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d385d-175">Even if these services implement their own handlers, we still recommended that you have client-side handling.</span></span> <span data-ttu-id="d385d-176">*再試行* ロジックを含む 429 のハンドラーの実装を検討してください。</span><span class="sxs-lookup"><span data-stu-id="d385d-176">Consider implementing the 429 handler with *retry-after* logic.</span></span>

## <a name="is-it-recommended-to-use-a-dedicated-integration-account-instead-of-just-the-generic-admin-user-account"></a><span data-ttu-id="d385d-177">汎用管理者ユーザー アカウントの代わりに、専用の統合アカウントを使用することが勧められていますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-177">Is it recommended to use a dedicated integration account instead of just the generic admin user account?</span></span>
<span data-ttu-id="d385d-178">はい、この方法を強く推奨します。</span><span class="sxs-lookup"><span data-stu-id="d385d-178">Yes, we strongly recommend this approach.</span></span> <span data-ttu-id="d385d-179">これらのサービス保護設定はユーザー固有の値に対して設定されているため、統合のほとんどまたはすべてに対して同じユーザー アカウントを使用すると、統合のニーズに対して相対的な優先順位を割り当てる機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="d385d-179">As these service protection settings are set up for user-specific values, using the same user account for most or all of your integration will limit your ability to assign relative priorities across your integration needs.</span></span> <span data-ttu-id="d385d-180">さらに、同じユーザー アカウントを使用すると、そのユーザー アカウントから発信されたすべての統合リクエストは調整の対象になります。</span><span class="sxs-lookup"><span data-stu-id="d385d-180">Further, if the same user account is used, all integration requests that originate from that user account will be subjected to throttling.</span></span>

## <a name="does-throttling-depend-on-the-tier-that-my-environment-is-running-on"></a><span data-ttu-id="d385d-181">調整は、自分の環境で実行している層によって異なりますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-181">Does throttling depend on the tier that my environment is running on?</span></span>
<span data-ttu-id="d385d-182">初期のリリースでは、いいえです。</span><span class="sxs-lookup"><span data-stu-id="d385d-182">In the initial release, no.</span></span> <span data-ttu-id="d385d-183">調整は、各環境の使用可能なリソースに基づき、しきい値を計算します。</span><span class="sxs-lookup"><span data-stu-id="d385d-183">Throttling will calculate its threshold based on the resources that are available for each environment.</span></span>

## <a name="is-throttling-functionality-legal-entityspecific"></a><span data-ttu-id="d385d-184">調整機能は法人固有のものですか?</span><span class="sxs-lookup"><span data-stu-id="d385d-184">Is throttling functionality legal entity–specific?</span></span>
<span data-ttu-id="d385d-185">No.</span><span class="sxs-lookup"><span data-stu-id="d385d-185">No.</span></span>

## <a name="does-throttling-affect-bring-your-own-database-byod-export"></a><span data-ttu-id="d385d-186">調整は、自分のデータベースの持ち込み (BYOD) エクスポートに影響を与えますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-186">Does throttling affect bring your own database (BYOD) export?</span></span>
<span data-ttu-id="d385d-187">No.</span><span class="sxs-lookup"><span data-stu-id="d385d-187">No.</span></span>

## <a name="will-throttling-monitoring-be-available-in-application-insights"></a><span data-ttu-id="d385d-188">調整監視は Application Insights で使用できるようになりますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-188">Will throttling monitoring be available in Application Insights?</span></span>
<span data-ttu-id="d385d-189">将来、監視は使用可能な任意のツールにオンボーディングされます。</span><span class="sxs-lookup"><span data-stu-id="d385d-189">Monitoring will be onboarded to any available tool in the future.</span></span>

## <a name="if-a-production-environment-regularly-runs-out-of-resources-will-microsoft-have-to-resize-it"></a><span data-ttu-id="d385d-190">運用環境が定期的にリソースを使い果たす場合、Microsoft はサイズ変更をする必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-190">If a production environment regularly runs out of resources, will Microsoft have to resize it?</span></span>
<span data-ttu-id="d385d-191">はい。</span><span class="sxs-lookup"><span data-stu-id="d385d-191">Yes.</span></span> <span data-ttu-id="d385d-192">サイズ変更見積もりも再検証され、アップロードされます。</span><span class="sxs-lookup"><span data-stu-id="d385d-192">Sizing estimate will also have to be revalidated and uploaded.</span></span>

## <a name="after-april-2021-will-the-system-be-able-to-override-priority-based-throttling"></a><span data-ttu-id="d385d-193">2021 年 4 月以降、システムは優先順位に基づく調整を上書きできますか?</span><span class="sxs-lookup"><span data-stu-id="d385d-193">After April 2021, will the system be able to override priority-based throttling?</span></span>
<span data-ttu-id="d385d-194">システムは、2021 年 4 月以降優先順位が構成されない場合、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d385d-194">The system will use default values if no priorities are configured after April 2021.</span></span>

## <a name="can-the-throttling-engine-be-configured-thresholds"></a><span data-ttu-id="d385d-195">調整エンジンは構成できますか (しきい値)?</span><span class="sxs-lookup"><span data-stu-id="d385d-195">Can the throttling engine be configured (thresholds)?</span></span>
<span data-ttu-id="d385d-196">No.</span><span class="sxs-lookup"><span data-stu-id="d385d-196">No.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
