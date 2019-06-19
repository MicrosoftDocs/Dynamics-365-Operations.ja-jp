---
title: Finance and Operations バージョン 10.0.2 (2019 年 5 月) の新機能および変更点
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.2 の新機能または変更された機能について説明します。 このバージョンは 5 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 1db22391cd5dd53da7ca24301a537ceafa6b6fc8
ms.sourcegitcommit: bbc9aa0d6b94a942e1f4d5b038601509dcc87937
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2019
ms.locfileid: "1619157"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1002-may-2019"></a><span data-ttu-id="ab1a2-104">Finance and Operations バージョン 10.0.2 (2019 年 5 月) の新機能および変更点</span><span class="sxs-lookup"><span data-stu-id="ab1a2-104">What's new or changed in Finance and Operations version 10.0.2 (May 2019)</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ab1a2-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 10.0.2.</span></span> <span data-ttu-id="ab1a2-106">このバージョンは 5 月にリリースされ、ビルド番号は 10.0.80 です。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-106">This version will be released in May and has a build number of 10.0.80.</span></span> <span data-ttu-id="ab1a2-107">バージョン 10.0.2 の詳細については [追加リソース](whats-new-changed-10-0-2.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-107">For more information about version 10.0.2, see [Additional resources](whats-new-changed-10-0-2.md#additional-resources).</span></span>


<span data-ttu-id="ab1a2-108">最新のリリースの Microsoft Dynamics 365 for Retail の新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.2 の新機能と変更](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/get-started/whats-new-10-0-2) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-108">To learn about the new features and changes in the latest releases of Microsoft Dynamics 365 for Retail, see [What's new or changed in Dynamics 365 for Retail version 10.0.2](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/get-started/whats-new-10-0-2).</span></span>

  
## <a name="recovering-vendor-invoices-that-are-in-use"></a><span data-ttu-id="ab1a2-109">使用中の仕入先請求書を回復します。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-109">Recovering vendor invoices that are in use</span></span>

<span data-ttu-id="ab1a2-110">**仕入先請求書を回復** ページを使用して、4 時間以上使用されている仕入先請求書を回復またはリリースし、編集可能にします。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-110">You can use the **Recover vendor invoices** page to recover or release vendor invoices that have been in use for more than four hours, so that they can be edited.</span></span> <span data-ttu-id="ab1a2-111">このページは、**定期処理タスク** ナビゲーション リンクまたは、**仕入先請求書の入力** ワークスペースのタイルから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-111">You can open this page from the **Periodic task** navigation link or a tile on the **Vendor invoice entry** workspace.</span></span> <span data-ttu-id="ab1a2-112">請求書が復旧した後、**仕入先請求書** ページで編集可能になります。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-112">After an invoice is recovered, it will be available for editing on the **Vendor invoice** page.</span></span>

<span data-ttu-id="ab1a2-113">詳細については [仕入先請求書の概要](../../financials/accounts-payable/vendor-invoices-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-113">For more information, see [Vendor invoices overview](../../financials/accounts-payable/vendor-invoices-overview.md).</span></span>
  
## <a name="bank-foreign-currency-revaluation"></a><span data-ttu-id="ab1a2-114">銀行の外貨再評価</span><span class="sxs-lookup"><span data-stu-id="ab1a2-114">Bank foreign currency revaluation</span></span>

<span data-ttu-id="ab1a2-115">期間終了の一環として、いくつかの会計の慣行では、外貨建ての銀行口座残高は異なる為替レートの種類 (現在、過去、平均など) を使用して再評価が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-115">As part of a period end, some accounting practices require that bank account balances in foreign currencies be revalued by using different exchange rate types (current, historical, average, and so on).</span></span> <span data-ttu-id="ab1a2-116">銀行の外貨再評価の機能を使用して、ひとつ以上の銀行口座を再評価できます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-116">The bank foreign currency revaluation feature can be used to revalue one or more bank accounts.</span></span> <span data-ttu-id="ab1a2-117">これはグローバルな機能でもあり、単一のページからアクセスできるすべての法人に対して銀行を再評価できます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-117">The is also a global feature, which means that from a single page, you can revalue banks across all the legal entities that you have access to.</span></span>
  
## <a name="create-project-based-sales-orders-for-projects-with-a-funding-source-of-type-grant"></a><span data-ttu-id="ab1a2-118">交付タイプの資金調達ソースのプロジェクトに対して、プロジェクト ベースの販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-118">Create project-based sales orders for projects with a funding source of type Grant</span></span>

<span data-ttu-id="ab1a2-119">この機能は、関連プロジェクト契約の交付によって出資される時間/実費払いプロジェクトのプロジェクト ベースの、販売注文の作成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-119">This feature provides support for the creation of project-based sales orders for time and material projects funded by a grant on the related project contract.</span></span> <span data-ttu-id="ab1a2-120">交付の連絡先として割り当てられている顧客は、販売注文の顧客です。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-120">The customer assigned as the contact for the grant will be the customer on the sales order.</span></span>

## <a name="support-for-project-based-sales-orders-for-projects-with-multiple-funding-sources"></a><span data-ttu-id="ab1a2-121">複数の資金調達ソースを持つプロジェクトに対するプロジェクト ベースの販売注文のサポート</span><span class="sxs-lookup"><span data-stu-id="ab1a2-121">Support for project-based sales orders for projects with multiple funding sources</span></span>

<span data-ttu-id="ab1a2-122">この機能を使用すると、関連するプロジェクト契約に複数の資金調達ソースがある場合に、時間/実費払いプロジェクトの販売注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-122">This feature lets you create sales orders for time and material projects where the related project contract has multiple funding sources.</span></span> <span data-ttu-id="ab1a2-123">**プロジェクト管理および会計パラメーター** ページの **一般** タブで **複数の資金調達ソースがあるプロジェクトの販売注文を許可する** オプションを選択して、この機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-123">Enable this feature by selecting the **Allow sales orders for projects with multiple funding sources** option on the **General** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="ab1a2-124">このパラメータは削除され、今後のリリースでこの機能は常に有効になる予定です。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-124">This parameter will be removed and the feature will always be enabled in a future release.</span></span> <span data-ttu-id="ab1a2-125">詳細については [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-125">For more information, refer to [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

## <a name="acceptance-test-library"></a><span data-ttu-id="ab1a2-126">承認テスト ライブラリ</span><span class="sxs-lookup"><span data-stu-id="ab1a2-126">Acceptance test library</span></span>

<span data-ttu-id="ab1a2-127">この開発者向け機能を使用すると、販売注文、顧客、品目などの何百ものエンティティを含む豊富なドメイン固有言語を使用して、単体テストおよびコンポーネント テストを効率的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-127">This developer features enables you to efficiently write unit and component tests using a rich domain-specific language that contains hundreds of entities such as sales orders, customers, and items.</span></span> <span data-ttu-id="ab1a2-128">詳細については [承認テスト ライブラリ](../../dev-itpro/perf-test/acceptance-test-library.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-128">For more information, see  [Acceptance test library](../../dev-itpro/perf-test/acceptance-test-library.md).</span></span>  

## <a name="regulatory-updates"></a><span data-ttu-id="ab1a2-129">規制の更新</span><span class="sxs-lookup"><span data-stu-id="ab1a2-129">Regulatory updates</span></span>
<span data-ttu-id="ab1a2-130">Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-130">For information about the regulatory updates for Finance and Operations, see [Localization and Regulatory features – Regulatory updates](../../financials/localizations/regulatory-updates.md).</span></span> <span data-ttu-id="ab1a2-131">また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-131">Alternatively, you can sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool, where you can search by country, type of feature, and release.</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="ab1a2-132">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="ab1a2-132">Extensibility enhancements</span></span>

<span data-ttu-id="ab1a2-133">このFinance and Operations のリリースでは、拡張性をサポートするために多くの機能拡張が行われています。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-133">In this release of Finance and Operations, numerous enhancements have been made to support extensibility.</span></span> <span data-ttu-id="ab1a2-134">たとえば、列挙体、メタデータ、メソッドに拡張性の機能拡張が行われています。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-134">For example, extensibility enhancements have been made to enumerations, metadata, and methods.</span></span> <span data-ttu-id="ab1a2-135">詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0.2 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10-2.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-135">For detailed information, see [Extensibility changes in Dynamics 365 for Finance and Operations version 10.0.2](../../dev-itpro/extensibility/extensibility-changes-10-2.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab1a2-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ab1a2-136">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ab1a2-137">バグ修正</span><span class="sxs-lookup"><span data-stu-id="ab1a2-137">Bug fixes</span></span>
<span data-ttu-id="ab1a2-138">Finance and Operations 10.0.2 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=313841&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-138">For information about the bug fixes included in each of the updates that are part of Finance and Operations version 10.0.2, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=313841&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8).</span></span>

### <a name="platform-update-26"></a><span data-ttu-id="ab1a2-139">プラットフォーム update 26</span><span class="sxs-lookup"><span data-stu-id="ab1a2-139">Platform update 26</span></span>

<span data-ttu-id="ab1a2-140">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 には、プラットフォーム更新プログラム 26 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-140">Microsoft Dynamics 365 for Finance and Operations version 10.0.2 includes Platform update 26.</span></span> <span data-ttu-id="ab1a2-141">プラットフォーム更新プログラム 26 の詳細ついては [Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) の新機と変更点](whats-new-platform-update-26.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-141">To learn more about Platform update 26, see [What's new or changed in Finance and Operations platform update 26 (May 2019)](whats-new-platform-update-26.md).</span></span>


### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="ab1a2-142">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="ab1a2-142">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="ab1a2-143">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="ab1a2-143">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="ab1a2-144">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-144">[Check out the April '19 release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="ab1a2-145">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-145">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="ab1a2-146">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="ab1a2-146">Removed and deprecated features</span></span>
<span data-ttu-id="ab1a2-147">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-147">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="ab1a2-148">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-148">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ab1a2-149">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-149">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ab1a2-150">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-150">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="ab1a2-151">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-151">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="ab1a2-152">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="ab1a2-152">Typically these are functional updates that need to be made to the compiler.</span></span>