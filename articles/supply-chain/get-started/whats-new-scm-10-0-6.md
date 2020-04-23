---
title: Dynamics 365 Supply Chain Management 10.0.6 (2019 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.6 の新機能または変更された機能について説明します。
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 319ba09184c087a194b664ca87076d57c6ba0c66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201551"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="d29a8-103">Dynamics 365 Supply Chain Management 10.0.6 (2019 年 11 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="d29a8-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d29a8-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management 10.0.6 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d29a8-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="d29a8-105">このバージョンのビルド番号は 10.0.234 です。</span><span class="sxs-lookup"><span data-stu-id="d29a8-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="d29a8-106">一般提供開始日は 11 月ですが、新機能は 10 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d29a8-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="d29a8-107">バージョン 10.0.6 の詳細については [追加リソース](whats-new-scm-10-0-6.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d29a8-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="d29a8-108">製品コンフィギュレーション モデル V2 データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="d29a8-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="d29a8-109">「製品コンフィギュレーション モデル」 データ エンティティの 2 番目のバージョンがリリースされます (「製品コンフィギュレーション モデル V2」 と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="d29a8-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="d29a8-110">既定のテンプレート 「418- 製品コンフィギュレーション モデル」も、インポート/エクスポート フレームワーク テンプレートで新しい「製品コンフィギュレーション モデル V2」 データ エンティティを使用するようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="d29a8-111">テンプレートは自動更新されないので、既定で手動でテンプレートを読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="d29a8-112">V2 エンティティは、1 つの行をインラインの代わりに添付ファイルの個別のファイルとしてエクスポートし、V1 エンティティのサイズ制限を解決します。</span><span class="sxs-lookup"><span data-stu-id="d29a8-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="d29a8-113">この変更を行うにはどうしますか。</span><span class="sxs-lookup"><span data-stu-id="d29a8-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="d29a8-114">V1 エンティティは使用されなくなったため、V1 から V2 への移行を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="d29a8-115">「418- 製品コンフィギュレーション モデル」 テンプレートを使用している場合、「既定のテンプレートの読み込み」ボタンをクリックし、テンプレート 「418- 製品コンフィギュレーション モデル」を再読み込みできます</span><span class="sxs-lookup"><span data-stu-id="d29a8-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="d29a8-116">既存のシステムとの互換性を維持する必要がある場合は、統合を新しいテンプレートに移行するまで、とりあえず既存のテンプレートおよび (非推奨) V1 エンティティを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="d29a8-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="d29a8-117">機能管理の拡張</span><span class="sxs-lookup"><span data-stu-id="d29a8-117">Feature management enhancements</span></span>
<span data-ttu-id="d29a8-118">機能管理を使用すると、既定ですべての新機能を有効にできます。それには機能を有効にするための確認と、まだ有効になっていないすべての機能を有効にすることが必要です。</span><span class="sxs-lookup"><span data-stu-id="d29a8-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="d29a8-119">購買契約責任者</span><span class="sxs-lookup"><span data-stu-id="d29a8-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="d29a8-120">購買契約分類フォームと結果の購買契約で、基本および二次の責任者を定義する機能が用意されました。</span><span class="sxs-lookup"><span data-stu-id="d29a8-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="d29a8-121">これにより、ユーザーは契約の監督者にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="d29a8-122">発注書明細行の RFQ リンク</span><span class="sxs-lookup"><span data-stu-id="d29a8-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="d29a8-123">発注書明細行から元の RFQ 明細行に参照リンクを追加できます。これにより、サポートする見積依頼ドキュメントをユーザーに簡単に提供できます。</span><span class="sxs-lookup"><span data-stu-id="d29a8-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d29a8-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d29a8-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d29a8-125">バグ修正</span><span class="sxs-lookup"><span data-stu-id="d29a8-125">Bug fixes</span></span>
<span data-ttu-id="d29a8-126">10.0.6 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d29a8-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="d29a8-127">プラットフォーム update 30</span><span class="sxs-lookup"><span data-stu-id="d29a8-127">Platform update 30</span></span>
<span data-ttu-id="d29a8-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 には、プラットフォーム更新プログラム 30 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d29a8-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="d29a8-129">プラットフォーム更新プロフラム 30 についての詳細は、[プラットフォーム更新プログラム 30 の新機能と変更](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d29a8-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="d29a8-130">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="d29a8-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="d29a8-131">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="d29a8-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="d29a8-132">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="d29a8-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="d29a8-133">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="d29a8-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="d29a8-134">削除済みおよび非推奨の Supply Chain Management 機能</span><span class="sxs-lookup"><span data-stu-id="d29a8-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="d29a8-135">[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d29a8-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="d29a8-136">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="d29a8-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="d29a8-137">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="d29a8-138">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="d29a8-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="d29a8-139">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="d29a8-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="d29a8-140">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="d29a8-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
