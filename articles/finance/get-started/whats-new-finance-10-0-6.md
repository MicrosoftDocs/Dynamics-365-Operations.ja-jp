---
title: Dynamics 365 Finance 10.0.6 (2019 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Finance 10.0.6 の新機能または変更された機能について説明します。
author: roschlom
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: d3c0e0f7089a82aa9e8f7cad45af1a7b3c6c7cc1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893858"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-1006-november-2019"></a><span data-ttu-id="991ce-103">Dynamics 365 Finance 10.0.6 (2019 年 11 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="991ce-103">What's new or changed in Dynamics 365 Finance 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="991ce-104">このトピックでは、Microsoft Dynamics 365 Finance 10.0.6 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="991ce-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Finance 10.0.6.</span></span> <span data-ttu-id="991ce-105">このバージョンのビルド番号は 10.0.234 です。</span><span class="sxs-lookup"><span data-stu-id="991ce-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="991ce-106">一般提供開始日は 11 月ですが、新機能は 10 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="991ce-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="991ce-107">バージョン 10.0.6 の詳細については [追加リソース](whats-new-finance-10-0-6.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="991ce-107">For more information about version 10.0.6, see [Additional resources](whats-new-finance-10-0-6.md#additional-resources).</span></span>

## <a name="feature-management-enhancements"></a><span data-ttu-id="991ce-108">機能管理の拡張</span><span class="sxs-lookup"><span data-stu-id="991ce-108">Feature management enhancements</span></span>
<span data-ttu-id="991ce-109">機能管理を使用すると、既定ですべての新機能を有効にできます。それには機能を有効にするための確認と、まだ有効になっていないすべての機能を有効にすることが必要です。</span><span class="sxs-lookup"><span data-stu-id="991ce-109">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 

## <a name="select-consolidation-amount-from-control-on-the-consolidate-online-for-dual-currency-consolidation"></a><span data-ttu-id="991ce-110">デュアル為替連結用オンラインでの連結の「連結金額の選択元」コントロール</span><span class="sxs-lookup"><span data-stu-id="991ce-110">“Select consolidation amount from” control on the consolidate online for dual currency consolidation</span></span>
<span data-ttu-id="991ce-111">この機能は、連結会社の取引通貨として使用される通貨 (会計またはレポート通貨) をコントロールするのに役立ち、通貨が同じ場合、ソースの会社から連結会社に金額を自動的にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="991ce-111">This features helps you control the currency (either the accounting or reporting currency) that's used as the transaction currency in the consolidation company and can automatically copy amounts from the source company to the consolidation company if the currencies are the same.</span></span>

## <a name="cancel-bank-reconciliation"></a><span data-ttu-id="991ce-112">口座調整のキャンセル</span><span class="sxs-lookup"><span data-stu-id="991ce-112">Cancel bank reconciliation</span></span>
<span data-ttu-id="991ce-113">ユーザーは、口座の調整を最新のものから始まる順序でキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="991ce-113">Users will be able to cancel bank reconciliations in chronological order of reconciliation starting with the most recent.</span></span> <span data-ttu-id="991ce-114">履歴が追跡され、調整が取り消された時期と担当者が表示されます。</span><span class="sxs-lookup"><span data-stu-id="991ce-114">History is tracked to show when and by whom the reconciliation was reversed.</span></span> <span data-ttu-id="991ce-115">これにより、ユーザーは、定期処理中に発生したエラーを修正するために仕訳帳を手動で調整する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="991ce-115">This will prevent users from having to manually adjust journals to correct any errors that occurred during the periodic process.</span></span>

## <a name="create-checks-with-a-blank-status-on-the-checks-page"></a><span data-ttu-id="991ce-116">[小切手] ページで空白状態の小切手を作成する</span><span class="sxs-lookup"><span data-stu-id="991ce-116">Create checks with a blank status on the Checks page</span></span>
<span data-ttu-id="991ce-117">**小切手** ページでは、新しい小切手番号の作成や小切手の削除など、小切手に関するメンテナンスタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="991ce-117">The **Checks** page is where you perform maintenance tasks on checks, such as creating new check numbers and deleting checks.</span></span> <span data-ttu-id="991ce-118">支払プロセス中にこの機能が有効になっている場合、支払プロセス中に空白ステータスの小切手を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="991ce-118">During the payment process, when this feature is enabled, you can't create checks with a blank status during the payment process.</span></span> <span data-ttu-id="991ce-119">この拡張機能により、不必要に小切手を無駄にすることがなくなります。</span><span class="sxs-lookup"><span data-stu-id="991ce-119">This enhancement helps prevent wasting checks unnecessarily.</span></span>

## <a name="reset-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a><span data-ttu-id="991ce-120">仕入先請求書のワークフロー ステータスを、修復不可能からドラフトにリセットする</span><span class="sxs-lookup"><span data-stu-id="991ce-120">Reset workflow status for vendor invoices from Unrecoverable to Draft</span></span>
<span data-ttu-id="991ce-121">ワークフローの履歴ページを使用して、ワークフロー状態をドラフトにリセットできます。</span><span class="sxs-lookup"><span data-stu-id="991ce-121">You can use the Workflow history page to reset the workflow status to Draft.</span></span> <span data-ttu-id="991ce-122">このページは、仕入先請求書 または 共通 > 照会 > ワークフロー へ移動することで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="991ce-122">This page can be opened from the Vendor invoice page or by going to Common > Inquires > Workflow.</span></span> <span data-ttu-id="991ce-123">ワークフロー状態をドラフトにリセットするには、取り消し を選択します。</span><span class="sxs-lookup"><span data-stu-id="991ce-123">To reset the workflow status to Draft, select Recall.</span></span> <span data-ttu-id="991ce-124">また、仕入先請求書 または 保留中の仕入先請求書 ページの 取り消し アクションを選択して、ワークフロー状態をドラフトにリセットすることもできます。</span><span class="sxs-lookup"><span data-stu-id="991ce-124">You can also reset the workflow status to Draft by selecting the Recall action on either the Vendor invoice or Pending vendor invoices page.</span></span> <span data-ttu-id="991ce-125">ワークフロー ステータスをドラフトにリセットした後、仕入れ先請求書 ページで編集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="991ce-125">After the workflow status is reset to Draft, it becomes available for editing on the Vendor invoice page.</span></span>

## <a name="revenue-recognition"></a><span data-ttu-id="991ce-126">収益認識</span><span class="sxs-lookup"><span data-stu-id="991ce-126">Revenue recognition</span></span>
<span data-ttu-id="991ce-127">収益認識管理は、会計および財務のプロフェッショナルが国際財務報告基準 (IFRS) 15 および会計基準成文化 (ASC) 606に準拠するために行うステップを自動化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="991ce-127">Revenue recognition management helps accounting and finance professionals automate the steps they take to comply with International Financial Reporting Standard (IFRS) 15 and Accounting Standards Codification (ASC) 606.</span></span>

<span data-ttu-id="991ce-128">新しい機能には、次のような製品バンドルとキットのサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="991ce-128">New capabilities will include support for product bundles and kits such as:</span></span>

- <span data-ttu-id="991ce-129">ソフトウェアおよびメンテナンス</span><span class="sxs-lookup"><span data-stu-id="991ce-129">Software and maintenance</span></span>
- <span data-ttu-id="991ce-130">ソフトウェアおよびサービス</span><span class="sxs-lookup"><span data-stu-id="991ce-130">Software and services</span></span>
- <span data-ttu-id="991ce-131">ソフトウェア</span><span class="sxs-lookup"><span data-stu-id="991ce-131">Software</span></span>
- <span data-ttu-id="991ce-132">ハードウェアおよびサービス</span><span class="sxs-lookup"><span data-stu-id="991ce-132">Hardware and service</span></span>

<span data-ttu-id="991ce-133">これらの処理能力により、次の機能が処理されます。</span><span class="sxs-lookup"><span data-stu-id="991ce-133">These capabilities will handle the following features:</span></span>

- <span data-ttu-id="991ce-134">収益価格設定</span><span class="sxs-lookup"><span data-stu-id="991ce-134">Revenue pricing</span></span> 
- <span data-ttu-id="991ce-135">収益スケジュール</span><span class="sxs-lookup"><span data-stu-id="991ce-135">Revenue schedules</span></span>
- <span data-ttu-id="991ce-136">バンドルの設定</span><span class="sxs-lookup"><span data-stu-id="991ce-136">Bundle setup</span></span> 
- <span data-ttu-id="991ce-137">複数の販売注文の再配賦</span><span class="sxs-lookup"><span data-stu-id="991ce-137">Multiple sales order reallocation</span></span>
- <span data-ttu-id="991ce-138">ワークスペースのナビゲーションおよびレポート</span><span class="sxs-lookup"><span data-stu-id="991ce-138">Workspace navigation and reporting</span></span>

## <a name="revenue-pricing"></a><span data-ttu-id="991ce-139">収益価格設定</span><span class="sxs-lookup"><span data-stu-id="991ce-139">Revenue pricing</span></span>
<span data-ttu-id="991ce-140">ユーザーは、顧客に請求するのとは異なって認識される価格を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="991ce-140">Users can enter a different price that they will recognize as different from what they charge the customer.</span></span>

<span data-ttu-id="991ce-141">[![収益価格設定のスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)</span><span class="sxs-lookup"><span data-stu-id="991ce-141">[![Revenue pricing screenshot](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)</span></span>

## <a name="revenue-schedules"></a><span data-ttu-id="991ce-142">収益スケジュール</span><span class="sxs-lookup"><span data-stu-id="991ce-142">Revenue schedules</span></span>
<span data-ttu-id="991ce-143">収益スケジュールによって、収益遅延の月数が決まります。</span><span class="sxs-lookup"><span data-stu-id="991ce-143">Revenue schedules determine the number of months for the revenue deferral.</span></span> <span data-ttu-id="991ce-144">その月の実際の日付に基づいて、月に均等配分、または発生した回数に基づいてスケジュールを作成するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="991ce-144">Options are available to create the schedule based on actual days of the month, splitting equally across month or based on a set number of occurrences.</span></span>

<span data-ttu-id="991ce-145">[![収益スケジュールのスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)</span><span class="sxs-lookup"><span data-stu-id="991ce-145">[![Revenue schedules screenshot](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)</span></span>

## <a name="multiple-sales-order-reallocation"></a><span data-ttu-id="991ce-146">複数の販売注文の再配賦</span><span class="sxs-lookup"><span data-stu-id="991ce-146">Multiple sales order reallocation</span></span>

<span data-ttu-id="991ce-147">[![複数の販売注文の再配賦のスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)</span><span class="sxs-lookup"><span data-stu-id="991ce-147">[![Multiple sales order reallocation screenshot](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)</span></span>

## <a name="workspace"></a><span data-ttu-id="991ce-148">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="991ce-148">Workspace</span></span> 
<span data-ttu-id="991ce-149">新しいワークスペースは、繰延収益に対して作成された収益スケジュール レコードのステータスを確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="991ce-149">The new workspace is used to look at the status of the revenues schedule records created for deferred revenue.</span></span>

<span data-ttu-id="991ce-150">[![収益認識ワークスペースのスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="991ce-150">[![Revenue recognition workspace screenshot](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)</span></span>

## <a name="project-contract-committed-detail"></a><span data-ttu-id="991ce-151">プロジェクト契約の確定済詳細</span><span class="sxs-lookup"><span data-stu-id="991ce-151">Project contract committed detail</span></span>
<span data-ttu-id="991ce-152">プロジェクト契約の資金調達ソースで確定された金額の詳細にドリルダウンして、確定された金額を構成する活動をユーザーが簡単に確認できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="991ce-152">You can now drilldown into the details of the committed amount on the funding source of a project contract, allowing the user to easily see the activity that makes up the committed amount.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="991ce-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="991ce-153">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="991ce-154">バグ修正</span><span class="sxs-lookup"><span data-stu-id="991ce-154">Bug fixes</span></span>
<span data-ttu-id="991ce-155">10.0.6 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="991ce-155">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="991ce-156">プラットフォーム update 30</span><span class="sxs-lookup"><span data-stu-id="991ce-156">Platform update 30</span></span>
<span data-ttu-id="991ce-157">Dynamics 365 Finance 10.0.6 には、プラットフォーム更新プログラム 30 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="991ce-157">Dynamics 365 Finance 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="991ce-158">プラットフォーム更新プログラム 30 についての詳細は、[Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能と変更点](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="991ce-158">To learn more about Platform update 30, see [What's new or changed in Platform update 30 for Finance and Operations apps (November 2019)](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="991ce-159">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="991ce-159">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="991ce-160">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="991ce-160">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="991ce-161">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="991ce-161">Check out the [Dynamics 365: 2019 release wave 2 plan](/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="991ce-162">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="991ce-162">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="991ce-163">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="991ce-163">Removed and deprecated features</span></span>
<span data-ttu-id="991ce-164">[Finance and Operations の削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックでは、Dynamics 365 forfin-ops-core/ Finance and Operations で削除または推奨されない機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="991ce-164">The [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 forfin-ops-core/ Finance and Operations.</span></span>

- <span data-ttu-id="991ce-165">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="991ce-165">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="991ce-166">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="991ce-166">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="991ce-167">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="991ce-167">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="991ce-168">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="991ce-168">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="991ce-169">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="991ce-169">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]