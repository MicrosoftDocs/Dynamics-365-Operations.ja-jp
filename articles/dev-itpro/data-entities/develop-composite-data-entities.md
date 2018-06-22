---
title: "複合データ エンティティの開発"
description: "複合エンティティは、相互に関連する複数のエンティティを利用して単一のエンティティを構築できる概念です。"
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 18411
ms.assetid: 1cb19868-cbfd-4f45-bc47-39b9f303583d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a44a74752c08e37e896e56365f8ef315c5860f8a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="develop-composite-data-entities"></a><span data-ttu-id="b8ee9-103">複合データ エンティティの開発</span><span class="sxs-lookup"><span data-stu-id="b8ee9-103">Develop composite data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8ee9-104">複合エンティティは、相互に関連する複数のエンティティを利用して単一のエンティティを構築できる概念です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-104">A composite entity is a concept that allows you to build a single entity by leveraging multiple entities that are related to each other.</span></span> 

<a name="what-is-a-composite-entity"></a><span data-ttu-id="b8ee9-105">複合エンティティとは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="b8ee9-105">What is a composite entity?</span></span>
---------------------------

<span data-ttu-id="b8ee9-106">複合エンティティは、互いに関連する複数のエンティティを活用して単一のエンティティを構築できるコンセプトです。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-106">Composite entity is concept that allows you to build a single entity by leveraging multiple entities that are related to each other.</span></span> <span data-ttu-id="b8ee9-107">この概念は、エンティティを販売ヘッダー/行、請求書ヘッダー/明細および仕入先カタログなどの単一の文書として表すことができるシナリオで頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-107">The concept is heavily used in scenarios where an entity can be represented as a single document, like Sales header/line, Invoice header/line and Vendor Catalog.</span></span> <span data-ttu-id="b8ee9-108">この概念は、同期 OData シナリオではなく非同期統合シナリオに適用され、データ管理プラットフォームからのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-108">This concept is applicable in asynchronous integration scenarios rather than synchronous OData scenarios, and it will only be supported from a data management platform.</span></span> <span data-ttu-id="b8ee9-109">X++ には複合エンティティ用のプログラム的なインターフェイスはありません。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-109">There is no programmatic interface for composite entities in X++.</span></span> <span data-ttu-id="b8ee9-110">XML ファイルに基づくインポート/エクスポートの一部であるデータ管理プラットフォームのみでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-110">It is only supported for a data management platform that is part of XML file-based imports/exports.</span></span>

## <a name="example"></a><span data-ttu-id="b8ee9-111">例</span><span class="sxs-lookup"><span data-stu-id="b8ee9-111">Example</span></span>
<span data-ttu-id="b8ee9-112">売上ヘッダーと販売明細行は、システムの 2 つの異なるエンティティです。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-112">Sales Header and Sales Line are two different entities in the system.</span></span> <span data-ttu-id="b8ee9-113">顧客の要求がそのヘッダーを示し、明細行が 1 つのドキュメントの一部である場合、これら 2 つのエンティティは複合エンティティとしてマージすることができます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-113">In case the customer requirement suggests that header and lines are part of a single document, then these two entities can be merged as a composite entity.</span></span> <span data-ttu-id="b8ee9-114">サンプル販売注文エンティティ: 複合エンティティ (MySalesTableCompositeEntity) は、販売注文ヘッダー エンティティ (MySalesTableEntity) と販売注文明細行エンティティ (MySalesTableLineEntity) から構成される販売注文ドキュメントを表します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-114">Sample sales order entity: The composite entity (MySalesTableCompositeEntity) represents a sales orders document which is comprised of Sales Order header entity (MySalesTableEntity) and Sales Order Line entity (MySalesTableLineEntity).</span></span> <span data-ttu-id="b8ee9-115">[![DevelopingCompositeEntities (17)](./media/developingcompositeentities-17-1024x290.png)](./media/developingcompositeentities-17.png) リンクされたエンティティに基づいて、これらのエンティティは、エンティティの埋め込み要素タグを持つ XML ドキュメントとして公開されます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-115">[![DevelopingCompositeEntities (17)](./media/developingcompositeentities-17-1024x290.png)](./media/developingcompositeentities-17.png) Based on the linked entities, these entities can be exposed as an XML document with embedded element tags for entities.</span></span> <span data-ttu-id="b8ee9-116">XML はデータ管理で複合エンティティを公開する唯一の方法です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-116">XML is the only way to expose a composite entity in data management.</span></span>

    <?xml version="1.0" encoding="utf-8"?>
    <Document>

    <MySalesTableEntity SalesID="SO1" CurrencyCode="USD" CustAccount="Acc001">
    <MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="1000" LineNum="1.00" SalesID="SO1"/>
    <MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="4401" LineNum="2.00" SalesID="SO1"/>
    </MySalesTableEntity>

    <MySalesTableEntity SalesID="SO2" CurrencyCode="USD" CustAccount="Acc002">
    <MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="4402" LineNum="1.00" SalesID="SO2"/>
    </MySalesTableEntity>

    </Document>

<span data-ttu-id="b8ee9-117">XML 内の各ノードでは、個々のエンティティから属性を表します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-117">Each node in the XML represents attributes from an individual entity.</span></span> <span data-ttu-id="b8ee9-118">たとえば - &lt;MySalesTableEntity SalesID="SO1" CurrencyCode="USD" CustAccount="Acc001"&gt; SalesId、CurrencyCode および CustAccount は MySalesTableEntity からの属性です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-118">For example - &lt;MySalesTableEntity SalesID="SO1" CurrencyCode="USD" CustAccount="Acc001"&gt; SalesId, CurrencyCode and CustAccount are attributes from MySalesTableEntity.</span></span>

## <a name="building-the-composite-entity"></a><span data-ttu-id="b8ee9-119">複合エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="b8ee9-119">Building the composite entity</span></span>
<span data-ttu-id="b8ee9-120">データ モデルの下に複合データ エンティティのノードがあります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-120">There is a node for composite data entities under Data model.</span></span> <span data-ttu-id="b8ee9-121">MySalesTableEntity の例を取り上げてみましょう。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-121">Let’s take the example of MySalesTableEntity.</span></span>

### <a name="step-1-identify-and-create-the-individual-entities-for-the-composite-entity"></a><span data-ttu-id="b8ee9-122">手順 1: 複合エンティティの個々のエンティティを識別して作成する</span><span class="sxs-lookup"><span data-stu-id="b8ee9-122">Step 1: Identify and create the individual entities for the composite entity</span></span>

<span data-ttu-id="b8ee9-123">エンティティが相互に関連していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-123">Make sure that the entities are related to each other.</span></span> <span data-ttu-id="b8ee9-124">この例では、個々のエンティティは MySalesTableEntity および MySalesLineEntity です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-124">In this example the individual entities are MySalesTableEntity and MySalesLineEntity.</span></span>

### <a name="step-2-add-relations-between-individual-entities"></a><span data-ttu-id="b8ee9-125">手順 2: 個々のエンティティの間の関係を追加する</span><span class="sxs-lookup"><span data-stu-id="b8ee9-125">Step 2: Add relations between individual entities</span></span>

<span data-ttu-id="b8ee9-126">リレーション ノードの親エンティティへのリレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-126">Add a relation to parent entity in the relations node.</span></span> <span data-ttu-id="b8ee9-127">例 – MySalesLineEntity は、MySalesTableEntity と関係性があります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-127">Example – MySalesLineEntity has relationship to MySalesTableEntity.</span></span>  <span data-ttu-id="b8ee9-128">[![DevelopingCompositeEntities (18)](./media/developingcompositeentities-18.png)](./media/developingcompositeentities-18.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-128">[![DevelopingCompositeEntities (18)](./media/developingcompositeentities-18.png)](./media/developingcompositeentities-18.png)</span></span>

### <a name="step-3-create-a-new-composite-entity"></a><span data-ttu-id="b8ee9-129">手順 3: 新しい複合エンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="b8ee9-129">Step 3: Create a new composite entity</span></span>

1.  <span data-ttu-id="b8ee9-130">**Composite entity** タイプの新しい **Dynamics 365** コンポーネント品目をプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-130">Add a new **Dynamics 365** artifact item of type **Composite entity** to the project.</span></span>
2.  <span data-ttu-id="b8ee9-131">デザイナー モードで、エンティティを右クリックし、**新しいルート データ エンティティ参照**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-131">In designer mode, right-click the entity and select **New Root Data Entity Reference**.</span></span> <span data-ttu-id="b8ee9-132">[![DevelopingCompositeEntities (2)](./media/developingcompositeentities-2.png)](./media/developingcompositeentities-2.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-132">[![DevelopingCompositeEntities (2)](./media/developingcompositeentities-2.png)](./media/developingcompositeentities-2.png)</span></span>
3.  <span data-ttu-id="b8ee9-133">親データ エンティティにデータ エンティティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-133">Set the data entity to parent data entity.</span></span> <span data-ttu-id="b8ee9-134">ここでは、MySalesTableEntity です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-134">In this case its MySalesTableEntity.</span></span>
4.  <span data-ttu-id="b8ee9-135">親エンティティ ノードを右クリックし、**新しい埋め込みデータ エンティティ参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-135">Right-click the parent entity node and select **New Embedded Data Entity Reference**.</span></span> <span data-ttu-id="b8ee9-136">[![DevelopingCompositeEntities (3)](./media/developingcompositeentities-3.png)](./media/developingcompositeentities-3.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-136">[![DevelopingCompositeEntities (3)](./media/developingcompositeentities-3.png)](./media/developingcompositeentities-3.png)</span></span>
5.  <span data-ttu-id="b8ee9-137">子エンティティとして埋め込みデータ エンティティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-137">Set the embedded data entity as the child entity.</span></span> <span data-ttu-id="b8ee9-138">ここでは、MySalesLineEntity です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-138">In this case it is MySalesLineEntity.</span></span>
6.  <span data-ttu-id="b8ee9-139">埋め込みデータ エンティティ プロパティのドロップダウン リストから **関係** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-139">Set the **Relation** property from the drop-down list on the embedded data entity properties.</span></span>  <span data-ttu-id="b8ee9-140">[![DevelopingCompositeEntities (4)](./media/developingcompositeentities-4.png)](./media/developingcompositeentities-4.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-140">[![DevelopingCompositeEntities (4)](./media/developingcompositeentities-4.png)](./media/developingcompositeentities-4.png)</span></span>
7.  <span data-ttu-id="b8ee9-141">複合エンティティには、複数レベルの子エンティティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-141">Composite entity supports multi-level child entities.</span></span>

### <a name="step-4-create-relationships-between-staging-tables"></a><span data-ttu-id="b8ee9-142">手順 4: ステージング テーブル間の関係を作成する</span><span class="sxs-lookup"><span data-stu-id="b8ee9-142">Step 4: Create relationships between staging tables</span></span>

<span data-ttu-id="b8ee9-143">ナチュラル キーに基づいたエンティティ ステージング テーブルの親と子間の関係を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-143">You need to create relationships between the parent and child entity staging tables based on the natural keys.</span></span> <span data-ttu-id="b8ee9-144">たとえば、MySalesTable および MySalesLine のステージング テーブルは、SalesID、DefinitionGroup、および ExecutionId によってリンクされます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-144">For example, staging tables for MySalesTable and MySalesLine are linked by SalesID, DefinitionGroup, and ExecutionId.</span></span>

1.  <span data-ttu-id="b8ee9-145">MySalesLineStaging テーブルの外部キー関係を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-145">Add a foreign key relation on MySalesLineStaging table.</span></span>  <span data-ttu-id="b8ee9-146">[![DevelopingCompositeEntities (5)](./media/developingcompositeentities-5.png)](./media/developingcompositeentities-5.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-146">[![DevelopingCompositeEntities (5)](./media/developingcompositeentities-5.png)](./media/developingcompositeentities-5.png)</span></span>
2.  <span data-ttu-id="b8ee9-147">複合データ エンティティに関連付けられているすべてのステージング テーブルに、2 つの列、RowId と ParentRowId (int 型) を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-147">Add two columns, RowId and ParentRowId (type int), on all the staging tables associated with the composite data entity.</span></span> <span data-ttu-id="b8ee9-148">列のプロパティについては、SysCompositeHeaderStaging テーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-148">Refer to SysCompositeHeaderStaging table for the columns properties.</span></span> <span data-ttu-id="b8ee9-149">[![DevelopingCompositeEntities (7)](./media/developingcompositeentities-7.png)](./media/developingcompositeentities-7.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-149">[![DevelopingCompositeEntities (7)](./media/developingcompositeentities-7.png)](./media/developingcompositeentities-7.png)</span></span>

<span data-ttu-id="b8ee9-150">これらの列は、ターゲット データのランタイム リレーションシップを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-150">These columns are used to define runtime relationships during the target data movement.</span></span>

-   <span data-ttu-id="b8ee9-151">RowId、ParentRowid、DefinitionGroup、および ExecutionId を含むステージング テーブルにクラスター インデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-151">Create a cluster index on the staging tables which includes RowId, ParentRowid,DefinitionGroup, and ExecutionId.</span></span> <span data-ttu-id="b8ee9-152">これは、パフォーマンス上の理由によります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-152">This is for performance reasons.</span></span>
-   <span data-ttu-id="b8ee9-153">コンポーネントをコンパイルして同期します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-153">Compile and synchronize the artifacts.</span></span>

### <a name="step-5-set-up-the-metadata-for-dmfentity"></a><span data-ttu-id="b8ee9-154">手順 5: DMFEntity のメタデータを設定する</span><span class="sxs-lookup"><span data-stu-id="b8ee9-154">Step 5: Set up the metadata for DMFEntity</span></span>

<span data-ttu-id="b8ee9-155">ローカル テストで、複合エンティティ メタデータは更新される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-155">For local testing the composite entity metadata needs to be refreshed.</span></span>

1.  <span data-ttu-id="b8ee9-156">**DIXF パラメータ &gt; エンティティ設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-156">Go to **DIXF Parameters &gt; Entity settings**.</span></span> <span data-ttu-id="b8ee9-157">**エンティティ リストの更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-157">Click **Refresh entity list**.</span></span>  <span data-ttu-id="b8ee9-158">[![DevelopingCompositeEntities (8)](./media/developingcompositeentities-8-1024x212.png)](./media/developingcompositeentities-8.png)</span><span class="sxs-lookup"><span data-stu-id="b8ee9-158">[![DevelopingCompositeEntities (8)](./media/developingcompositeentities-8-1024x212.png)](./media/developingcompositeentities-8.png)</span></span>
2.  <span data-ttu-id="b8ee9-159">別の方法として、複合エンティティ リストのメタデータを更新するために次のジョブを書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-159">Alternately, you can write the following job to refresh the composite entity list metadata.</span></span>

        DMFDataPopulation::refreshCompositeEntityList();

3.  <span data-ttu-id="b8ee9-160">ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-160">Execute the job.</span></span> <span data-ttu-id="b8ee9-161">エンティティ ルックアップに必要なメタデータが更新されます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-161">This refreshes the metadata required for the entity lookup.</span></span>

<span data-ttu-id="b8ee9-162">**注記:** 現在これが回避方法です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-162">**Note:** Currently this is a workaround.</span></span> <span data-ttu-id="b8ee9-163">今後、コンパイル/同期時にリストを更新する機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-163">In the future a feature will be enabled to refresh the list at compile/sync time.</span></span>

### <a name="step-6-test-the-entity-locally"></a><span data-ttu-id="b8ee9-164">手順 6: ローカル エンティティをテストする</span><span class="sxs-lookup"><span data-stu-id="b8ee9-164">Step 6: Test the entity locally</span></span>

<span data-ttu-id="b8ee9-165">DIXF 標準プロセスからの通常のエンティティとして、データをインポートおよびエクスポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-165">We recommend that you import and export the data as a normal entity from DIXF standard process.</span></span> <span data-ttu-id="b8ee9-166">エンティティのインポートとエクスポートの以下の手順をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-166">Refer to the following the steps for importing and exporting entity.</span></span> <span data-ttu-id="b8ee9-167">**注記:** ソース タイプの XML-属性または XML-要素は、複合エンティティでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-167">**Note:** The source types of XML-Attribute or XML-Element are supported for composite entity.</span></span>

## <a name="import-a-composite-entity"></a><span data-ttu-id="b8ee9-168">複合エンティティのインポート</span><span class="sxs-lookup"><span data-stu-id="b8ee9-168">Import a composite entity</span></span>
1.  <span data-ttu-id="b8ee9-169">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-169">Click **Import**.</span></span>
2.  <span data-ttu-id="b8ee9-170">**名前**、**ソース データ フォーマット**、および**エンティティ名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-170">Enter **Name**, **Source data format**, and **Entity name**.</span></span>
3.  <span data-ttu-id="b8ee9-171">**ソース データ形式** は、xml-attribute または xml-element です。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-171">The **Source data format** is either xml-attribute or xml-element.</span></span>
4.  <span data-ttu-id="b8ee9-172">**今すぐインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-172">Click **Import now**.</span></span>
5.  <span data-ttu-id="b8ee9-173">作成/更新/保留中のレコードの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-173">The number of records created/updated/pending are shown.</span></span>

## <a name="export-a-composite-entity"></a><span data-ttu-id="b8ee9-174">複合エンティティをエキスポート</span><span class="sxs-lookup"><span data-stu-id="b8ee9-174">Export a composite entity</span></span>
1.  <span data-ttu-id="b8ee9-175">**エクスポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-175">Click **Export**.</span></span>
2.  <span data-ttu-id="b8ee9-176">**名前**、**ソース データ フォーマット**、**およびエンティティ名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-176">Enter **Name**, **Source data format**, **and Entity name**.</span></span>
3.  <span data-ttu-id="b8ee9-177">**エンティティの追加**および**今すぐエクスポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-177">Click **Add entity** and **Export now**.</span></span>
4.  <span data-ttu-id="b8ee9-178">**ダウンロード パッケージ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-178">Click **Download package**.</span></span>

## <a name="general-troubleshooting-guidelines"></a><span data-ttu-id="b8ee9-179">トラブルシューティングの一般的なガイドライン</span><span class="sxs-lookup"><span data-stu-id="b8ee9-179">General troubleshooting guidelines</span></span>
-   <span data-ttu-id="b8ee9-180">問題: エクスポートされた複合 XML ファイルがインポートされません。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-180">Issue: The exported composite XML file is not imported.</span></span> <span data-ttu-id="b8ee9-181">これを生成するシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-181">The scenario that produces this is:</span></span>
    -   <span data-ttu-id="b8ee9-182">複合エンティティのファイルをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-182">Export a file for composite entity.</span></span>
    -   <span data-ttu-id="b8ee9-183">同じファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-183">Import the same file.</span></span>
    -   <span data-ttu-id="b8ee9-184">マッピングに失敗し、ファイルがインポートされません。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-184">Mapping fails and the file is not imported.</span></span>
-   <span data-ttu-id="b8ee9-185">根本原因:</span><span class="sxs-lookup"><span data-stu-id="b8ee9-185">Root cause:</span></span>
    -   <span data-ttu-id="b8ee9-186">エクスポートされたファイルに行または関連する子エンティティ情報があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-186">Check if the exported file has lines or related child entity information.</span></span>
    -   <span data-ttu-id="b8ee9-187">明細行または関連する子エンティティについての情報がある場合、明細行はインポート中にマップされません。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-187">If there no lines or related child entity information, then the lines will not be mapped during import.</span></span>
-   <span data-ttu-id="b8ee9-188">解決策: </span><span class="sxs-lookup"><span data-stu-id="b8ee9-188">Resolution:</span></span>
    -   <span data-ttu-id="b8ee9-189">すべての子のエンティティを含むサンプル ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-189">Create a sample file with all of the child entities.</span></span>
    -   <span data-ttu-id="b8ee9-190">このファイルは初期マッピングにのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-190">Use this file for initial mapping only.</span></span>
    -   <span data-ttu-id="b8ee9-191">マッピングに成功したら、明細行データがエンティティに含まれていない実際のファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-191">When the mapping is successful, import the actual file which does not have the line data into the entity.</span></span> <span data-ttu-id="b8ee9-192">再インポートを使用するか、新しいファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-192">Use reimport or upload a new file.</span></span>
    -   <span data-ttu-id="b8ee9-193">レコードの有効性に応じて、部分データ (空の子レコード) を含むファイルをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8ee9-193">This should import files with partial data (blank child records), depending on the validity of the records.</span></span>





