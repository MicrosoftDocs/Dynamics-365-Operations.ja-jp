---
title: 優先順位に基づく調整に関する FAQ
description: このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合の優先順位に基づく調整に関するよく寄せられる質問 (FAQ) に対する回答を提供します。
author: hasaid
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 88dd0cb8f17e742819cf1c7374e3af39772ecc28
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885349"
---
# <a name="priority-based-throttling-faq"></a><span data-ttu-id="ee7bd-103">優先順位に基づく調整に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="ee7bd-103">Priority-based throttling FAQ</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ee7bd-104">このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合の[優先順位に基づく調整](priority-based-throttling.md) に関するよく寄せられる質問 (FAQ) に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-104">This topic provides answers to some frequently asked questions (FAQ) about [priority-based throttling](priority-based-throttling.md) for Open Data Protocol (OData) and custom service-based integrations.</span></span>

## <a name="how-do-i-access-the-data-management-yammer-group"></a><span data-ttu-id="ee7bd-105">Yammer グループのデータ管理にどのようにアクセスできますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-105">How do I access the Data management Yammer group?</span></span>

<span data-ttu-id="ee7bd-106">次のリンクを参照してください: [Yammer グループのデータ管理](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417)。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-106">Follow this link: [Data management Yammer group](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417).</span></span>

## <a name="will-a-retry-request-receive-preferential-treatment-over-a-new-request"></a><span data-ttu-id="ee7bd-107">再試行要求は新規要求より優先処理されますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-107">Will a retry request receive preferential treatment over a new request?</span></span>

<span data-ttu-id="ee7bd-108">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-108">No.</span></span>

## <a name="is-there-a-report-that-determines-when-throttling-might-occur"></a><span data-ttu-id="ee7bd-109">調整が発生する時を決定するレポートがありますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-109">Is there a report that determines when throttling might occur?</span></span>

<span data-ttu-id="ee7bd-110">はい。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-110">Yes.</span></span> <span data-ttu-id="ee7bd-111">レポートは提供され、Microsoft Dynamics Lifecycle Services (LCS) の環境監視ページ内の**未加工ログ**を通してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-111">A report will be provided and can be accessed through the **Raw logs** within environment monitoring page in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="will-throttling-affect-the-data-importexport-framework-dixf-and-batch"></a><span data-ttu-id="ee7bd-112">調整はデータのインポート/エクスポート フレームワーク (DIXF) とバッチに影響しますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-112">Will throttling affect the Data Import/Export Framework (DIXF) and batch?</span></span>

<span data-ttu-id="ee7bd-113">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-113">No.</span></span> <span data-ttu-id="ee7bd-114">調整は、Odata と カスタム サービス統合のためです。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-114">Throttling is only for OData and custom service integrations.</span></span>

## <a name="in-preview-will-my-requests-be-throttled-if-priorities-arent-configured"></a><span data-ttu-id="ee7bd-115">プレビューで、優先順位が構成されない場合、自分の要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-115">In Preview, will my requests be throttled if priorities aren't configured?</span></span>

<span data-ttu-id="ee7bd-116">いいえ、なぜならテレメトリのみが有効だからです。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-116">No, because only the telemetry is available.</span></span> <span data-ttu-id="ee7bd-117">実際の調整は、優先順位を構成した場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-117">The actual throttling occurs if you configure priorities.</span></span> <span data-ttu-id="ee7bd-118">プレビュー期間中は、**非実稼働**環境でこのアプローチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-118">We recommend that you use this approach in **non-production** environments during the Preview period.</span></span>

## <a name="what-happens-to-requests-if-the-user-didnt-retry-a-throttled-request"></a><span data-ttu-id="ee7bd-119">ユーザーが調整された要求を再試行しなかった場合は、要求にどのような影響がありますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-119">What happens to requests if the user didn't retry a throttled request?</span></span>

<span data-ttu-id="ee7bd-120">現時点では、429 エラーが発生して要求が再度実行されない場合、要求は処理されません。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-120">Currently, if a request isn't retried when a 429 error is received, the request won't be processed.</span></span>

## <a name="will-historic-throttling-information-be-used-to-advise-me-when-i-resize-environments"></a><span data-ttu-id="ee7bd-121">環境のサイズを変更した場合、履歴の調整情報を使用して通知することができますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-121">Will historic throttling information be used to advise me when I resize environments?</span></span>

<span data-ttu-id="ee7bd-122">はい。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-122">Yes.</span></span> <span data-ttu-id="ee7bd-123">1 か月間、情報を Excel にエクスポートして、より詳細な分析やアーカイブを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-123">For one month, you can export the information to Excel for more analysis and archiving.</span></span>

## <a name="is-throttling-functionality-version-specific-if-it-is-which-version-is-it-available-in"></a><span data-ttu-id="ee7bd-124">調整機能はバージョン固有ですか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-124">Is throttling functionality version-specific?</span></span> <span data-ttu-id="ee7bd-125">その場合、どのバージョンで利用できますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-125">If it is, which version is it available in?</span></span>

<span data-ttu-id="ee7bd-126">優先順位に基づく調整は、**Finance and Operations アプリ** リリース バージョン 10.0.13 のプラットフォーム更新プログラムからプレビューでご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-126">Priority-based throttling will be available in Preview starting with the **Platform updates for version 10.0.13 of Finance and Operations apps** release.</span></span>

## <a name="are-there-plans-to-provide-an-option-for-the-priority-mapping-grid-entry"></a><span data-ttu-id="ee7bd-127">優先順位マッピング グリッドのエントリにオプションを用意する計画はありますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-127">Are there plans to provide an option for the Priority mapping grid entry?</span></span>

<span data-ttu-id="ee7bd-128">この要求は、今後のリリースで考慮されます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-128">Microsoft will consider this request in a future release.</span></span>

## <a name="will-the-requests-of-my-interactive-users-be-throttled"></a><span data-ttu-id="ee7bd-129">対話型ユーザーの要求は調整されますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-129">Will the requests of my interactive users be throttled?</span></span>

<span data-ttu-id="ee7bd-130">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-130">No.</span></span> <span data-ttu-id="ee7bd-131">対話型 (オンライン) ユーザーの要求には影響しません。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-131">There will be no impact on the requests of interactive (online) users.</span></span>

## <a name="if-i-experience-a-performance-issue-in-dynamics-365-finance-while-a-page-is-being-loaded-or-a-business-document-is-being-processed-how-does-that-performance-issue-differ-from-throttling"></a><span data-ttu-id="ee7bd-132">ページが読み込まれているとき、またはビジネス ドキュメントが処理されているときに Dynamics 365 Finance でパフォーマンスの問題が発生した場合、そのパフォーマンスの問題は、調整とどのように異なりますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-132">If I experience a performance issue in Dynamics 365 Finance while a page is being loaded or a business document is being processed, how does that performance issue differ from throttling?</span></span>

<span data-ttu-id="ee7bd-133">調整は、リソースの制約がある場合、システムを正常に管理する助けになります。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-133">Throttling helps maintain a healthy system when there is a resource constraint.</span></span> <span data-ttu-id="ee7bd-134">ページ アクションには影響しません。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-134">It won't affect any page actions.</span></span>

## <a name="how-can-i-determine-the-wait-time-before-i-retry-a-throttled-request"></a><span data-ttu-id="ee7bd-135">調整された要求を再試行するまでの待機時間をどのようにして決定できますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-135">How can I determine the wait time before I retry a throttled request?</span></span>

<span data-ttu-id="ee7bd-136">要求が調整された場合、再試行ロジックで時間を含めた回答ヘッダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-136">When a request is throttled, the response header includes a time that will be used in retry logic.</span></span>

## <a name="do-you-recommend-that-i-use-a-dedicated-integration-account-instead-of-just-the-generic-admin-user-account"></a><span data-ttu-id="ee7bd-137">汎用管理者ユーザー アカウントの代わりに、専用の統合アカウントを使用することが勧められていますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-137">Do you recommend that I use a dedicated integration account instead of just the generic admin user account?</span></span>

<span data-ttu-id="ee7bd-138">はい、この方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-138">Yes, we recommend this approach.</span></span> <span data-ttu-id="ee7bd-139">ただし、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-139">However, it isn't mandatory.</span></span>

## <a name="does-throttling-depend-on-the-tier-that-my-environment-is-running-on"></a><span data-ttu-id="ee7bd-140">調整は、自分の環境で実行している層によって異なりますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-140">Does throttling depend on the tier that my environment is running on?</span></span>

<span data-ttu-id="ee7bd-141">初期のリリースでは、いいえです。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-141">In the initial release, no.</span></span> <span data-ttu-id="ee7bd-142">調整は、各環境の使用可能なリソースに基づき、しきい値を計算します。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-142">Throttling will calculate its threshold based on the resources that are available for each environment.</span></span>

## <a name="is-throttling-functionality-legal-entityspecific"></a><span data-ttu-id="ee7bd-143">調整機能は法人固有のものですか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-143">Is throttling functionality legal entity–specific?</span></span>

<span data-ttu-id="ee7bd-144">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-144">No.</span></span>

## <a name="does-throttling-affect-bring-your-own-database-byod-export"></a><span data-ttu-id="ee7bd-145">調整は、自分のデータベースの持ち込み (BYOD) エクスポートに影響を与えますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-145">Does throttling affect bring your own database (BYOD) export?</span></span>

<span data-ttu-id="ee7bd-146">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-146">No.</span></span>

## <a name="will-throttling-monitoring-be-available-in-application-insights"></a><span data-ttu-id="ee7bd-147">調整監視は Application Insights で使用できるようになりますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-147">Will throttling monitoring be available in Application Insights?</span></span>

<span data-ttu-id="ee7bd-148">将来、監視は使用可能な任意のツールにオンボーディングされます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-148">Monitoring will be onboarded to any available tool in the future.</span></span>

## <a name="if-a-production-environment-regularly-runs-out-of-resources-will-microsoft-have-to-resize-it"></a><span data-ttu-id="ee7bd-149">運用環境が定期的にリソースを使い果たす場合、Microsoft はサイズ変更をする必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-149">If a production environment regularly runs out of resources, will Microsoft have to resize it?</span></span>

<span data-ttu-id="ee7bd-150">はい。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-150">Yes.</span></span> <span data-ttu-id="ee7bd-151">サイズ変更見積もりも再検証され、アップロードされます。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-151">Sizing estimate will also have to be revalidated and uploaded.</span></span>

## <a name="after-april-2021-will-the-system-be-able-to-override-priority-based-throttling"></a><span data-ttu-id="ee7bd-152">2021 年 4 月以降、システムは優先順位に基づく調整を上書きできますか?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-152">After April 2021, will the system be able to override priority-based throttling?</span></span>

<span data-ttu-id="ee7bd-153">システムは、2021 年 4 月以降優先順位が構成されない場合、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ee7bd-153">The system will use default values if no priorities are configured after April 2021.</span></span>

## <a name="can-the-throttling-engine-be-configured-thresholds"></a><span data-ttu-id="ee7bd-154">調整エンジンは構成できますか (しきい値)?</span><span class="sxs-lookup"><span data-stu-id="ee7bd-154">Can the throttling engine be configured (thresholds)?</span></span>

<span data-ttu-id="ee7bd-155">No.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-155">No.</span></span>
