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
ms.openlocfilehash: 8957065bcadc3f33adb60c2a8f2be78710289631
ms.sourcegitcommit: d03f301633175b15d46690fc97067820bf21579f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2020
ms.locfileid: "3775150"
---
# <a name="dual-write-overview"></a><span data-ttu-id="72ace-104">二重書き込みの概要</span><span class="sxs-lookup"><span data-stu-id="72ace-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="72ace-105">二重書き込みとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="72ace-105">What is dual-write?</span></span>

<span data-ttu-id="72ace-106">二重書き込みは、Customer Engagement アプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。</span><span class="sxs-lookup"><span data-stu-id="72ace-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="72ace-107">顧客、製品、人材、および業務に関するデータがアプリケーション境界を超えてフローする場合、組織のすべての部門が権利を持つことになります。</span><span class="sxs-lookup"><span data-stu-id="72ace-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="72ace-108">二重書き込みは、Finance and Operations アプリと Common Data Service の間で密に結合された双方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="72ace-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="72ace-109">Finance and Operations アプリでのデータの変更によって Common Data Service 書き込みが行われ、Common Data Service のデータの変更によって Finance and Operations アプリケーションへの書き込みが行われます。</span><span class="sxs-lookup"><span data-stu-id="72ace-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="72ace-110">この自動化されたデータ フローによって、アプリ間で統合されたユーザー エクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![アプリ間のデータの関係](media/dual-write-overview.jpg)

<span data-ttu-id="72ace-112">二重書き込みには、*インフラストラクチャ*の側面と*アプリケーション*の側面の 2 つの側面があります。</span><span class="sxs-lookup"><span data-stu-id="72ace-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="72ace-113">インフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="72ace-113">Infrastructure</span></span>

<span data-ttu-id="72ace-114">二重書き込みインフラストラクチャは、拡張性と信頼性を備えており、次の主な機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="72ace-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="72ace-115">アプリケーション間の同期および双方向のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="72ace-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="72ace-116">同期と、オンラインおよびオフライン/非同期モードでシステムをサポートするための再生、一時停止、キャッチ アップの各モードとの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="72ace-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="72ace-117">アプリケーション間で初期データを同期する機能</span><span class="sxs-lookup"><span data-stu-id="72ace-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="72ace-118">データ管理者の活動とエラー ログの結合ビュー</span><span class="sxs-lookup"><span data-stu-id="72ace-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="72ace-119">カスタム警告としきい値をコンフィギュレーションし、通知をサブスクライブする機能</span><span class="sxs-lookup"><span data-stu-id="72ace-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="72ace-120">フィルタリングと変換のための直観的なユーザー インターフェイス (UI)</span><span class="sxs-lookup"><span data-stu-id="72ace-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="72ace-121">エンティティの相互関係と関係を設定および表示する機能</span><span class="sxs-lookup"><span data-stu-id="72ace-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="72ace-122">標準エンティティとカスタム エンティティおよびマップの両方に対する拡張性</span><span class="sxs-lookup"><span data-stu-id="72ace-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="72ace-123">信頼できるアプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="72ace-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="72ace-124">新しい顧客に対する標準の設定エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="72ace-125">申請</span><span class="sxs-lookup"><span data-stu-id="72ace-125">Application</span></span>

<span data-ttu-id="72ace-126">二重書き込みでは、Finance and Operations アプリと Customer Engagement アプリにおける概念の間にマッピングが作成されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="72ace-127">この統合により、次のシナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="72ace-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="72ace-128">統合された顧客マスター</span><span class="sxs-lookup"><span data-stu-id="72ace-128">Integrated customer master</span></span>
+ <span data-ttu-id="72ace-129">顧客ロイヤルティ カードおよび報酬ポイントへのアクセス</span><span class="sxs-lookup"><span data-stu-id="72ace-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="72ace-130">統一された製品マスタリング エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="72ace-131">組織階層の認識</span><span class="sxs-lookup"><span data-stu-id="72ace-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="72ace-132">統合された仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="72ace-132">Integrated vendor master</span></span>
+ <span data-ttu-id="72ace-133">財務および税参照データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="72ace-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="72ace-134">オンデマンドの価格エンジンのエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="72ace-135">統合された見込み顧客エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="72ace-136">フィールド エージェントを介して社内資産と顧客資産の両方を提供する機能</span><span class="sxs-lookup"><span data-stu-id="72ace-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="72ace-137">統合された仕入れから支払エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="72ace-138">顧客データおよびドキュメントに関する統合された活動とメモ</span><span class="sxs-lookup"><span data-stu-id="72ace-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="72ace-139">手持在庫状態および詳細を検索する機能</span><span class="sxs-lookup"><span data-stu-id="72ace-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="72ace-140">プロジェクトの現金化エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="72ace-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="72ace-141">関係者の概念を使用して複数の住所と役割を処理する機能</span><span class="sxs-lookup"><span data-stu-id="72ace-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="72ace-142">ユーザーに対する単一のソース管理</span><span class="sxs-lookup"><span data-stu-id="72ace-142">Single source management for users</span></span>
+ <span data-ttu-id="72ace-143">小売業とマーケティング向けの統合チャネル</span><span class="sxs-lookup"><span data-stu-id="72ace-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="72ace-144">プロモーションと割引の可視性</span><span class="sxs-lookup"><span data-stu-id="72ace-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="72ace-145">サービス要求機能</span><span class="sxs-lookup"><span data-stu-id="72ace-145">Request-for-service functions</span></span>
+ <span data-ttu-id="72ace-146">合理化されたサービス工程</span><span class="sxs-lookup"><span data-stu-id="72ace-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="72ace-147">二重書き込みを使用する主な理由</span><span class="sxs-lookup"><span data-stu-id="72ace-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="72ace-148">二重書き込みにより、Microsoft Dynamics 365 アプリケーション間でデータの統合が提供されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="72ace-149">この信頼性の高いフレームワークでは、環境をリンクして、さまざまなビジネス アプリケーションを連携させることができます。</span><span class="sxs-lookup"><span data-stu-id="72ace-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="72ace-150">二重書き込みを使用する必要がある主な理由は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="72ace-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="72ace-151">二重書き込みは、Finance and Operations アプリと Dynamics 365 の モデル駆動型アプリの間で密結合、ほぼリアルタイム、および双方向の統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="72ace-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="72ace-152">この統合により、すべてのビジネスソリューションに対して、1 つの停止ショップとして Microsoft Dynamics 365 が作成されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="72ace-153">Dynamics 365 Finance と Dynamics 365 Supply Chain Management を使用しているが、顧客関係管理 (CRM) に対して Microsoft 以外のソリューションを使用している顧客は、二重書き込みをサポートするために Dynamics 365 に移行しています。</span><span class="sxs-lookup"><span data-stu-id="72ace-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="72ace-154">顧客、製品、工程、プロジェクト、およびインターネット オブ シングス (IoT) のデータは、自動的に二重書き込みによって Common Data Service にフローします。</span><span class="sxs-lookup"><span data-stu-id="72ace-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="72ace-155">この接続は、Microsoft Power Platform の展開に関心のある企業にとって便利です。</span><span class="sxs-lookup"><span data-stu-id="72ace-155">This connection is useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="72ace-156">二重書き込みインフラストラクチャは、コードなし/ロー コード原則に従います。</span><span class="sxs-lookup"><span data-stu-id="72ace-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="72ace-157">標準のテーブルからテーブルへのマップを拡張したり、カスタム マップを含めたりするには、最小限のエンジニアリング実績が要求されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="72ace-158">二重書き込みでは、オンライン モードとオフライン モードの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="72ace-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="72ace-159">Microsoft は、オンラインとオフライン モードのサポートを提供している唯一の会社です。</span><span class="sxs-lookup"><span data-stu-id="72ace-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="72ace-160">二重書き込みは、Customer Engagement アプリの開発者と設計者にとって何を意味しますか?</span><span class="sxs-lookup"><span data-stu-id="72ace-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="72ace-161">二重書き込みは、Finance and Operations アプリと Customer Engagement アプリ間のデータ フローを自動化します。</span><span class="sxs-lookup"><span data-stu-id="72ace-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="72ace-162">二重書き込みは、Common Data Service にインストールされている 2 つの AppSource ソリューションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="72ace-162">Dual-write consists of two AppSource solutions that are installed on Common Data Service.</span></span> <span data-ttu-id="72ace-163">ソリューションは、Common Data Service のエンティティ スキーマ、プラグイン、ワークフローを展開して、ERP サイズに合わせて拡張できるようにします。</span><span class="sxs-lookup"><span data-stu-id="72ace-163">The solutions expand the entity schema, plugins, and workflows on Common Data Service so that they can scale to ERP size.</span></span> <span data-ttu-id="72ace-164">実装を成功させるためには、Customer Engagement アプリの開発者や設計者は、これらの変更点を理解し、Finance and Operations アプリ上で担当者と協力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72ace-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="72ace-165">Finance and Operations アプリケーションと同等の機能を作成するために、二重書き込みは Common Data Service スキーマにいくつかの重要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="72ace-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Common Data Service schema.</span></span> <span data-ttu-id="72ace-166">計画を理解すれば、将来の設計や開発のやり直しを回避できます。</span><span class="sxs-lookup"><span data-stu-id="72ace-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="72ace-167">二重書き込み AppSource パッケージがインストールされると、Common Data Service は会社や関係者などの新しい概念を持つようになります。</span><span class="sxs-lookup"><span data-stu-id="72ace-167">When the dual-write AppSource package is installed, Common Data Service will have new concepts such as company and party.</span></span> <span data-ttu-id="72ace-168">これらの概念は、Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service、Dynamics 365 Field Service を含む、Common Data Service 上に構築されたアプリケーションが、Finance and Operations アプリとシームレスとやりとりするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="72ace-168">These concepts help applications built on Common Data Service, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="72ace-169">活動とメモは統合されており、C1s (システムのユーザー) と C2s (システムの顧客) の両方をサポートするように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="72ace-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="72ace-170">Finance and Operations アプリと Common Data Service 間の通貨転送中のデータ損失を防ぐために、Customer Engagement アプリの通貨のデータ型で小数点以下の桁数を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="72ace-170">To prevent data loss during currency transmission between Finance and Operations apps and the Common Data Service, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="72ace-171">この機能は、既存のレコードをメタデータ レイヤーで新しい拡張状態に自動変換します。</span><span class="sxs-lookup"><span data-stu-id="72ace-171">The feature autotranslates existing records to the new extended state at the metadata layer.</span></span> <span data-ttu-id="72ace-172">このプロセス中に、通貨の値は、money データではなく10進数データに変換され、通貨の値は小数点以下 10 桁をサポートします。</span><span class="sxs-lookup"><span data-stu-id="72ace-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="72ace-173">この機能はオプトインであり、小数点以下 4 桁を超える精度を必要としない組織はオプトインする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="72ace-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="72ace-174">詳細については、[二重書き込みの通貨データ型の移行](currrency-decimal-places.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72ace-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="72ace-175">[日付の有効期間](../../dev-tools/date-effectivity.md) は Common Data Service に追加されます。</span><span class="sxs-lookup"><span data-stu-id="72ace-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Common Data Service.</span></span> <span data-ttu-id="72ace-176">同じエンティティ上の過去、現在、将来のデータをサポートします。</span><span class="sxs-lookup"><span data-stu-id="72ace-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="72ace-177">製品の [単位換算](../../../../supply-chain/pim/tasks/manage-unit-measure.md) では、製品、見積、注文、および請求書がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="72ace-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="72ace-178">今後の変更の詳細については、[二重書き込みの新機能および変更された機能](whats-new-dual-write.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72ace-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

