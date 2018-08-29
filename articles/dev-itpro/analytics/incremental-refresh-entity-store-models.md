---
title: "エンティティ ストア モデルの差分更新オプション"
description: "差分更新は、モデルによって参照されるオブジェクトの変更に合わせてエンティティ ストア モデルを更新するためのオプションです。"
author: tjvass
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-31
ms.dyn365.ops.version: Platform update 16
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e7dfa56bb20fe58049c364217fbeec7a7d53c4d1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="incremental-refresh-option-for-entity-store-models"></a><span data-ttu-id="e5534-103">エンティティ ストア モデルの差分更新オプション</span><span class="sxs-lookup"><span data-stu-id="e5534-103">Incremental refresh option for Entity store models</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

## <a name="what-are-entity-store-models"></a><span data-ttu-id="e5534-104">エンティティ ストア モデルとはなんですか。</span><span class="sxs-lookup"><span data-stu-id="e5534-104">What are entity store models?</span></span>
<span data-ttu-id="e5534-105">エンティティ ストア モデルは、レポートおよび分析ツールの業務データのアクセス可能な表示を提供するために、Microsoft Dynamics 365 for Finance and Operations で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5534-105">Entity store models are used in Microsoft Dynamics 365 for Finance and Operations to provide customers with accessible views of business data for reporting and analytical tools.</span></span> <span data-ttu-id="e5534-106">エンティティ ストア モデルは、アプリケーション メタデータの一部として提供され、特定の業務プロセスに関連付けられているデータセットとリレーションシップの集合として表すことができます。</span><span class="sxs-lookup"><span data-stu-id="e5534-106">Delivered as part of the application metadata, entity store models can be described as collections of data sets and relationships associated with a particular business process.</span></span> <span data-ttu-id="e5534-107">モデルには多くの場合、営業活動とパフォーマンスの分析に役立つルート データ ソースおよび一連の関連ビューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5534-107">Models often contain a root data source and a series of related views that are useful in analyzing business activities and performance.</span></span> 

<span data-ttu-id="e5534-108">たとえば、顧客回収および元帳活動は、報告と分析のためエンティティ格納モデルを必要とする業務プロセスの例です。</span><span class="sxs-lookup"><span data-stu-id="e5534-108">For instance, customer collections and ledger activity are examples of business processes that require an entity store model for reporting and analytics.</span></span> <span data-ttu-id="e5534-109">これらの表示は、集計の測定を使用してアプリケーション メタデータで定義され、ダッシュボードや電子申告に埋め込まれた視覚エフェクトのような、大量に消費するデータのソースとなるよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="e5534-109">Defined in the application metadata using aggregate measurements, these views are designed to be the source of data for high-volume consumers like visualizations that are embedded in dashboards and electronic reports.</span></span>

<span data-ttu-id="e5534-110">エンティティ ストアは、Finance and Operations トランザクション データベースおよび Excel または Power BI.com のような外部レポートや分析ツールによって消費された公開済エンドポイント間の中間のキャッシュとして機能します。</span><span class="sxs-lookup"><span data-stu-id="e5534-110">The entity store functions as an intermediary cache between the Finance and Operations transactional database and the published end-points consumed by external reporting and analytical tooling like Excel or Power BI.com.</span></span> <span data-ttu-id="e5534-111">エンティティ ストアは、ソリューションの報告と監視によって消費されるメモリがウェブ アプリケーションのアクティブなユーザー セッションをサポートするリソースを干渉しないようにします。</span><span class="sxs-lookup"><span data-stu-id="e5534-111">Entity store ensures the memory consumed by reporting and monitoring solutions do not interfere with resources supporting active user sessions in the web application.</span></span> <span data-ttu-id="e5534-112">クラウド ホスト サービスでは、システム管理者による更新スケジュールの管理に基づくエンティティ ストア モデルが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="e5534-112">The cloud-hosted service automatically updates entity store models based on a refresh schedule managed by the system administrator.</span></span> 

<span data-ttu-id="e5534-113">次の図は、レポートと分析ツールのビジネス データの管理を示します。</span><span class="sxs-lookup"><span data-stu-id="e5534-113">The following diagram illustrates the management of business data for reporting and analytics tooling.</span></span>

<span data-ttu-id="e5534-114">[![差分更新](./media/Incremental-refresh-data-flow-diagram.png)](./media/Incremental-refresh-data-flow-diagram.png)</span><span class="sxs-lookup"><span data-stu-id="e5534-114">[![Incremental-refresh](./media/Incremental-refresh-data-flow-diagram.png)](./media/Incremental-refresh-data-flow-diagram.png)</span></span> 

<span data-ttu-id="e5534-115">顧客回収モデルでは、未払いの顧客債務の追跡を担当するビジネス担当者に関連するビューを提供する、一連のデータセットがあります。</span><span class="sxs-lookup"><span data-stu-id="e5534-115">Within the customer collections model, you'll find a group of data sets that provide views relevant to a person within a business responsible for tracking outstanding customer debts.</span></span> <span data-ttu-id="e5534-116">これらのビューは、**分析コード**と呼ばれるカテゴリ フィールドをピボットすることができる、**メジャー**と呼ばれる高度な計算および集計を表示します。</span><span class="sxs-lookup"><span data-stu-id="e5534-116">These views provide advanced calculations and aggregations known as **Measures** that you can pivot on category fields referred to as **Dimensions**.</span></span> <span data-ttu-id="e5534-117">たとえば、アプリケーション スイートには、顧客会衆代行業者用のエンティティ ストア モデルが用意されています。このモデルを使用して、顧客のエイジング バケットを視覚化することができます。</span><span class="sxs-lookup"><span data-stu-id="e5534-117">For example, the application suite provides an entity store model for customer collections agents that can be used to visualize the aging buckets of customers.</span></span> <span data-ttu-id="e5534-118">エンティティ店舗からデータが確定されるため、このモデルにバインドされているレポートは、トランザクション データベースで処理されるデータの待ち時間の代わりに、ミリ単位のデータを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="e5534-118">Because the data is sourced from the entity store, reports bound to this model can visualize the data in milliseconds instead of waiting minutes for the data to be processed in the transactional database.</span></span> <span data-ttu-id="e5534-119">エンティティ格納の詳細については、[エンティティ格納と Power BI の統合の概要](power-bi-integration-entity-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5534-119">For more information about the entity store, see [Overview of Power BI integration with entity store](power-bi-integration-entity-store.md).</span></span>

## <a name="managing-entity-store-models"></a><span data-ttu-id="e5534-120">エンティティ ストア モデルの管理</span><span class="sxs-lookup"><span data-stu-id="e5534-120">Managing entity store models</span></span>
<span data-ttu-id="e5534-121">申告および分析クエリをエンティティ格納にチャネルすることで、システム管理者は、データの時間精度を制御できます。</span><span class="sxs-lookup"><span data-stu-id="e5534-121">By channeling reporting and analytical queries to the entity store, system administrators can control the time accuracy of the data.</span></span> <span data-ttu-id="e5534-122">一部のデータ分析シナリオでは、5-10 分遅延したデータはユーザーに受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="e5534-122">For some data analytics scenarios, data that is delayed by 5-10 minutes will be acceptable by users.</span></span> <span data-ttu-id="e5534-123">ただし、他のタイプのレポート エクスペリエンスには、顧客はほぼリアルタイムの結果を必要とします。</span><span class="sxs-lookup"><span data-stu-id="e5534-123">However, for other types of reporting experiences, customers require near real-time results.</span></span> <span data-ttu-id="e5534-124">エンティティ ストア モデルの戦略の更新を展開する前に、データに関連付けられている時間要件を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e5534-124">It's important to understand time requirements associated with the data before rolling out a refresh strategy for entity store models.</span></span>

<span data-ttu-id="e5534-125">システム管理者は組み込まれているツールを使用して、トランザクションのデータベースで使用可能な最新の更新を使用してエンティティ ストア モデルが更新される頻度を管理します。</span><span class="sxs-lookup"><span data-stu-id="e5534-125">System administrators use built-in tooling to manage the frequency at which entity store models are refreshed with the latest updates available in the transactional database.</span></span> <span data-ttu-id="e5534-126">Finance and Operations は、モデルを最新の状態に維持するために使用される完全な同期および差分同期の両方の戦略をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e5534-126">Finance and Operations supports both a full and incremental synchronization strategy that can be used to keep models up to date.</span></span>

- <span data-ttu-id="e5534-127">**完全同期** - エンティティ ストア内の既存データが削除され、バックグラウンド プロセス中にモデル全体を計算し、実現されます。</span><span class="sxs-lookup"><span data-stu-id="e5534-127">**Full synchronization** - Existing data in the entity store is deleted and the entire model is calculated and materialized during the background process.</span></span>

- <span data-ttu-id="e5534-128">**差分更新** - オブジェクトの削除を含む、トランザクション データベースの更新は、エンティティ ストア モデルと同期されます。</span><span class="sxs-lookup"><span data-stu-id="e5534-128">**Incremental refresh** - Updates to the transactional database, including object deletes, are synchronized with the entity store models.</span></span>

### <a name="full-synchronization"></a><span data-ttu-id="e5534-129">完全同期</span><span class="sxs-lookup"><span data-stu-id="e5534-129">Full synchronization</span></span>
<span data-ttu-id="e5534-130">完全な同期では、エンティティ ストア モデルのすべての側面が更新されることが保証されていますが、大規模なデータ セットの場合、プロセスに数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e5534-130">While full synchronization ensures that all aspects of an entity store model are refreshed, the process could take several minutes for large data sets.</span></span> <span data-ttu-id="e5534-131">このため、完全更新の操作は、可能な場合は営業時間外にのみ実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5534-131">For this reason, it's recommended that full-refresh operations are only performed during non-business hours where possible.</span></span>

### <a name="incremental-refresh"></a><span data-ttu-id="e5534-132">差分更新</span><span class="sxs-lookup"><span data-stu-id="e5534-132">Incremental refresh</span></span>
<span data-ttu-id="e5534-133">差分更新は、プラットフォーム更新プログラム 16 以降で使用できる、モデルによって参照されるオブジェクトの変更に合わせてエンティティ ストア モデルを更新するためのオプションです。</span><span class="sxs-lookup"><span data-stu-id="e5534-133">Incremental refresh, available starting in Platform update 16, is an option for updating entity store models in response to changes in objects referenced by the model.</span></span> <span data-ttu-id="e5534-134">これらは、エンティティ ストアの更新中にデルタ処理エンジンによって検出されるモデル内のルート属性の変更です。</span><span class="sxs-lookup"><span data-stu-id="e5534-134">These are changes to root attributes within a model that are detected by the delta processing engine during an entity store refresh.</span></span> <span data-ttu-id="e5534-135">これには、フィールドの参照を使用する一意に識別できるエンティティ店舗モデル コレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5534-135">This includes entity store model collections that can be uniquely identified using a field reference.</span></span> <span data-ttu-id="e5534-136">システム管理者は Finance and Operations に付属のエンティティ ストア管理ツールを使用して、計検出ロジックでサポートされているエンティティ ストア モデルを識別します。</span><span class="sxs-lookup"><span data-stu-id="e5534-136">System administrators can use the entity store management tooling provided with Finance and Operations to identify entity store models supported by the incremental delta detection logic.</span></span>

> [!Note]
> <span data-ttu-id="e5534-137">モデルのすべての詳細が最新であることを保証するために、インクリメンタル リフレッシュ オプションを利用するモデルを含む、すべてのモデルに対して完全な同期を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5534-137">We recommend that you occasionally perform a full synchronization for all models, including those that take advantage of the incremental refresh option, to ensure all details of the model are up to date.</span></span>

## <a name="can-i-have-an-entity-store-model-that-uses-both-incremental-and-full-refresh"></a><span data-ttu-id="e5534-138">差分と完全更新の両方を使用するエンティティ ストア モデルを持つことはできますか？</span><span class="sxs-lookup"><span data-stu-id="e5534-138">Can I have an entity store model that uses both incremental and full-refresh?</span></span> 
<span data-ttu-id="e5534-139">この時点ではありません。</span><span class="sxs-lookup"><span data-stu-id="e5534-139">Not at this time.</span></span> <span data-ttu-id="e5534-140">現在、差分更新プロセスでサポートされているモデリング集計データ パターンのコレクションの拡大に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="e5534-140">We are currently working to expand the collection of aggregate data modelling patterns supported by the incremental refresh process.</span></span> <span data-ttu-id="e5534-141">拡張機能は、将来のプラットフォームの更新プログラムの一部として定期的に配信されます。</span><span class="sxs-lookup"><span data-stu-id="e5534-141">Enhancements will be delivered routinely as part of future platform updates.</span></span>

<span data-ttu-id="e5534-142">差分更新オプションを使用したエンティティ格納モデルの管理操作のスクリーン ショットです。</span><span class="sxs-lookup"><span data-stu-id="e5534-142">Here's a screenshot of the entity store model administration experience using incremental refresh options.</span></span>

<span data-ttu-id="e5534-143">[![増分管理](./media/Entity-Store-model-management.png)](./media/Entity-Store-model-management.png)</span><span class="sxs-lookup"><span data-stu-id="e5534-143">[![Incremental-administration](./media/Entity-Store-model-management.png)](./media/Entity-Store-model-management.png)</span></span> 

<span data-ttu-id="e5534-144">システム管理者は、エンティティ ストア モデル管理ページを使用して、Finance and Operations トランザクション データベースと同期データのスケジュールを定義します。</span><span class="sxs-lookup"><span data-stu-id="e5534-144">System administrators use the entity store model management page to define the schedule for synchronizing data with the Finance and Operations transactional database.</span></span> <span data-ttu-id="e5534-145">エンティティ格納管理ツールの使用方法の詳細については、[エンティティ格納モデル更新のスケジューリング](aggregate-measurements-refreshed-incrementally.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5534-145">For more information about using the entity store administration tools, see [Scheduling entity store model updates](aggregate-measurements-refreshed-incrementally.md).</span></span>

