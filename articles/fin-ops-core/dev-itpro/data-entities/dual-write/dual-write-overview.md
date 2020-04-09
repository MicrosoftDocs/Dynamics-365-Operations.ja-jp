---
title: 二重書き込みの概要
description: このトピックでは、二重書き込みの概要について説明します。 二重書き込みは、Microsoft Dynamics 365 モデル駆動型のアプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供するインフラストラクチャです。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172787"
---
# <a name="dual-write-overview"></a><span data-ttu-id="538c9-104">二重書き込みの概要</span><span class="sxs-lookup"><span data-stu-id="538c9-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="538c9-105">二重書き込みとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="538c9-105">What is dual-write?</span></span>

<span data-ttu-id="538c9-106">二重書き込みは、Microsoft Dynamics 365 モデル駆動型のアプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。</span><span class="sxs-lookup"><span data-stu-id="538c9-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="538c9-107">顧客、製品、人材、および業務に関するデータがアプリケーション境界を超えてフローする場合、組織のすべての部門が権利を持つことになります。</span><span class="sxs-lookup"><span data-stu-id="538c9-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="538c9-108">二重書き込みは、Finance and Operations アプリと Common Data Service の間で密に結合された双方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="538c9-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="538c9-109">Finance and Operations アプリでのデータの変更によって Common Data Service 書き込みが行われ、Common Data Service のデータの変更によって Finance and Operations アプリケーションへの書き込みが行われます。</span><span class="sxs-lookup"><span data-stu-id="538c9-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="538c9-110">この自動化されたデータ フローによって、アプリ間で統合されたユーザー エクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![アプリ間のデータの関係](media/dual-write-overview.jpg)

<span data-ttu-id="538c9-112">二重書き込みには、*インフラストラクチャ*の側面と*アプリケーション*の側面の 2 つの側面があります。</span><span class="sxs-lookup"><span data-stu-id="538c9-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="538c9-113">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="538c9-113">Infrastructure</span></span>

<span data-ttu-id="538c9-114">二重書き込みインフラストラクチャは、拡張性と信頼性を備えており、次の主な機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="538c9-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="538c9-115">アプリケーション間の同期および双方向のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="538c9-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="538c9-116">同期と、オンラインおよびオフライン/非同期モードでシステムをサポートするための再生、一時停止、キャッチ アップの各モードとの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="538c9-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="538c9-117">アプリケーション間で初期データを同期する機能</span><span class="sxs-lookup"><span data-stu-id="538c9-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="538c9-118">データ管理者の活動とエラー ログの統合ビュー</span><span class="sxs-lookup"><span data-stu-id="538c9-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="538c9-119">カスタム警告としきい値をコンフィギュレーションし、通知をサブスクライブする機能</span><span class="sxs-lookup"><span data-stu-id="538c9-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="538c9-120">フィルタリングと変換のための直観的なユーザー インターフェイス (UI)</span><span class="sxs-lookup"><span data-stu-id="538c9-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="538c9-121">エンティティの相互関係と関係を設定および表示する機能</span><span class="sxs-lookup"><span data-stu-id="538c9-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="538c9-122">標準エンティティとカスタム エンティティおよびマップの両方に対する拡張性</span><span class="sxs-lookup"><span data-stu-id="538c9-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="538c9-123">信頼できるアプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="538c9-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="538c9-124">新しい顧客に対する標準の設定エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="538c9-125">申請</span><span class="sxs-lookup"><span data-stu-id="538c9-125">Application</span></span>

<span data-ttu-id="538c9-126">二重書き込みでは、Finance and Operations アプリと Dynamics 365 のモデル駆動型アプリにおける概念の間にマッピングが作成されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="538c9-127">この統合により、次のシナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="538c9-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="538c9-128">統合された顧客マスター</span><span class="sxs-lookup"><span data-stu-id="538c9-128">Integrated customer master</span></span>
+ <span data-ttu-id="538c9-129">顧客ロイヤルティ カードおよび報酬ポイントへのアクセス</span><span class="sxs-lookup"><span data-stu-id="538c9-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="538c9-130">統一された製品マスタリング エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="538c9-131">組織階層の認識</span><span class="sxs-lookup"><span data-stu-id="538c9-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="538c9-132">統合された仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="538c9-132">Integrated vendor master</span></span>
+ <span data-ttu-id="538c9-133">財務および税参照データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="538c9-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="538c9-134">オンデマンドの価格エンジンのエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="538c9-135">統合された見込み顧客エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="538c9-136">フィールド エージェントを介して社内資産と顧客資産の両方を提供する機能</span><span class="sxs-lookup"><span data-stu-id="538c9-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="538c9-137">統合された仕入れから支払エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="538c9-138">顧客データおよびドキュメントに関する統合された活動とメモ</span><span class="sxs-lookup"><span data-stu-id="538c9-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="538c9-139">手持在庫状態および詳細を検索する機能</span><span class="sxs-lookup"><span data-stu-id="538c9-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="538c9-140">プロジェクトの現金化エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="538c9-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="538c9-141">関係者の概念を使用して複数の住所と役割を処理する機能</span><span class="sxs-lookup"><span data-stu-id="538c9-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="538c9-142">ユーザーに対する単一のソース管理</span><span class="sxs-lookup"><span data-stu-id="538c9-142">Single source management for users</span></span>
+ <span data-ttu-id="538c9-143">小売業とマーケティング向けの統合チャネル</span><span class="sxs-lookup"><span data-stu-id="538c9-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="538c9-144">プロモーションと割引の可視性</span><span class="sxs-lookup"><span data-stu-id="538c9-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="538c9-145">サービス要求機能</span><span class="sxs-lookup"><span data-stu-id="538c9-145">Request-for-service functions</span></span>
+ <span data-ttu-id="538c9-146">合理化されたサービス工程</span><span class="sxs-lookup"><span data-stu-id="538c9-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="538c9-147">二重書き込みを使用する主な理由</span><span class="sxs-lookup"><span data-stu-id="538c9-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="538c9-148">二重書き込みにより、Microsoft Dynamics 365 アプリケーション間でデータの統合が提供されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="538c9-149">この信頼性の高いフレームワークでは、環境をリンクして、さまざまなビジネス アプリケーションを連携させることができます。</span><span class="sxs-lookup"><span data-stu-id="538c9-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="538c9-150">二重書き込みを使用する必要がある主な理由は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="538c9-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="538c9-151">二重書き込みは、Finance and Operations アプリと Dynamics 365 の モデル駆動型アプリの間で密結合、ほぼリアルタイム、および双方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="538c9-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="538c9-152">この統合により、すべてのビジネスソリューションに対して、1 つの停止ショップとして Microsoft Dynamics 365 が作成されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="538c9-153">Dynamics 365 Finance と Dynamics 365 Supply Chain Management を使用しているが、顧客関係管理 (CRM) に対して Microsoft 以外のソリューションを使用している顧客は、二重書き込みをサポートするために Dynamics 365 に移行しています。</span><span class="sxs-lookup"><span data-stu-id="538c9-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="538c9-154">顧客、製品、工程、プロジェクト、およびインターネット オブ シングス (IoT) のデータは、自動的に二重書き込みによって Common Data Service にフローします。</span><span class="sxs-lookup"><span data-stu-id="538c9-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="538c9-155">この接続は、Microsoft Power Platform の展開に関心のある企業にとって非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="538c9-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="538c9-156">二重書き込みインフラストラクチャは、コードなし/ロー コード原則に従います。</span><span class="sxs-lookup"><span data-stu-id="538c9-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="538c9-157">標準のテーブルからテーブルへのマップを拡張したり、カスタム マップを含めたりするには、最小限のエンジニアリング実績が要求されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="538c9-158">二重書き込みでは、オンライン モードとオフライン モードの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="538c9-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="538c9-159">Microsoft は、オンラインとオフライン モードのサポートを提供している唯一の会社です。</span><span class="sxs-lookup"><span data-stu-id="538c9-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="538c9-160">CRM 製品のユーザーと設計者における二重書き込みの意味は何ですか?</span><span class="sxs-lookup"><span data-stu-id="538c9-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="538c9-161">二重書き込みでは、Finance and Operations アプリと Common Data Service 間のデータ フローを自動化します。</span><span class="sxs-lookup"><span data-stu-id="538c9-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="538c9-162">将来のリリースでは、Dynamics 365 のモデル駆動アプリ (顧客、連絡先、見積、注文など) の概念が、中規模市場および本社の顧客に縮小増幅されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="538c9-163">最初のリリースでは、自動化のほとんどは二重書き込みソリューションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="538c9-164">今後のリリースでは、これらのソリューションは Common Data Service に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="538c9-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="538c9-165">Common Data Service への今後の変更点を理解することにより、長期的に実績を節約することができます。</span><span class="sxs-lookup"><span data-stu-id="538c9-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="538c9-166">次に重要変更のいくつかを挙げます。</span><span class="sxs-lookup"><span data-stu-id="538c9-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="538c9-167">Common Data Service に会社や関係者などの新しい概念が追加されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="538c9-168">これらの概念は、Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service、および Dynamics 365 Field Service など、Common Data Service に構築されているすべてのアプリに影響します。</span><span class="sxs-lookup"><span data-stu-id="538c9-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="538c9-169">活動とメモは統合されており、C1s (システムのユーザー) と C2s (システムの顧客) の両方をサポートするように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="538c9-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="538c9-170">次に Common Data Service の変更のいくつかを挙げます。</span><span class="sxs-lookup"><span data-stu-id="538c9-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="538c9-171">10 進データ型によって金額データ型が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="538c9-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="538c9-172">日付の有効期間は、過去、現在、将来のデータを同じ場所にサポートします。</span><span class="sxs-lookup"><span data-stu-id="538c9-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="538c9-173">通貨と為替レートはより詳細にサポートされ、**為替レート**のアプリケーション プログラミング インターフェイス (API) が更新されます。</span><span class="sxs-lookup"><span data-stu-id="538c9-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="538c9-174">単位換算がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="538c9-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="538c9-175">今後の変更の詳細については、[Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="538c9-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
