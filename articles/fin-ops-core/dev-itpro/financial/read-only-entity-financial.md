---
title: 財務分析コードを公開する読み取り専用エンティティの作成
description: このトピックでは、登録済のトランザクションのエンティティを作成する方法について説明します。
author: robinarh
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 273653
ms.assetid: 119610df-3975-43ce-830b-84fe58266321
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: dc0ccf4bf0c4176b0f01a20b7035dd1ca9c6150d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749900"
---
# <a name="create-read-only-entities-that-expose-financial-dimensions"></a><span data-ttu-id="23bfa-103">財務分析コードを公開する読み取り専用エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="23bfa-103">Create read-only entities that expose financial dimensions</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="23bfa-104">このトピックでは、登録されている登録済のトランザクションのエンティティを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-104">In this topic, we describe how to build an entity for registered transactions that are registered.</span></span> 

> [!NOTE] 
> <span data-ttu-id="23bfa-105">このトピックは、ソリューション アーキテクチャ チームの Per Baarsoe Jorgensen から得たものです。</span><span class="sxs-lookup"><span data-stu-id="23bfa-105">This topic comes from Per Baarsoe Jorgensen of the Solutions Architecture team.</span></span> <span data-ttu-id="23bfa-106">顧客と作業時に発生した実際のシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-106">It describes a real-world scenario that we have encountered as we work with customers.</span></span> 

<span data-ttu-id="23bfa-107">配分を使用して適用された財務分析コードと共にすべての仕入先請求明細行のトランザクションを公開しなければならないシナリオを考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="23bfa-107">Imagine a scenario where we must expose all vendor invoice line transactions together with the financial dimensions that were applied through the distributions.</span></span> <span data-ttu-id="23bfa-108">サード パーティのツールによる簡単な消費が不可欠なので、このシナリオ用のエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-108">Because easy consumption by a third-party tool is essential, we will create an entity for this scenario.</span></span> <span data-ttu-id="23bfa-109">結果として、エンティティは他の関連するエンティティと結合する必要はなく、単独で値を提供できるべきです。</span><span class="sxs-lookup"><span data-stu-id="23bfa-109">As a result, the entity should not have to be joined with other related entities but should be able to provide value on its own.</span></span>

<span data-ttu-id="23bfa-110">これらの要件を満たすために、サンプル エンティティを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-110">We will walk through the process of creating a sample entity to meet these requirements.</span></span> <span data-ttu-id="23bfa-111">(これらの手順はすでに文書化されているため、Microsoft Azure DevOps との統合の手順は省略します。)</span><span class="sxs-lookup"><span data-stu-id="23bfa-111">(We will leave out instructions for integrating with Microsoft Azure DevOps, because those steps are already well documented.)</span></span>

## <a name="create-a-basic-entity"></a><span data-ttu-id="23bfa-112">基本エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="23bfa-112">Create a basic entity</span></span>
<span data-ttu-id="23bfa-113">最初のステップは、**新しい品目** を選択して、プロジェクト内に新しい要素を作成することです。.</span><span class="sxs-lookup"><span data-stu-id="23bfa-113">The first step is to create a new element in a project by selecting **New Item**.</span></span> 

<span data-ttu-id="23bfa-114">[![新しい項目](./media/fd-basic.png)](./media/fd-basic.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-114">[![New item](./media/fd-basic.png)](./media/fd-basic.png)</span></span>

<span data-ttu-id="23bfa-115">開いているフォームで、データ モデルの **データ エンティティ** 要素のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-115">In the form that opens, under Data Model, we select the **Data Entity** element type.</span></span>

<span data-ttu-id="23bfa-116">[![データ要素](./media/fd-element.png)](./media/fd-element.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-116">[![Data element](./media/fd-element.png)](./media/fd-element.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="23bfa-117">後で名前を変更できないためエンティティに名前を付けるときは注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="23bfa-117">Be careful when you name the entity, because you can’t rename it later.</span></span>

<span data-ttu-id="23bfa-118">次に、データ エンティティ ウィザードで、適切なプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-118">Next, in the Data Entity wizard, we select the appropriate primary data source.</span></span> <span data-ttu-id="23bfa-119">シナリオでは、このデータ ソースは VendInvoiceTrans です。</span><span class="sxs-lookup"><span data-stu-id="23bfa-119">For our scenario, this data source is VendInvoiceTrans.</span></span>

<span data-ttu-id="23bfa-120">[![データ エンティティ ウィザード](./media/fd-wizard.png)](./media/fd-wizard.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-120">[![Data entity wizard](./media/fd-wizard.png)](./media/fd-wizard.png)</span></span>

<span data-ttu-id="23bfa-121">VendInvoiceTrans の場合のように、ウィザードは自然キーを持たないテーブルを受け入れません。</span><span class="sxs-lookup"><span data-stu-id="23bfa-121">The wizard doesn’t accept tables that don’t have a natural key, as is the case with VendInvoiceTrans.</span></span> <span data-ttu-id="23bfa-122">したがって、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-122">Therefore, we receive the following error message.</span></span>

<span data-ttu-id="23bfa-123">[![ナチュラル キーのエラー](./media/fd-error.png)](./media/fd-error.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-123">[![Natural key error](./media/fd-error.png)](./media/fd-error.png)</span></span>

<span data-ttu-id="23bfa-124">この問題を回避するには、VendGroup などの自然なキーが関連付けられている他のプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-124">The workaround is to select any other primary data source that has a natural key associated, such as VendGroup.</span></span>

<span data-ttu-id="23bfa-125">このデータ ソースは実際には必要ないので、フィールドも必要ありません。</span><span class="sxs-lookup"><span data-stu-id="23bfa-125">Because we don’t really need this data source, we also don’t need any fields for it.</span></span> <span data-ttu-id="23bfa-126">したがって、**すべて選択** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="23bfa-126">Therefore, we clear the **Select all** check box.</span></span>

<span data-ttu-id="23bfa-127">[![すべての選択を解除](./media/fd-wizard2.png)](./media/fd-wizard2.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-127">[![Clear select all](./media/fd-wizard2.png)](./media/fd-wizard2.png)</span></span>

<span data-ttu-id="23bfa-128">最後に、**完了** をクリックして、エンティティのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-128">Finally, we create the template for our entity by clicking **Finish**.</span></span>

## <a name="customize-the-basic-entity"></a><span data-ttu-id="23bfa-129">基本的なエンティティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="23bfa-129">Customize the basic entity</span></span>
<span data-ttu-id="23bfa-130">エンティティ、ステージング テーブル、およびセキュリティ資産が作成され、カスタム エンティティを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="23bfa-130">The entity, staging table, and security assets have been created, and we can now produce our custom entity.</span></span> <span data-ttu-id="23bfa-131">プロジェクトでは、デザイナーで VendorInvoiceTransactionDetailsEntity エンティティを開きます。</span><span class="sxs-lookup"><span data-stu-id="23bfa-131">In the project, we open the VendorInvoiceTransactionDetailsEntity entity in the designer.</span></span> 

<span data-ttu-id="23bfa-132">[![デザイナーの VendorInvoiceTransactionDetailsEntity](./media/fd-designer.png)](./media/fd-designer.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-132">[![VendorInvoiceTransactionDetailsEntity in designer](./media/fd-designer.png)](./media/fd-designer.png)</span></span>

<span data-ttu-id="23bfa-133">デザイナーで、ウィザードに適用したダミー テーブル (VendGroup) を、トランザクション テーブル VendInvoiceTrans に変えます。</span><span class="sxs-lookup"><span data-stu-id="23bfa-133">In the designer, we replace the dummy table (VendGroup) that we applied in the wizard with the transaction table VendInvoiceTrans.</span></span> <span data-ttu-id="23bfa-134">フィールドの追加を選択しなかったため、エンティティのフィールドを削除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="23bfa-134">Because we didn't choose to add the fields, we don't have to remove fields in the entity.</span></span>

<span data-ttu-id="23bfa-135">[![データ エンティティのタイプ](./media/fd-menu.png)](./media/fd-menu.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-135">[![Data Entity Type](./media/fd-menu.png)](./media/fd-menu.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="23bfa-136">このエンティティを使用してトランザクション データを公開するため、エンティティを読み取り専用としてマークすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="23bfa-136">Because we are exposing transactional data by using this entity, it's important that we mark the entity as read-only.</span></span> <span data-ttu-id="23bfa-137">そのため、トップ ノードで **Is read only** プロパティを **Yes** に設定します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-137">Therefore, we set the **Is read only** property to **Yes** on the top node.</span></span> <span data-ttu-id="23bfa-138">勘定配布はバージョン管理されているため、クエリを実行するときに現在のバージョンのみが返されることが重要です。</span><span class="sxs-lookup"><span data-stu-id="23bfa-138">Because accounting distributions are versioned, it's important that only the current version be returned when we query.</span></span> <span data-ttu-id="23bfa-139">したがって、この部分を複数のエンティティ間で簡単に再利用できるようにするビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-139">Therefore, we create a view that makes this part easily reusable across multiple entities.</span></span> 

<span data-ttu-id="23bfa-140">[![VendInvoiceTrans と置き換え](./media/fd-menu2.png)](./media/fd-menu2.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-140">[![Replace with VendInvoiceTrans](./media/fd-menu2.png)](./media/fd-menu2.png)</span></span>

<span data-ttu-id="23bfa-141">プロパティで、**ReferenceDistribution** に **0** の範囲フィルター値、**ReferenceRole** に **1** の範囲フィルター値を代入します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-141">In the properties, we assign **ReferenceDistribution** a range filter value of **0** and **ReferenceRole** a range filter value of **1**.</span></span> <span data-ttu-id="23bfa-142">AccountDistributionReverse データ ソースの結合モード プロパティは、**NoExistsJoin** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-142">The join mode property for the AccountDistributionReverse data source must be **NoExistsJoin**.</span></span> <span data-ttu-id="23bfa-143">新しいビューを配置した後、現在作成している VendorInvoiceTransactionDetailsEntity エンティティに追加できます。</span><span class="sxs-lookup"><span data-stu-id="23bfa-143">After the new view is in place, we can add it to the VendorInvoiceTransactionDetailsEntity entity that we are currently building.</span></span> 

<span data-ttu-id="23bfa-144">[![VendorInvoiceTransactionDetailsEntity の追加](./media/fd-menu3.png)](./media/fd-menu3.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-144">[![Add to VendorInvoiceTransactionDetailsEntity](./media/fd-menu3.png)](./media/fd-menu3.png)</span></span>

## <a name="expose-financial-dimensions-as-fields"></a><span data-ttu-id="23bfa-145">財務分析コードをフィールドとして公開</span><span class="sxs-lookup"><span data-stu-id="23bfa-145">Expose financial dimensions as fields</span></span>
<span data-ttu-id="23bfa-146">次の重要なステップは、財務分析コードをエンティティ上の異なるフィールドとして公開することです。</span><span class="sxs-lookup"><span data-stu-id="23bfa-146">The next important step is to expose the financial dimensions as separate fields on the entity.</span></span> <span data-ttu-id="23bfa-147">シナリオは転記済トランザクションの上に構築されるため、フィールドを DimensionCombinationentity エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-147">Because our scenario builds on top of a posted transaction, we must add the fields to the DimensionCombinationentity entity.</span></span> <span data-ttu-id="23bfa-148">拡張機能による方法を使用して復元力のある方法で調整を行います。これにより、コード ベースを新しいバージョンに今後アップグレードするとき、必要なメンテナンスは最小限になります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-148">We want to make the adjustments in a resilient manner by using the extension approach, so that minimal maintenance will be required when we upgrade the code base to newer versions in the future.</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-version-1611"></a><span data-ttu-id="23bfa-149">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="23bfa-149">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition version 1611</span></span>

<span data-ttu-id="23bfa-150">バージョン 1611 以降については、Microsoft Visual Studio (**Dynamics 365** &gt; **アドイン** &gt; **Odata の財務分析コードの追加**) で利用できるウィザードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-150">For version 1611 or later, you should use the wizard that is available in Microsoft Visual Studio (at **Dynamics 365** &gt; **Addins** &gt; **Add financial dimensions for Odata**).</span></span> <span data-ttu-id="23bfa-151">手順については、[Excel テンプレートに分析コードを追加する](dimensions-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23bfa-151">For instructions, see [Add dimensions to Excel templates](dimensions-overview.md).</span></span>

### <a name="earlier-versions"></a><span data-ttu-id="23bfa-152">以前のバージョン</span><span class="sxs-lookup"><span data-stu-id="23bfa-152">Earlier versions</span></span>

<span data-ttu-id="23bfa-153">以前のバージョンで作業している場合、ここで説明されている手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-153">If you're working with earlier versions, you must complete the steps that are outlined here.</span></span> <span data-ttu-id="23bfa-154">最初に、エンティティ拡張機能自体を追加します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-154">First, we add the entity extension itself.</span></span> <span data-ttu-id="23bfa-155">コンテキスト メニュー (ショートカット メニュー) で **拡張機能を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-155">Select **Create extension** on the context menu (shortcut menu).</span></span> <span data-ttu-id="23bfa-156">次に、データを取得するコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-156">Next, we create the code that retrieves the data.</span></span> <span data-ttu-id="23bfa-157">エンティティ拡張子が既に確立されているため、新しいクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-157">Because the entity extension is already in place, we must create a new class.</span></span> <span data-ttu-id="23bfa-158">次の例では、**ProductLine** という名前の任意の分析コードを追加します。.</span><span class="sxs-lookup"><span data-stu-id="23bfa-158">The following example adds code for an arbitrary dimension that is named **ProductLine**.</span></span>
    
```xpp    
[ExtensionOf(dataentityviewstr(DimensionCombinationentity))]
  public final class DimensionCombinationentity_Extension
  {
    private static server str getEmptyOrDimensionValueSqlString(str _attributeName)
    {
        str sqlStatement;

        DimensionAttribute dimensionAttribute = DimensionAttribute::findByName(_attributeName);

        if (!dimensionAttribute)
        {
            sqlStatement = SysComputedColumn::returnLiteral('');
        }
        else
        {
            sqlStatement = strFmt('SELECT TOP 1 T1.%1 ', dimensionAttribute.DimensionValueColumnName);
        }

        return sqlStatement;
    }

    /// Generates the sql to populate the FOTA view field.
    public static server str ProductLineValue()
    {
        return DimensionCombinationentity::getEmptyOrDimensionValueSqlString('ProductLine');
    }
  }
```

<span data-ttu-id="23bfa-159">これらのメソッドを参照するカスタム フィールドを使用して、新たに作成されたエンティティ拡張機能にフィールドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="23bfa-159">We now add fields to the newly created entity extension by using custom fields that reference these methods.</span></span> 

<span data-ttu-id="23bfa-160">[![フィールドの追加](./media/fd-menu4.png)](./media/fd-menu4.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-160">[![Add fields](./media/fd-menu4.png)](./media/fd-menu4.png)</span></span>

<span data-ttu-id="23bfa-161">次に、フィールドがマップされておらず、拡張機能クラスに対して作成したコードを通じて取得する必要があることを反映するためにプロパティ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-161">Next, we set the property values to reflect the fact that the field is unmapped and should be retrieved through the code that we made for the extension class.</span></span> <span data-ttu-id="23bfa-162">リレーションを作成するとき、次の値も設定します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-162">When you create the relation, also set the following values:</span></span>

-   <span data-ttu-id="23bfa-163">カーディナリティ: **ZeroMore**</span><span class="sxs-lookup"><span data-stu-id="23bfa-163">Cardinality: **ZeroMore**</span></span>
-   <span data-ttu-id="23bfa-164">関連データ エンティティ: **DimensionCombinationentity**</span><span class="sxs-lookup"><span data-stu-id="23bfa-164">Related data entity: **DimensionCombinationentity**</span></span>
-   <span data-ttu-id="23bfa-165">関連データ エンティティ カーディナリティ: **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="23bfa-165">Related data entity cardinality: **ZeroOne**</span></span>
-   <span data-ttu-id="23bfa-166">関係タイプ: **関連**</span><span class="sxs-lookup"><span data-stu-id="23bfa-166">Relationship type: **Association**</span></span>

<span data-ttu-id="23bfa-167">[![関係の作成](./media/fd-menu5.png)](./media/fd-menu5.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-167">[![Create relation](./media/fd-menu5.png)](./media/fd-menu5.png)</span></span>

> [!Note]
> <span data-ttu-id="23bfa-168">クラス名でデータ メソッドを完全に修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-168">We must fully qualify the data method with the class name.</span></span> 

<span data-ttu-id="23bfa-169">新しい VendInvoiceTransactionentity エンティティに DimensionCombinationentity エンティティを追加する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="23bfa-169">We are now ready to add the DimensionCombinationentity entity to our new VendInvoiceTransactionentity entity.</span></span> 

<span data-ttu-id="23bfa-170">[![DimensionCombinationentity の追加](./media/fd-menu6.png)](./media/fd-menu6.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-170">[![Add DimensionCombinationentity](./media/fd-menu6.png)](./media/fd-menu6.png)</span></span>

<span data-ttu-id="23bfa-171">AccountingDistributionCurrent と DimensionCombinationentity エンティティの両方が外部結合であることに注意します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-171">Notice that both the AccountingDistributionCurrent and the DimensionCombinationentity entity should be outer-joined.</span></span> 

<span data-ttu-id="23bfa-172">[![外部結合](./media/fd-menu7.png)](./media/fd-menu7.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-172">[![Outer join](./media/fd-menu7.png)](./media/fd-menu7.png)</span></span>

<span data-ttu-id="23bfa-173">ここで、新しいエンティティで必須フィールドをさまざまなデータ ソースから **フィールド** ノード (つまり、新たに作成された ProductLine) にドラッグする必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-173">Now, we just have to drag the required fields from the various data sources to the **Fields** node on the new entity (that is, to our newly created ProductLine).</span></span> 

<span data-ttu-id="23bfa-174">[![ProductLine にドラッグ](./media/fd-menu8.png)](./media/fd-menu8.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-174">[![Drag to ProductLine](./media/fd-menu8.png)](./media/fd-menu8.png)</span></span>

<span data-ttu-id="23bfa-175">エクスポートの構成時に差分更新機能を有効にするために、エンティティにキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-175">We should add a key to the entity to enable the incremental update functionality during the export configuration.</span></span> <span data-ttu-id="23bfa-176">したがって、VendInvoiceTrans データ ソースの RecId が、たとえば VendInvoiceTransRecId と名付けられたフィールドの一部であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-176">Therefore, we must make sure that RecId from the VendInvoiceTrans data source is part of the fields named e.g. VendInvoiceTransRecId.</span></span> <span data-ttu-id="23bfa-177">フィールドがフィールドリストに入った後、フィールドを **EntityKey** ノードにドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="23bfa-177">After the field is in the field list, we can drag it to the **EntityKey** node.</span></span> 

<span data-ttu-id="23bfa-178">[![EntityKey にドラッグ](./media/fd-menu9.png)](./media/fd-menu9.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-178">[![Drag to EntityKey](./media/fd-menu9.png)](./media/fd-menu9.png)</span></span>

<span data-ttu-id="23bfa-179">ステージング テーブルが完全に構成されたエンティティに関連付けられていることを確認するには、ステージング テーブルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-179">To make sure that the staging table is associated with the fully configured entity, we must update it.</span></span> <span data-ttu-id="23bfa-180">エンティティのコンテキスト メニューで、**ステージング テーブルの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="23bfa-180">On the context menu for the entity, we select **Update staging table**.</span></span> 

<span data-ttu-id="23bfa-181">[![ステージング テーブルの更新](./media/fd-menu10.png)](./media/fd-menu10.png)</span><span class="sxs-lookup"><span data-stu-id="23bfa-181">[![Update staging table](./media/fd-menu10.png)](./media/fd-menu10.png)</span></span>

<span data-ttu-id="23bfa-182">エンティティの作業が完了したら、それを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="23bfa-182">The entity work is now complete, and we can build it.</span></span> 

> [!NOTE]
> <span data-ttu-id="23bfa-183">このシナリオでは、LedgerDimension が DimensionCombinationentity エンティティに関連付けられました。</span><span class="sxs-lookup"><span data-stu-id="23bfa-183">In this scenario, a LedgerDimension was associated with the DimensionCombinationentity entity.</span></span> <span data-ttu-id="23bfa-184">DefaultDimension があるシナリオでは、DimensionSetentity エンティティに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="23bfa-184">In scenarios where there is a DefaultDimension, we must associate it with the DimensionSetentity entity.</span></span> <span data-ttu-id="23bfa-185">必要な強化と拡張は、DimensionCombinationentity エンティティに対して行った強化と拡張と同じです。</span><span class="sxs-lookup"><span data-stu-id="23bfa-185">The improvements and extensions that are required are identical to the improvements and extensions that we made to the DimensionCombinationentity entity.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23bfa-186">追加リソース</span><span class="sxs-lookup"><span data-stu-id="23bfa-186">Additional resources</span></span>

[<span data-ttu-id="23bfa-187">Dynamics AX 7 のエンティティを自分の Azure SQL データベースにエクスポートする</span><span class="sxs-lookup"><span data-stu-id="23bfa-187">Export Dynamics AX 7 Entities to your own Azure SQL Database</span></span>](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/27/export-dynamics-ax7-entities-to-your-own-azure-sql-database/)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]