---
title: Finance and Operations アプリ バージョン 10.0.6 (2019 年 11 月) の新機能と変更点
description: このトピックでは、Finance and Operations アプリ バージョン 10.0.6 の新機能または変更された機能について説明します。 このバージョンは 10 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: f23018d822fa2b6641bedc7da895b01744b59487
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693499"
---
# <a name="whats-new-or-changed-in-finance-and-operations-apps-version-1006-november-2019"></a><span data-ttu-id="4a788-104">Finance and Operations アプリ バージョン 10.0.6 (2019 年 11 月) の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="4a788-104">What's new or changed in Finance and Operations apps version 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4a788-105">このトピックでは、バージョン 10.0.6 の、Microsoft Dynamics 365 Finance および Microsoft Dynamics 365 Supply Chain Management を含む Finance and Operations アプリの新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a788-105">This topic describes features that are either new or changed in Finance and Operations apps, including Microsoft Dynamics 365 Finance and Microsoft Dynamics 365 Supply Chain Management for version 10.0.6.</span></span> <span data-ttu-id="4a788-106">このバージョンのビルド番号は 10.0.234 です。</span><span class="sxs-lookup"><span data-stu-id="4a788-106">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="4a788-107">一般提供開始日は 11 月ですが、新機能は 10 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a788-107">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="4a788-108">バージョン 10.0.6 の詳細については [追加リソース](whats-new-changed-10-0-6.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a788-108">For more information about version 10.0.6, see [Additional resources](whats-new-changed-10-0-6.md#additional-resources).</span></span>

<span data-ttu-id="4a788-109">Microsoft Dynamics 365 Retail の新機能と変更の最新のリリースについては、[Dynamics 365 Retail バージョン 10.0.6 の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-6) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a788-109">To learn about the new features and changes in the latest releases of Microsoft Dynamics 365 Retail, see [What's new or changed in Dynamics 365 Retail version 10.0.6](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-6).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="4a788-110">製品コンフィギュレーション モデル V2 データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="4a788-110">Product configuration models V2 data entity</span></span>

<span data-ttu-id="4a788-111">"製品コンフィギュレーション モデル" データ エンティティの 2 番目のバージョンがリリースされます ("製品コンフィギュレーション モデルV2" と呼ばれる)。</span><span class="sxs-lookup"><span data-stu-id="4a788-111">A second version for the “product configuration models” data entity is released (called “products configuration models V2”).</span></span> <span data-ttu-id="4a788-112">既定のテンプレート "418- 製品コンフィギュレーション モデル" も、インポート/エクスポート フレームワーク テンプレートで新しい "製品コンフィギュレーション モデル V2" データ エンティティを使用するようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a788-112">The default template “418-product configuration models” is also needs to be so that it uses the new “product configuration models V2” data entity in the import/export framework templates.</span></span> <span data-ttu-id="4a788-113">テンプレートは自動更新されないので、既定で手動でテンプレートを読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a788-113">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="4a788-114">V2 エンティティは、1 つの行をインラインの代わりに添付ファイルの個別のファイルとしてエクスポートし、V1 エンティティのサイズ制限を解決します。</span><span class="sxs-lookup"><span data-stu-id="4a788-114">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="4a788-115">この変更を行うにはどうしますか。</span><span class="sxs-lookup"><span data-stu-id="4a788-115">What do you need to do to take this change?</span></span>
-   <span data-ttu-id="4a788-116">V1 エンティティは使用されなくなったため、V1 から V2 への移行を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a788-116">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="4a788-117">“418- 製品コンフィギュレーション モデル“ テンプレートを使用している場合、“既定のテンプレートの読み込み“ ボタンをクリックし、テンプレート "418- 製品コンフィギュレーション モデル" を再読み込みできます。</span><span class="sxs-lookup"><span data-stu-id="4a788-117">If you are using the  “418-product configuration models” template, you can click on “load default templates” button and reload the template “418 – product configuration models”</span></span>
-   <span data-ttu-id="4a788-118">既存のシステムとの互換性を維持する必要がある場合は、統合を新しいテンプレートに移行するまで、とりあえず既存のテンプレートおよび (非推奨) V1 エンティティを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a788-118">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="4a788-119">機能管理の拡張</span><span class="sxs-lookup"><span data-stu-id="4a788-119">Feature management enhancements</span></span>
<span data-ttu-id="4a788-120">機能管理を使用すると、既定ですべての新機能を有効にできます。それには機能を有効にするための確認と、まだ有効になっていないすべての機能を有効にすることが必要です。</span><span class="sxs-lookup"><span data-stu-id="4a788-120">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 

## <a name="project-contract-committed-detail"></a><span data-ttu-id="4a788-121">プロジェクト契約の確定済詳細</span><span class="sxs-lookup"><span data-stu-id="4a788-121">Project contract committed detail</span></span>
<span data-ttu-id="4a788-122">プロジェクト契約の資金調達ソースで確定された金額の詳細にドリルダウンして、確定された金額を構成する活動をユーザーが簡単に確認できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4a788-122">You can now drilldown into the details of the committed amount on the funding source of a project contract, allowing the user to easily see the activity that makes up the committed amount.</span></span>

## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="4a788-123">購買契約責任者</span><span class="sxs-lookup"><span data-stu-id="4a788-123">Purchase agreement responsible party</span></span>
<span data-ttu-id="4a788-124">購買契約分類フォームと結果の購買契約で、基本および二次の責任者を定義する機能が用意されました。</span><span class="sxs-lookup"><span data-stu-id="4a788-124">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="4a788-125">これにより、ユーザーは契約の監督者にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="4a788-125">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="4a788-126">発注書明細行の RFQ リンク</span><span class="sxs-lookup"><span data-stu-id="4a788-126">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="4a788-127">発注書明細行から元の RFQ 明細行に参照リンクを追加できます。これにより、サポートする見積依頼ドキュメントをユーザーに簡単に提供できます。</span><span class="sxs-lookup"><span data-stu-id="4a788-127">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a788-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4a788-128">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4a788-129">バグ修正</span><span class="sxs-lookup"><span data-stu-id="4a788-129">Bug fixes</span></span>
<span data-ttu-id="4a788-130">バージョン 10.0.6 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a788-130">For information about the bug fixes included in each of the updates that are part of version 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="4a788-131">プラットフォーム update 30</span><span class="sxs-lookup"><span data-stu-id="4a788-131">Platform update 30</span></span>
<span data-ttu-id="4a788-132">バージョン 10.0.6 には、プラットフォーム更新プログラム 30 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a788-132">Version 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="4a788-133">プラットフォーム更新プログラム 30 についての詳細は、[Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能と変更点](whats-new-platform-update-30.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a788-133">To learn more about Platform update 30, see [What's new or changed in Platform update 30 for Finance and Operations apps (November 2019)](whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="4a788-134">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="4a788-134">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="4a788-135">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="4a788-135">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="4a788-136">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="4a788-136">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="4a788-137">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="4a788-137">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="4a788-138">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="4a788-138">Removed and deprecated features</span></span>
<span data-ttu-id="4a788-139">[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md)トピックでは、削除または廃止された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a788-139">The [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated.</span></span>

- <span data-ttu-id="4a788-140">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="4a788-140">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="4a788-141">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4a788-141">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="4a788-142">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="4a788-142">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="4a788-143">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="4a788-143">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="4a788-144">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="4a788-144">Typically, these are functional updates that need to be made to the compiler.</span></span>
