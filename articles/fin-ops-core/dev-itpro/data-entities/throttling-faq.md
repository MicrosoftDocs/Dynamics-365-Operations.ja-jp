---
title: 優先順位に基づく調整に関する FAQ
description: このトピックでは、OData の優先度ベースのスロットリングとカスタムサービスベースの統合に関するよくある質問 (FAQ) に対する回答を提供します。
author: hasaid
ms.date: 04/20/2021
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
ms.openlocfilehash: f318d6854648325b6ca9a997da47c82f92b76976
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935593"
---
# <a name="priority-based-throttling-faq"></a><span data-ttu-id="84179-103">優先順位に基づく調整に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="84179-103">Priority-based throttling FAQ</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="84179-104">このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合に関する [優先順位に基づく調整](priority-based-throttling.md) に関するよく寄せられる質問 (FAQ) に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="84179-104">This topic provides answers to some frequently asked questions about [priority-based throttling](priority-based-throttling.md) for Open Data Protocol (OData) and custom service-based integrations.</span></span>

## <a name="how-do-i-access-the-data-management-yammer-group"></a><span data-ttu-id="84179-105">Yammer グループのデータ管理にどのようにアクセスできますか?</span><span class="sxs-lookup"><span data-stu-id="84179-105">How do I access the Data management Yammer group?</span></span>
<span data-ttu-id="84179-106">データ管理 Yammer グループにアクセスするには、[データ管理 Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417) に移動します。</span><span class="sxs-lookup"><span data-stu-id="84179-106">To access the Data management Yammer group, go to [Data management Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417).</span></span>

## <a name="when-will-throttling-be-enabled-by-default"></a><span data-ttu-id="84179-107">調整はいつ既定で有効になりますか?</span><span class="sxs-lookup"><span data-stu-id="84179-107">When will throttling be enabled by default?</span></span>
<span data-ttu-id="84179-108">調整機能は、Finance 10.0.13 以降にプレビューされており、バージョン 10.0.19 から既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="84179-108">The throttling feature has been in preview since Finance 10.0.13 and will be enabled by default starting in version 10.0.19.</span></span> <span data-ttu-id="84179-109">OData およびカスタム サービス リクエストの優先順位を設定することにより、環境に手動で調整をトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="84179-109">You can manually trigger throttling in your environment by setting the priority for your OData and Custom service requests.</span></span> <span data-ttu-id="84179-110">ただし、Finance 10.0.19 のリリース以降、優先順位を設定していなくても、調整は自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="84179-110">However, starting with the release of Finance 10.0.19, throttling will be automatically enabled even if you haven't set priorities.</span></span>

<span data-ttu-id="84179-111">Finance バージョン 10.0.19 は、2021 年 4 月後半にプレリリースされる予定で、通常は 2021 年 6 月に一般的に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="84179-111">Finance version 10.0.19 will be available for pre-release in late April 2021 and will be generally available in June 2021.</span></span>

## <a name="will-a-retry-request-receive-preferential-treatment-over-a-new-request"></a><span data-ttu-id="84179-112">再試行要求は新規要求より優先処理されますか?</span><span class="sxs-lookup"><span data-stu-id="84179-112">Will a retry request receive preferential treatment over a new request?</span></span>
<span data-ttu-id="84179-113">いいえ。</span><span class="sxs-lookup"><span data-stu-id="84179-113">No.</span></span>

## <a name="will-my-environment-be-subjected-to-any-api-limits"></a><span data-ttu-id="84179-114">私の環境は API の制限対象になりますか?</span><span class="sxs-lookup"><span data-stu-id="84179-114">Will my environment be subjected to any API limits?</span></span>
<span data-ttu-id="84179-115">いいえ。</span><span class="sxs-lookup"><span data-stu-id="84179-115">No.</span></span> <span data-ttu-id="84179-116">現時点では、環境は API の制限対象ではありません。</span><span class="sxs-lookup"><span data-stu-id="84179-116">At this time, environments aren't subject to any API limits.</span></span> 

## <a name="is-there-a-report-that-determines-when-throttling-might-occur"></a><span data-ttu-id="84179-117">調整が発生する時を決定するレポートがありますか?</span><span class="sxs-lookup"><span data-stu-id="84179-117">Is there a report that determines when throttling might occur?</span></span>
<span data-ttu-id="84179-118">はい。</span><span class="sxs-lookup"><span data-stu-id="84179-118">Yes.</span></span> <span data-ttu-id="84179-119">レポートは利用可能で、LCS の **環境の監視** ページの **未加工ログ** からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="84179-119">A report is available and can be accessed through the **Raw logs** on the **Environment monitoring** page in LCS.</span></span> <span data-ttu-id="84179-120">このビューに一覧表示される要求は、Finance バージョン 10.0.19 以降、この機能が既定でオンになっている場合に調整される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84179-120">The requests that are listed in this view are likely to be throttled when this feature is turned on by default starting in Finance version 10.0.19.</span></span>

## <a name="will-throttling-affect-the-data-importexport-framework-dixf-and-batch"></a><span data-ttu-id="84179-121">調整はデータのインポート/エクスポート フレームワーク (DIXF) とバッチに影響しますか?</span><span class="sxs-lookup"><span data-stu-id="84179-121">Will throttling affect the Data Import/Export Framework (DIXF) and batch?</span></span>
<span data-ttu-id="84179-122">No.</span><span class="sxs-lookup"><span data-stu-id="84179-122">No.</span></span> <span data-ttu-id="84179-123">調整は、Odata と カスタム サービス統合のためです。</span><span class="sxs-lookup"><span data-stu-id="84179-123">Throttling is only for OData and custom service integrations.</span></span>

## <a name="is-throttling-available-for-on-premises-environments"></a><span data-ttu-id="84179-124">オンプレミス環境で調整を使用できますか?</span><span class="sxs-lookup"><span data-stu-id="84179-124">Is throttling available for on-premises environments?</span></span>
<span data-ttu-id="84179-125">いいえ。</span><span class="sxs-lookup"><span data-stu-id="84179-125">No.</span></span> <span data-ttu-id="84179-126">オンプレミス環境で調整は使用できません。</span><span class="sxs-lookup"><span data-stu-id="84179-126">Throttling is not available for on-premises environments.</span></span>

## <a name="in-preview-will-my-requests-be-throttled-if-priorities-arent-configured"></a><span data-ttu-id="84179-127">プレビューで、優先順位が構成されない場合、自分の要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="84179-127">In Preview, will my requests be throttled if priorities aren't configured?</span></span>
<span data-ttu-id="84179-128">いいえ、なぜならテレメトリのみが有効だからです。</span><span class="sxs-lookup"><span data-stu-id="84179-128">No, because only the telemetry is available.</span></span> <span data-ttu-id="84179-129">実際の調整は、優先順位を構成した場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="84179-129">The actual throttling occurs if you configure priorities.</span></span> <span data-ttu-id="84179-130">プレビュー期間中は、**非実稼働** 環境でこのアプローチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="84179-130">We recommend that you use this approach in **non-production** environments during the Preview period.</span></span>

## <a name="can-throttling-be-enabled-on-dev-boxes"></a><span data-ttu-id="84179-131">開発ボックスで調整は有効にできますか?</span><span class="sxs-lookup"><span data-stu-id="84179-131">Can throttling be enabled on dev boxes?</span></span>
<span data-ttu-id="84179-132">いいえ。</span><span class="sxs-lookup"><span data-stu-id="84179-132">No.</span></span> <span data-ttu-id="84179-133">優先順位を設定して、調整をトリガーできるのは、サンドボックス環境か実稼働環境のみです。</span><span class="sxs-lookup"><span data-stu-id="84179-133">You can only set priority and trigger throttling in sandbox or production environments.</span></span>

## <a name="what-happens-to-requests-if-the-user-didnt-retry-a-throttled-request"></a><span data-ttu-id="84179-134">ユーザーが調整された要求を再試行しなかった場合は、要求にどのような影響がありますか?</span><span class="sxs-lookup"><span data-stu-id="84179-134">What happens to requests if the user didn't retry a throttled request?</span></span>
<span data-ttu-id="84179-135">現時点では、429 エラーが発生して要求が再度実行されない場合、要求は処理されません。</span><span class="sxs-lookup"><span data-stu-id="84179-135">Currently, if a request isn't retried when a 429 error is received, the request won't be processed.</span></span>

## <a name="will-historic-throttling-information-be-used-to-advise-me-when-i-resize-environments"></a><span data-ttu-id="84179-136">環境のサイズを変更した場合、履歴の調整情報を使用して通知することができますか?</span><span class="sxs-lookup"><span data-stu-id="84179-136">Will historic throttling information be used to advise me when I resize environments?</span></span>
<span data-ttu-id="84179-137">はい。</span><span class="sxs-lookup"><span data-stu-id="84179-137">Yes.</span></span> <span data-ttu-id="84179-138">1 か月間、情報を Excel にエクスポートして、より詳細な分析やアーカイブを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="84179-138">For one month, you can export the information to Excel for more analysis and archiving.</span></span>

## <a name="is-throttling-functionality-version-specific-if-it-is-which-version-is-it-available-in"></a><span data-ttu-id="84179-139">調整機能はバージョン固有ですか?</span><span class="sxs-lookup"><span data-stu-id="84179-139">Is throttling functionality version-specific?</span></span> <span data-ttu-id="84179-140">その場合、どのバージョンで利用できますか?</span><span class="sxs-lookup"><span data-stu-id="84179-140">If it is, which version is it available in?</span></span>
<span data-ttu-id="84179-141">優先順位に基づく調整は、Finance and Operations アプリのバージョン 10.0.13 以降のプレビューでご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="84179-141">Priority-based throttling will be available in Preview starting with the version 10.0.13 of Finance and Operations apps.</span></span>

## <a name="are-there-plans-to-provide-an-option-for-the-priority-mapping-grid-entry"></a><span data-ttu-id="84179-142">優先順位マッピング グリッドのエントリにオプションを用意する計画はありますか?</span><span class="sxs-lookup"><span data-stu-id="84179-142">Are there plans to provide an option for the Priority mapping grid entry?</span></span>
<span data-ttu-id="84179-143">この要求は、今後のリリースで考慮されます。</span><span class="sxs-lookup"><span data-stu-id="84179-143">Microsoft will consider this request in a future release.</span></span>

## <a name="will-the-requests-of-my-interactive-users-be-throttled"></a><span data-ttu-id="84179-144">対話型ユーザーの要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="84179-144">Will the requests of my interactive users be throttled?</span></span>
<span data-ttu-id="84179-145">No.</span><span class="sxs-lookup"><span data-stu-id="84179-145">No.</span></span> <span data-ttu-id="84179-146">対話型 (オンライン) ユーザーの要求には影響しません。</span><span class="sxs-lookup"><span data-stu-id="84179-146">There will be no impact on the requests of interactive (online) users.</span></span>

## <a name="if-i-experience-a-performance-issue-in-dynamics-365-finance-while-a-page-is-being-loaded-or-a-business-document-is-being-processed-how-does-that-performance-issue-differ-from-throttling"></a><span data-ttu-id="84179-147">ページが読み込まれているとき、またはビジネス ドキュメントが処理されているときに Dynamics 365 Finance でパフォーマンスの問題が発生した場合、そのパフォーマンスの問題は、調整とどのように異なりますか?</span><span class="sxs-lookup"><span data-stu-id="84179-147">If I experience a performance issue in Dynamics 365 Finance while a page is being loaded or a business document is being processed, how does that performance issue differ from throttling?</span></span>
<span data-ttu-id="84179-148">調整は、リソースの制約がある場合、システムを正常に管理する助けになります。</span><span class="sxs-lookup"><span data-stu-id="84179-148">Throttling helps maintain a healthy system when there is a resource constraint.</span></span> <span data-ttu-id="84179-149">ページ アクションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="84179-149">It won't affect any page actions.</span></span>

## <a name="how-can-i-determine-the-wait-time-before-i-retry-a-throttled-request"></a><span data-ttu-id="84179-150">調整された要求を再試行するまでの待機時間をどのようにして決定できますか?</span><span class="sxs-lookup"><span data-stu-id="84179-150">How can I determine the wait time before I retry a throttled request?</span></span>
<span data-ttu-id="84179-151">要求が調整された場合、再試行ロジックで時間を含めた回答ヘッダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="84179-151">When a request is throttled, the response header includes a time that will be used in retry logic.</span></span> <span data-ttu-id="84179-152">**再試行** HTTP ヘッダーを使用すると、秒単位で提供される値をでフェッチできます。</span><span class="sxs-lookup"><span data-stu-id="84179-152">You can use the **Retry-After** HTTP header to fetch the value that will be provided in seconds.</span></span> <span data-ttu-id="84179-153">たとえば、**再試行: 60**。</span><span class="sxs-lookup"><span data-stu-id="84179-153">For example, **Retry-After: 60**.</span></span>

## <a name="what-is-the-message-that-is-shown-as-part-of-the-429-http-response"></a><span data-ttu-id="84179-154">429 HTTP 応答の一部として表示されるメッセージは何ですか?</span><span class="sxs-lookup"><span data-stu-id="84179-154">What is the message that is shown as part of the 429 HTTP response?</span></span>
<span data-ttu-id="84179-155">次のメッセージが表示されます。「システムのリソース稼働率が高いため、現時点ではこのリクエストを処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="84179-155">You will receive the message, "This request could not be processed at this time due to system experiencing high resource utilization.</span></span> <span data-ttu-id="84179-156">要求を {0} 秒後に再試行します」。</span><span class="sxs-lookup"><span data-stu-id="84179-156">Retry the request after {0} seconds".</span></span>
<span data-ttu-id="84179-157">**{0}** には，動的に計算された再試行サイクル間隔があります。</span><span class="sxs-lookup"><span data-stu-id="84179-157">Where **{0}** will have the dynamically calculated retry-after time interval.</span></span>

## <a name="does-throttling-apply-to-internal-microsoft-services"></a><span data-ttu-id="84179-158">調整は Microsoft の内部サービスに適用されますか?</span><span class="sxs-lookup"><span data-stu-id="84179-158">Does throttling apply to internal Microsoft services?</span></span>
<span data-ttu-id="84179-159">DRA、WHSMobile、RetailAPI などの Microsoft の内部サービスは、現在、調整の対象から除外されています。</span><span class="sxs-lookup"><span data-stu-id="84179-159">Internal Microsoft services, such as DRA, WHSMobile, and RetailAPI are currently exempt from throttling.</span></span> <span data-ttu-id="84179-160">ただし、テレメトリは、システム全体の正常性に対するこれらのサービスのパフォーマンスについて収集されています。</span><span class="sxs-lookup"><span data-stu-id="84179-160">However, telemetry is being collected on the performance of these services on the overall system health.</span></span> <span data-ttu-id="84179-161">Microsoft は、これらの内部サービス チームと協力し、ある特定の時点で使用ベースの制限を確立します。</span><span class="sxs-lookup"><span data-stu-id="84179-161">Microsoft will work with each of these internal service teams to establish usage-based limits at some point.</span></span>

## <a name="is-it-recommended-to-use-a-dedicated-integration-account-instead-of-just-the-generic-admin-user-account"></a><span data-ttu-id="84179-162">汎用管理者ユーザー アカウントの代わりに、専用の統合アカウントを使用することが勧められていますか?</span><span class="sxs-lookup"><span data-stu-id="84179-162">Is it recommended to use a dedicated integration account instead of just the generic admin user account?</span></span>
<span data-ttu-id="84179-163">はい、この方法を強く推奨します。</span><span class="sxs-lookup"><span data-stu-id="84179-163">Yes, we strongly recommend this approach.</span></span> <span data-ttu-id="84179-164">これらのサービス保護設定はユーザー固有の値に対して設定されているため、統合のほとんどまたはすべてに対して同じユーザー アカウントを使用すると、統合のニーズに対して相対的な優先順位を割り当てる機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="84179-164">As these service protection settings are set up for user-specific values, using the same user account for most or all of your integration will limit your ability to assign relative priorities across your integration needs.</span></span> <span data-ttu-id="84179-165">さらに、同じユーザー アカウントを使用すると、そのユーザー アカウントから発信されたすべての統合リクエストは調整の対象になります。</span><span class="sxs-lookup"><span data-stu-id="84179-165">Further, if the same user account is used, all integration requests that originate from that user account will be subjected to throttling.</span></span>

## <a name="does-throttling-depend-on-the-tier-that-my-environment-is-running-on"></a><span data-ttu-id="84179-166">調整は、自分の環境で実行している層によって異なりますか?</span><span class="sxs-lookup"><span data-stu-id="84179-166">Does throttling depend on the tier that my environment is running on?</span></span>
<span data-ttu-id="84179-167">初期のリリースでは、いいえです。</span><span class="sxs-lookup"><span data-stu-id="84179-167">In the initial release, no.</span></span> <span data-ttu-id="84179-168">調整は、各環境の使用可能なリソースに基づき、しきい値を計算します。</span><span class="sxs-lookup"><span data-stu-id="84179-168">Throttling will calculate its threshold based on the resources that are available for each environment.</span></span>

## <a name="is-throttling-functionality-legal-entityspecific"></a><span data-ttu-id="84179-169">調整機能は法人固有のものですか?</span><span class="sxs-lookup"><span data-stu-id="84179-169">Is throttling functionality legal entity–specific?</span></span>
<span data-ttu-id="84179-170">No.</span><span class="sxs-lookup"><span data-stu-id="84179-170">No.</span></span>

## <a name="does-throttling-affect-bring-your-own-database-byod-export"></a><span data-ttu-id="84179-171">調整は、自分のデータベースの持ち込み (BYOD) エクスポートに影響を与えますか?</span><span class="sxs-lookup"><span data-stu-id="84179-171">Does throttling affect bring your own database (BYOD) export?</span></span>
<span data-ttu-id="84179-172">No.</span><span class="sxs-lookup"><span data-stu-id="84179-172">No.</span></span>

## <a name="will-throttling-monitoring-be-available-in-application-insights"></a><span data-ttu-id="84179-173">調整監視は Application Insights で使用できるようになりますか?</span><span class="sxs-lookup"><span data-stu-id="84179-173">Will throttling monitoring be available in Application Insights?</span></span>
<span data-ttu-id="84179-174">将来、監視は使用可能な任意のツールにオンボーディングされます。</span><span class="sxs-lookup"><span data-stu-id="84179-174">Monitoring will be onboarded to any available tool in the future.</span></span>

## <a name="if-a-production-environment-regularly-runs-out-of-resources-will-microsoft-have-to-resize-it"></a><span data-ttu-id="84179-175">運用環境が定期的にリソースを使い果たす場合、Microsoft はサイズ変更をする必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="84179-175">If a production environment regularly runs out of resources, will Microsoft have to resize it?</span></span>
<span data-ttu-id="84179-176">はい。</span><span class="sxs-lookup"><span data-stu-id="84179-176">Yes.</span></span> <span data-ttu-id="84179-177">サイズ変更見積もりも再検証され、アップロードされます。</span><span class="sxs-lookup"><span data-stu-id="84179-177">Sizing estimate will also have to be revalidated and uploaded.</span></span>

## <a name="after-april-2021-will-the-system-be-able-to-override-priority-based-throttling"></a><span data-ttu-id="84179-178">2021 年 4 月以降、システムは優先順位に基づく調整を上書きできますか?</span><span class="sxs-lookup"><span data-stu-id="84179-178">After April 2021, will the system be able to override priority-based throttling?</span></span>
<span data-ttu-id="84179-179">システムは、2021 年 4 月以降優先順位が構成されない場合、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="84179-179">The system will use default values if no priorities are configured after April 2021.</span></span>

## <a name="can-the-throttling-engine-be-configured-thresholds"></a><span data-ttu-id="84179-180">調整エンジンは構成できますか (しきい値)?</span><span class="sxs-lookup"><span data-stu-id="84179-180">Can the throttling engine be configured (thresholds)?</span></span>
<span data-ttu-id="84179-181">No.</span><span class="sxs-lookup"><span data-stu-id="84179-181">No.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
