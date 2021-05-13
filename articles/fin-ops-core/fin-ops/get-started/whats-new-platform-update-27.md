---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) でプレビューされる機能について説明します。
author: tonyafehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-06-30
ms.dyn365.ops.version: Platform 27
ms.openlocfilehash: 01e792d9f92f92124867d514a20ad240cf520e09
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923325"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-27-june-2019"></a><span data-ttu-id="25016-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="25016-103">What's new or changed in Dynamics 365 for Finance and Operations platform update 27 (June 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25016-104">このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="25016-104">This topic describes features that are new or changed in Dynamics 365 for Finance and Operations platform update 27.</span></span> <span data-ttu-id="25016-105">このバージョンのビルド番号は 7.0.5286 です。</span><span class="sxs-lookup"><span data-stu-id="25016-105">This version has a build number of 7.0.5286.</span></span> <span data-ttu-id="25016-106">プラットフォーム更新プログラム 27 の詳細については [追加リソース](whats-new-platform-update-27.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25016-106">For more information about Platform update 27, see [Additional resources](whats-new-platform-update-27.md#additional-resources).</span></span>

## <a name="feature-management"></a><span data-ttu-id="25016-107">機能管理</span><span class="sxs-lookup"><span data-stu-id="25016-107">Feature Management</span></span>
<span data-ttu-id="25016-108">**機能管理** エクスペリエンスは、各リリースで提供されている機能を表示、有効化、無効化、およびスケジュールできるワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="25016-108">The **Feature management** experience provides a workspace where you can view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="25016-109">既定では、新機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="25016-109">By default, new features are turned off.</span></span> <span data-ttu-id="25016-110">ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="25016-110">You can use the workspace to turn them on and view the documentation for them.</span></span> 

<span data-ttu-id="25016-111">機能管理の詳細については [機能管理の概要](feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25016-111">For more information about Feature management, see [Feature management overview](feature-management/feature-management-overview.md).</span></span>

## <a name="dedicated-capacity-to-process-business-events"></a><span data-ttu-id="25016-112">ビジネス イベントを処理する専用キャパシティ</span><span class="sxs-lookup"><span data-stu-id="25016-112">Dedicated capacity to process business events</span></span> 
<span data-ttu-id="25016-113">ビジネス イベント処理バッチ ジョブをスケジュールして、ビジネス イベントを処理する必要はもうなくなります。</span><span class="sxs-lookup"><span data-stu-id="25016-113">It will be no longer required to schedule the business event processing batch job to process business events.</span></span> <span data-ttu-id="25016-114">専用スレッドがシステムによってビジネス イベントを処理するために割り当てられ、これによりビジネス イベントの処理が高速化します。</span><span class="sxs-lookup"><span data-stu-id="25016-114">Dedicated threads are allocated to process business events by the system, which ensures faster processing of business events.</span></span> <span data-ttu-id="25016-115">既存のバッチ ジョブをまだ使用できます (ただし、専用キャパシティに問題がある場合を除き、実行する必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="25016-115">The existing batch job is still available (but is not needed to run unless there are issues with dedicated capacity).</span></span> <span data-ttu-id="25016-116">このプラットフォーム更新の前にバッチ ジョブが既にスケジュールされていた場合は、バッチが無効になり、更新後に専用スレッドに引き継がれます。</span><span class="sxs-lookup"><span data-stu-id="25016-116">If the batch job was already scheduled prior to this platform update, the batch will become ineffective and dedicated threads will take over after the update.</span></span>

<span data-ttu-id="25016-117">詳細については、[ビジネス イベントの概要](../../dev-itpro/business-events/home-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25016-117">For more information, see [Business events overview](../../dev-itpro/business-events/home-page.md).</span></span>

## <a name="cancel-a-running-batch-job"></a><span data-ttu-id="25016-118">実行中のバッチ ジョブをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="25016-118">Cancel a running batch job</span></span>
<span data-ttu-id="25016-119">ジョブに現在実行中のタスクが含まれている場合、バッチ ジョブのキャンセルに長い時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="25016-119">It can take a long time to cancel a batch job if the job has tasks that are currently executing.</span></span> <span data-ttu-id="25016-120">中止オプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、ジョブがキャンセルされた場合にジョブに対してすでに実行中のタスクをキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="25016-120">The abort option provides a system administrator or batch job manager with the ability to cancel already executing tasks for jobs if the jobs are canceled.</span></span> <span data-ttu-id="25016-121">これは他の場所でシステムの使用に影響を与える可能性がある長時間実行中のジョブをキャンセルする、はるかに高速なメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="25016-121">This provides a much faster mechanism to cancel a long running job that might impact system usage in other places.</span></span> <span data-ttu-id="25016-122">詳細については [実行中のバッチ ジョブの中止](../../dev-itpro/sysadmin/batch-abort.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25016-122">For more information, see [Abort an executing batch job](../../dev-itpro/sysadmin/batch-abort.md)</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="25016-123">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="25016-123">Extensibility enhancements</span></span>
<span data-ttu-id="25016-124">プラットフォーム更新プログラム 27 に含まれる [プラットフォーム拡張機能の 4 番目の波](/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility4) は、2019 年 4 月リリース ノートにドキュメントされています。</span><span class="sxs-lookup"><span data-stu-id="25016-124">The [fourth wave of platform extensibility enhancements](/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility4) included in Platform update 27 is documented in the April 2019 release notes.</span></span> <span data-ttu-id="25016-125">2 つの機能強化の詳細が記載されており、そのハイライトは表示拡張がラベルとヘルプ テキストの値を変更できるようになったことです。</span><span class="sxs-lookup"><span data-stu-id="25016-125">There are two enhancements detailed, with the highlight being that View extensions can now change label and help text values.</span></span>

## <a name="export-data-from-all-companies-to-byod-can-be-enabled-via-parameters"></a><span data-ttu-id="25016-126">パラメーターを使用してすべての会社からデータをエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="25016-126">Export data from all companies to BYOD can be enabled via parameters</span></span>
<span data-ttu-id="25016-127">すべての企業から BYOD へのエクスポートを可能にする機能を、データ管理のフレームワーク パラメーターで有効にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="25016-127">The functionality to enable export from all companies to BYOD can now be enabled in framework parameters in data management.</span></span> <span data-ttu-id="25016-128">この時点では、これにより、不要なフライトが有効になります。</span><span class="sxs-lookup"><span data-stu-id="25016-128">Until now, this required a flight to be enabled which is no longer needed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25016-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="25016-129">Additional resources</span></span>

### <a name="platform-update-27-bug-fixes"></a><span data-ttu-id="25016-130">プラットフォーム アップデート 27 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="25016-130">Platform update 27 bug fixes</span></span>
<span data-ttu-id="25016-131">プラットフォーム更新 27 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=320391&dbType=3&qc=d5539716f56ccea45e2187c269570772af20e1f10a78371811220da6315a3c34)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25016-131">For information about the bug fixes included in each of the updates that are part of Platform update 27, sign in to Lifecycle Services (LCS) and view this [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=320391&dbType=3&qc=d5539716f56ccea45e2187c269570772af20e1f10a78371811220da6315a3c34).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="25016-132">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="25016-132">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="25016-133">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="25016-133">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="25016-134">[2019 年 4 月リリース ノートをご覧ください](/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="25016-134">[Check out the April '19 release notes](/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="25016-135">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="25016-135">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="25016-136">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="25016-136">Removed and deprecated features</span></span>
<span data-ttu-id="25016-137">[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="25016-137">The [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="25016-138">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="25016-138">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="25016-139">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25016-139">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="25016-140">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="25016-140">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="25016-141">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="25016-141">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="25016-142">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="25016-142">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]