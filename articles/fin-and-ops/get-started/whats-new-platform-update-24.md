---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能または変更された機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 20189-XX-XX
ms.dyn365.ops.version: Platform 24
ms.openlocfilehash: af737fa630848f317ef34067f193447fe26a343d
ms.sourcegitcommit: 6f5b749a544b17def634301e48b59b8ff1c7b42a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "375178"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-24-march-2019"></a><span data-ttu-id="0d265-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0d265-103">What's new or changed in Dynamics 365 for Finance and Operations platform update 24 (March 2019)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0d265-104">このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 24 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d265-104">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations platform update 24.</span></span> <span data-ttu-id="0d265-105">このバージョンのビルド番号は、7.0.5179 です。</span><span class="sxs-lookup"><span data-stu-id="0d265-105">This version has a build number of 7.0.5179.</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="0d265-106">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="0d265-106">Dynamics 365 April '19 release notes</span></span>

<span data-ttu-id="0d265-107">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="0d265-107">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="0d265-108">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="0d265-108">[Check out the April '19 release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="0d265-109">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="0d265-109">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="platform-update-24-bug-fixes"></a><span data-ttu-id="0d265-110">プラットフォーム アップデート 24 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="0d265-110">Platform update 24 bug fixes</span></span>

<span data-ttu-id="0d265-111">プラットフォーム更新 24 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=287129&qc=6daf0a1b735f67d827cf6f643a2ef482dc0d66a220ce23ba6f3cba32ece56015)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d265-111">For information about the bug fixes included in each of the updates that are part of Platform update 24, sign in to Lifecycle Services (LCS) and view this [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=287129&qc=6daf0a1b735f67d827cf6f643a2ef482dc0d66a220ce23ba6f3cba32ece56015).</span></span>

## <a name="business-events"></a><span data-ttu-id="0d265-112">ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="0d265-112">Business events</span></span>
<span data-ttu-id="0d265-113">この新しい機能により、Finance and Operations の業務プロセスが実行されるときにビジネス イベントをキャプチャし、そのイベントを外部システムまたはアプリケーションに送信できるフレームワークが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0d265-113">This new capability will provide a framework that will allow business processes in Finance and Operations to capture business events as business processes are executed, and send the events to an external system or application.</span></span>

<span data-ttu-id="0d265-114">これにより、たとえば、発注書の承認によって、仕入先組織でのフルフィルメントがすぐにトリガーされるようになります。また破損部品の受領書 1 枚で、仕入先クレーム処理をリアルタイムでトリガーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0d265-114">This will allow, for example, a purchase order approval to quickly trigger a fulfillment in the vendor organization sooner than later; a receipt of a damaged part to trigger the vendor claim process in real time; and so on.</span></span> <span data-ttu-id="0d265-115">これらのイベントは業務プロセスのコンテキストで発生するため、*ビジネス イベント*と呼ばれ、*業務プロセスの統合*が可能になります。</span><span class="sxs-lookup"><span data-stu-id="0d265-115">Because these events happen in the context of business processes they are called *business events*, which enable *business process integration*.</span></span>

<span data-ttu-id="0d265-116">外部業務プロセスは、発生したときに通知を受けるために Finance and Operations の特定のビジネス イベントにサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="0d265-116">External business processes will subscribe to specific business events from Finance and Operations to get notified when they occur.</span></span> <span data-ttu-id="0d265-117">ビジネス イベントは Microsoft Finance and Operations コネクタの「トリガー」としても使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d265-117">The business events can also be consumed as "triggers" in the Finance and Operations connector.</span></span>

<span data-ttu-id="0d265-118">含まれる予定の機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d265-118">Some capabilities that will be included are:</span></span>

-   <span data-ttu-id="0d265-119">ビジネス イベント フレームワーク、パートナーおよび顧客が実装するビジネス イベント。</span><span class="sxs-lookup"><span data-stu-id="0d265-119">Business events framework, for partner and customer implemented business events.</span></span>

-   <span data-ttu-id="0d265-120">ビジネス イベント管理者エクスペリエンス。</span><span class="sxs-lookup"><span data-stu-id="0d265-120">Business events administrator experience.</span></span>

-   <span data-ttu-id="0d265-121">アプリケーション ビジネス イベント。</span><span class="sxs-lookup"><span data-stu-id="0d265-121">Application business events.</span></span>

-   <span data-ttu-id="0d265-122">ワークフロー ビジネス イベント。</span><span class="sxs-lookup"><span data-stu-id="0d265-122">Workflow business events.</span></span>

-   <span data-ttu-id="0d265-123">高度な統合シナリオのための Azure イベント グリッドおよび Azure Service Bus ですぐに使える統合。</span><span class="sxs-lookup"><span data-stu-id="0d265-123">Out-of-the-box integration with Azure Event Grid and Azure Service Bus for advanced integration scenarios.</span></span>

-   <span data-ttu-id="0d265-124">Microsoft Flow でビジネス イベントを「トリガー」として公開する。</span><span class="sxs-lookup"><span data-stu-id="0d265-124">Exposing business events as 'triggers' in Microsoft Flow.</span></span>

<span data-ttu-id="0d265-125">詳細については[ビジネス イベント](../../dev-itpro/business-events/home-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d265-125">For more information, see [Business events](../../dev-itpro/business-events/home-page.md).</span></span>

## <a name="new-apis"></a><span data-ttu-id="0d265-126">新しい API</span><span class="sxs-lookup"><span data-stu-id="0d265-126">New APIs</span></span>

<span data-ttu-id="0d265-127">データ プロジェクトのインポート実行中に発生したエラーをデータ統合が取得するために、新しい API が追加されました。</span><span class="sxs-lookup"><span data-stu-id="0d265-127">New APIs have been added to help data integration retrieve errors that occurred during the import execution runs in a data project.</span></span> <span data-ttu-id="0d265-128">詳細については、[データ管理パッケージ REST API](../../dev-itpro/data-entities/data-management-api.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d265-128">For more information, see [Data management package REST API](../../dev-itpro/data-entities/data-management-api.md).</span></span>

## <a name="client-alert-support-for-email-notifications-preview"></a><span data-ttu-id="0d265-129">電子メール通知のクライアント警告サポート (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="0d265-129">Client Alert support for email notifications (Preview)</span></span>
<span data-ttu-id="0d265-130">統合された変更追跡ツールで業務データを常に把握します。</span><span class="sxs-lookup"><span data-stu-id="0d265-130">Stay on top of your business data with integrated change tracking tools.</span></span>  <span data-ttu-id="0d265-131">プラットフォーム更新プログラム 24 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d265-131">With Platform update 24, users are able to create Alert Rules that automatically dispatch email notifications to contacts when triggered by an event.</span></span>  <span data-ttu-id="0d265-132">この機能は、Dynamic Ideas カスタマー フォーラムで最も求められている機能であると区別されています。</span><span class="sxs-lookup"><span data-stu-id="0d265-132">This capability has the distinction of being the number 1 requested feature in the Dynamics Ideas customer forum.</span></span>  <span data-ttu-id="0d265-133">Dynamics 365 for Finance and Operations で、ユーザーはデータのフィルター処理されたビューを監視するためのカスタム警告ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0d265-133">With Dynamics 365 for Finance and Operations, users are able to define custom Alert rules to monitor filtered views of their data.</span></span>  <span data-ttu-id="0d265-134">電子メール通知を受信するオプションは、サポートされているすべての警告タイプで使用可能であり、既存の警告ルールでも有効にできます。</span><span class="sxs-lookup"><span data-stu-id="0d265-134">The option of receiving email notifications is available for all supported Alert types and can be enabled for existing Alert rules.</span></span>  

<span data-ttu-id="0d265-135">サポートされるシナリオには、わかりやすいコントロールを使用して、システム バッチ ジョブのフィルター処理されたビューを監視する警告ルールを作成することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d265-135">Supported scenarios include using intuitive controls to create Alerts rules that monitor filtered views of System batch jobs.</span></span>  <span data-ttu-id="0d265-136">業務データへの変更についてのレポートを常にチェックするという負担から離れ、あなたに代わって Dynamics 365 for Finance and Operations インテリジェント変更検出サービスにモニタリングさせましょう。</span><span class="sxs-lookup"><span data-stu-id="0d265-136">Move beyond the burden of constantly checking reports for changes to business data and let the Dynamics 365 for Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

> [!Note]
> <span data-ttu-id="0d265-137">プレビュー機能への早期アクセスを取得するために、Dynamics 365 Insider プログラムに参加してください。</span><span class="sxs-lookup"><span data-stu-id="0d265-137">Join the Dynamics 365 Insider Program to get early access to preview features.</span></span>

## <a name="clear-identification-of-preview-builds"></a><span data-ttu-id="0d265-138">プレビュー ビルドの明確な ID</span><span class="sxs-lookup"><span data-stu-id="0d265-138">Clear identification of preview builds</span></span>
<span data-ttu-id="0d265-139">一部のパートナー、ISV、および顧客は、Preview Early Access Program (PEAP) に参加することによって、またはサービスの公開プレビューを使用することによって、Finance and Operations の運用前ビルドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0d265-139">Some partners, ISVs, and customers have access to preproduction builds of Finance and Operations by being part of the Preview Early Access Program (PEAP) or by using public previews of the service.</span></span> <span data-ttu-id="0d265-140">このプレビュー フェーズは、最新の機能についてのフィードバックおよびカスタマイズ検証のメカニズムとなることを意図しています。</span><span class="sxs-lookup"><span data-stu-id="0d265-140">This preview phase is intended as a mechanism for feedback on the latest features and for validation of customizations.</span></span> <span data-ttu-id="0d265-141">ただし、これらの初期リリースは実稼働環境での使用を許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0d265-141">These early releases, however, are not authorized to be used in production.</span></span> <span data-ttu-id="0d265-142">Finance and Operations のリリース プロセスの詳細については、[標準および最初のリリース サービス更新プログラム](public-preview-releases.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d265-142">For more information about the Finance and Operations release process, see [Standard and First release service updates](public-preview-releases.md).</span></span>

<span data-ttu-id="0d265-143">**プレビュー** ステータスをユーザーに明確にするために、各運用前ビルドは 2 つの異なる方法でタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="0d265-143">To make the **preview** status clear to users, each preproduction build will be tagged in two different ways:</span></span> 

- <span data-ttu-id="0d265-144">ナビゲーション バーには製品名の接尾語として「プレビュー」という単語が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d265-144">Users will see the word "Preview" as a suffix to the product name in the navigation bar.</span></span>  

    <span data-ttu-id="0d265-145">![ナビゲーション バーのプレビュー インジケーター](media/previewCallout.png  "ナビゲーション バーのプレビュー インジケーター")</span><span class="sxs-lookup"><span data-stu-id="0d265-145">![Preview indicator in the navigation bar](media/previewCallout.png  "Preview indicator in the navigation bar")</span></span>  

- <span data-ttu-id="0d265-146">**情報**ボックスのタイトルには、「プレビュー」という単語が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d265-146">The title of the **About** box will include the word "Preview".</span></span> 

    <span data-ttu-id="0d265-147">![プレビューは情報ボックスにも表示されます](media/previewAboutBox.png  "プレビューは情報ボックスにも表示されます")</span><span class="sxs-lookup"><span data-stu-id="0d265-147">![Preview is also indicated in the About box](media/previewAboutBox.png  "Preview is also indicated in the About box")</span></span>
    

## <a name="updated-navigation-bar-that-aligns-with-the-office-header"></a><span data-ttu-id="0d265-148">Office のヘッダーに対応した更新済みのナビゲーション バー</span><span class="sxs-lookup"><span data-stu-id="0d265-148">Updated navigation bar that aligns with the Office header</span></span>
<span data-ttu-id="0d265-149">Dynamics 365 Office 製品は、各ヘッダーを Office ヘッダーと対応させて、Microsoft 製品全体のユーザーにとってよりまとまりのあるシェル エクスペリエンスを提供するよう取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="0d265-149">Dynamics 365 products are working to align their respective headers with the Office header to provide a more cohesive shell experience for users across Microsoft products.</span></span> <span data-ttu-id="0d265-150">Finance and Operations のユーザーにとって、このヘッダー更新プログラムは、ナビゲーション検索をより目立つようにした、完全に再構成されたナビゲーション バーを見なされるでしょう。</span><span class="sxs-lookup"><span data-stu-id="0d265-150">For Finance and Operations users, this header update will be seen as a completely restyled navigation bar that more prominently features navigation search.</span></span> <span data-ttu-id="0d265-151">特に、新しいデザインには階層リンクは含まれません。</span><span class="sxs-lookup"><span data-stu-id="0d265-151">Notably, the new design does not include a breadcrumb.</span></span> 

<span data-ttu-id="0d265-152">次の図は、プラットフォーム更新プログラム 24 の更新済のナビゲーション バーを表示します。</span><span class="sxs-lookup"><span data-stu-id="0d265-152">The following image shows the updated navigation bar in Platform update 24.</span></span>

<span data-ttu-id="0d265-153">![プラットフォーム更新プログラム 24 の更新済ナビゲーション バー](media/updatedNavBar.png  "プラットフォーム更新プログラム 24 の更新済ナビゲーション バー")</span><span class="sxs-lookup"><span data-stu-id="0d265-153">![Updated navigation bar in Platform update 24](media/updatedNavBar.png  "Updated navigation bar in Platform update 24")</span></span>

<span data-ttu-id="0d265-154">次の図は、プラットフォーム更新プログラム 23 でナビゲーション バーがどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="0d265-154">The following image shows how the navigation bar appeared in Platform update 23.</span></span>

<span data-ttu-id="0d265-155">![プラットフォーム更新プログラム 23 のナビゲーション バー](media/existingNavBar.png  "プラットフォーム更新プログラム 23 のナビゲーション バー")</span><span class="sxs-lookup"><span data-stu-id="0d265-155">![Navigation bar in Platform update 23](media/existingNavBar.png  "Navigation bar in Platform update 23")</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="0d265-156">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="0d265-156">Extensibility enhancements</span></span>

<span data-ttu-id="0d265-157">プラットフォーム更新プログラム 24 に含まれる[プラットフォーム拡張機能の 1 番目の波](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility)は、2019 年 4 月リリース ノートにドキュメントされています。</span><span class="sxs-lookup"><span data-stu-id="0d265-157">The [first wave of platform extensibility enhancements](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility), included in Platform update 24, are documented in the April 2019 Release notes.</span></span> <span data-ttu-id="0d265-158">9 つの拡張機能が詳細に説明されています。ハイライトの 1 つは、フォーム ボタン コントロールの新しい onClicking イベントです。</span><span class="sxs-lookup"><span data-stu-id="0d265-158">There are nine enhancements detailed, with one of the highlights being a new onClicking event for form button controls.</span></span>
