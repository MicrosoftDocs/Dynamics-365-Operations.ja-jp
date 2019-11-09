---
title: 財務分析コードを公開する読み取り専用エンティティの作成
description: このトピックでは、登録済のトランザクションのエンティティを作成する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 273653
ms.assetid: 119610df-3975-43ce-830b-84fe58266321
ms.search.region: Global
ms.author: pbj
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4fd2b89a21ef38ce21010c86933c6447785ff8e4
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278095"
---
# <a name="create-read-only-entities-that-expose-financial-dimensions"></a><span data-ttu-id="cf8c2-103">財務分析コードを公開する読み取り専用エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="cf8c2-103">Create read-only entities that expose financial dimensions</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="cf8c2-104">このトピックでは、登録されている登録済のトランザクションのエンティティを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-104">In this topic, we describe how to build an entity for registered transactions that are registered.</span></span> 

> [!NOTE] 
> <span data-ttu-id="cf8c2-105">このトピックは、ソリューション アーキテクチャ チームの Per Baarsoe Jorgensen から得たものです。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-105">This topic comes from Per Baarsoe Jorgensen of the Solutions Architecture team.</span></span> <span data-ttu-id="cf8c2-106">顧客と作業時に発生した実際のシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-106">It describes a real-world scenario that we have encountered as we work with customers.</span></span> 

<span data-ttu-id="cf8c2-107">配分を使用して適用された財務分析コードと共にすべての仕入先請求明細行のトランザクションを公開しなければならないシナリオを考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-107">Imagine a scenario where we must expose all vendor invoice line transactions together with the financial dimensions that were applied through the distributions.</span></span> <span data-ttu-id="cf8c2-108">サード パーティのツールによる簡単な消費が不可欠なので、このシナリオ用のエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-108">Because easy consumption by a third-party tool is essential, we will create an entity for this scenario.</span></span> <span data-ttu-id="cf8c2-109">結果として、エンティティは他の関連するエンティティと結合する必要はなく、単独で値を提供できるべきです。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-109">As a result, the entity should not have to be joined with other related entities but should be able to provide value on its own.</span></span>

<span data-ttu-id="cf8c2-110">これらの要件を満たすために、サンプル エンティティを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-110">We will walk through the process of creating a sample entity to meet these requirements.</span></span> <span data-ttu-id="cf8c2-111">(これらの手順はすでに文書化されているため、Microsoft Azure DevOps との統合の手順は省略します。)</span><span class="sxs-lookup"><span data-stu-id="cf8c2-111">(We will leave out instructions for integrating with Microsoft Azure DevOps, because those steps are already well documented.)</span></span>

## <a name="create-a-basic-entity"></a><span data-ttu-id="cf8c2-112">基本エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="cf8c2-112">Create a basic entity</span></span>
<span data-ttu-id="cf8c2-113">最初のステップは、**新しい品目** を選択して、プロジェクト内に新しい要素を作成することです。.</span><span class="sxs-lookup"><span data-stu-id="cf8c2-113">The first step is to create a new element in a project by selecting **New Item**.</span></span> 

<span data-ttu-id="cf8c2-114">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-114">[</span></span>![新しい項目](./media/fd-basic.png)<span data-ttu-id="cf8c2-116">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-116">]</span></span>

<span data-ttu-id="cf8c2-117">開いているフォームで、データ モデルの**データ エンティティ**要素のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-117">In the form that opens, under Data Model, we select the **Data Entity** element type.</span></span>

<span data-ttu-id="cf8c2-118">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-118">[</span></span>![データ要素](./media/fd-element.png)<span data-ttu-id="cf8c2-120">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-120">]</span></span>

> [!NOTE] 
> <span data-ttu-id="cf8c2-121">後で名前を変更できないためエンティティに名前を付けるときは注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-121">Be careful when you name the entity, because you can’t rename it later.</span></span>

<span data-ttu-id="cf8c2-122">次に、データ エンティティ ウィザードで、適切なプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-122">Next, in the Data Entity wizard, we select the appropriate primary data source.</span></span> <span data-ttu-id="cf8c2-123">シナリオでは、このデータ ソースは VendInvoiceTrans です。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-123">For our scenario, this data source is VendInvoiceTrans.</span></span>

<span data-ttu-id="cf8c2-124">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-124">[</span></span>![データ エンティティ ウィザード](./media/fd-wizard.png)<span data-ttu-id="cf8c2-126">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-126">]</span></span>

<span data-ttu-id="cf8c2-127">VendInvoiceTrans の場合のように、ウィザードは自然キーを持たないテーブルを受け入れません。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-127">The wizard doesn’t accept tables that don’t have a natural key, as is the case with VendInvoiceTrans.</span></span> <span data-ttu-id="cf8c2-128">したがって、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-128">Therefore, we receive the following error message.</span></span>

<span data-ttu-id="cf8c2-129">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-129">[</span></span>![ナチュラル キーのエラー](./media/fd-error.png)<span data-ttu-id="cf8c2-131">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-131">]</span></span>

<span data-ttu-id="cf8c2-132">この問題を回避するには、VendGroup などの自然なキーが関連付けられている他のプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-132">The workaround is to select any other primary data source that has a natural key associated, such as VendGroup.</span></span>

<span data-ttu-id="cf8c2-133">このデータ ソースは実際には必要ないので、フィールドも必要ありません。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-133">Because we don’t really need this data source, we also don’t need any fields for it.</span></span> <span data-ttu-id="cf8c2-134">したがって、**すべて選択** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-134">Therefore, we clear the **Select all** check box.</span></span>

<span data-ttu-id="cf8c2-135">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-135">[</span></span>![すべての選択を解除](./media/fd-wizard2.png)<span data-ttu-id="cf8c2-137">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-137">]</span></span>

<span data-ttu-id="cf8c2-138">最後に、**完了**をクリックして、エンティティのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-138">Finally, we create the template for our entity by clicking **Finish**.</span></span>

## <a name="customize-the-basic-entity"></a><span data-ttu-id="cf8c2-139">基本的なエンティティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-139">Customize the basic entity</span></span>
<span data-ttu-id="cf8c2-140">エンティティ、ステージング テーブル、およびセキュリティ資産が作成され、カスタム エンティティを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-140">The entity, staging table, and security assets have been created, and we can now produce our custom entity.</span></span> <span data-ttu-id="cf8c2-141">プロジェクトでは、デザイナーで VendorInvoiceTransactionDetailsEntity エンティティを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-141">In the project, we open the VendorInvoiceTransactionDetailsEntity entity in the designer.</span></span> 

<span data-ttu-id="cf8c2-142">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-142">[</span></span>![デザイナーの VendorInvoiceTransactionDetailsEntity](./media/fd-designer.png)<span data-ttu-id="cf8c2-144">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-144">]</span></span>

<span data-ttu-id="cf8c2-145">デザイナーで、ウィザードに適用したダミー テーブル (VendGroup) を、トランザクション テーブル VendInvoiceTrans に変えます。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-145">In the designer, we replace the dummy table (VendGroup) that we applied in the wizard with the transaction table VendInvoiceTrans.</span></span> <span data-ttu-id="cf8c2-146">フィールドの追加を選択しなかったため、エンティティのフィールドを削除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-146">Because we didn't choose to add the fields, we don't have to remove fields in the entity.</span></span>

<span data-ttu-id="cf8c2-147">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-147">[</span></span>![データ エンティティのタイプ](./media/fd-menu.png)<span data-ttu-id="cf8c2-149">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-149">]</span></span>
> [!NOTE] 
> <span data-ttu-id="cf8c2-150">このエンティティを使用してトランザクション データを公開するため、エンティティを読み取り専用としてマークすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-150">Because we are exposing transactional data by using this entity, it's important that we mark the entity as read-only.</span></span> <span data-ttu-id="cf8c2-151">そのため、トップ ノードで **Is read only** プロパティを **Yes** に設定します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-151">Therefore, we set the **Is read only** property to **Yes** on the top node.</span></span> <span data-ttu-id="cf8c2-152">勘定配布はバージョン管理されているため、クエリを実行するときに現在のバージョンのみが返されることが重要です。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-152">Because accounting distributions are versioned, it's important that only the current version be returned when we query.</span></span> <span data-ttu-id="cf8c2-153">したがって、この部分を複数のエンティティ間で簡単に再利用できるようにするビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-153">Therefore, we create a view that makes this part easily reusable across multiple entities.</span></span> 

<span data-ttu-id="cf8c2-154">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-154">[</span></span>![VendInvoiceTrans と置き換え](./media/fd-menu2.png)<span data-ttu-id="cf8c2-156">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-156">]</span></span>

<span data-ttu-id="cf8c2-157">プロパティで、**ReferenceDistribution** に **0** の範囲フィルター値、**ReferenceRole** に **1** の範囲フィルター値を代入します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-157">In the properties, we assign **ReferenceDistribution** a range filter value of **0** and **ReferenceRole** a range filter value of **1**.</span></span> <span data-ttu-id="cf8c2-158">AccountDistributionReverse データ ソースの結合モード プロパティは、**NoExistsJoin** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-158">The join mode property for the AccountDistributionReverse data source must be **NoExistsJoin**.</span></span> <span data-ttu-id="cf8c2-159">新しいビューを配置した後、現在作成している VendorInvoiceTransactionDetailsEntity エンティティに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-159">After the new view is in place, we can add it to the VendorInvoiceTransactionDetailsEntity entity that we are currently building.</span></span> 

<span data-ttu-id="cf8c2-160">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-160">[</span></span>![VendorInvoiceTransactionDetailsEntity の追加](./media/fd-menu3.png)<span data-ttu-id="cf8c2-162">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-162">]</span></span>

## <a name="expose-financial-dimensions-as-fields"></a><span data-ttu-id="cf8c2-163">財務分析コードをフィールドとして公開</span><span class="sxs-lookup"><span data-stu-id="cf8c2-163">Expose financial dimensions as fields</span></span>
<span data-ttu-id="cf8c2-164">次の重要なステップは、財務分析コードをエンティティ上の異なるフィールドとして公開することです。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-164">The next important step is to expose the financial dimensions as separate fields on the entity.</span></span> <span data-ttu-id="cf8c2-165">シナリオは転記済トランザクションの上に構築されるため、フィールドを DimensionCombinationentity エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-165">Because our scenario builds on top of a posted transaction, we must add the fields to the DimensionCombinationentity entity.</span></span> <span data-ttu-id="cf8c2-166">拡張機能による方法を使用して復元力のある方法で調整を行います。これにより、コード ベースを新しいバージョンに今後アップグレードするとき、必要なメンテナンスは最小限になります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-166">We want to make the adjustments in a resilient manner by using the extension approach, so that minimal maintenance will be required when we upgrade the code base to newer versions in the future.</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-version-1611"></a><span data-ttu-id="cf8c2-167">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="cf8c2-167">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition version 1611</span></span>

<span data-ttu-id="cf8c2-168">バージョン 1611 以降については、Microsoft Visual Studio (**Dynamics 365** &gt; **アドイン** &gt; **Odata の財務分析コードの追加**) で利用できるウィザードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-168">For version 1611 or later, you should use the wizard that is available in Microsoft Visual Studio (at **Dynamics 365** &gt; **Addins** &gt; **Add financial dimensions for Odata**).</span></span> <span data-ttu-id="cf8c2-169">手順については、「[Microsoft Excel テンプレートに分析コードを追加する](dimensions-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-169">For instructions, see [Add dimensions to the Microsoft Excel template](dimensions-overview.md).</span></span>

### <a name="earlier-versions"></a><span data-ttu-id="cf8c2-170">以前のバージョン</span><span class="sxs-lookup"><span data-stu-id="cf8c2-170">Earlier versions</span></span>

<span data-ttu-id="cf8c2-171">以前のバージョンで作業している場合、ここで説明されている手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-171">If you're working with earlier versions, you must complete the steps that are outlined here.</span></span> <span data-ttu-id="cf8c2-172">最初に、エンティティ拡張機能自体を追加します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-172">First, we add the entity extension itself.</span></span> <span data-ttu-id="cf8c2-173">コンテキスト メニュー (ショートカット メニュー) で **拡張機能を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-173">Select **Create extension** on the context menu (shortcut menu).</span></span> <span data-ttu-id="cf8c2-174">次に、データを取得するコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-174">Next, we create the code that retrieves the data.</span></span> <span data-ttu-id="cf8c2-175">エンティティ拡張子が既に確立されているため、新しいクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-175">Because the entity extension is already in place, we must create a new class.</span></span> <span data-ttu-id="cf8c2-176">次の例では、**ProductLine** という名前の任意の分析コードを追加します。.</span><span class="sxs-lookup"><span data-stu-id="cf8c2-176">The following example adds code for an arbitrary dimension that is named **ProductLine**.</span></span>

  <span data-ttu-id="cf8c2-177">[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) {str sqlStatement;</span><span class="sxs-lookup"><span data-stu-id="cf8c2-177">[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) { str sqlStatement;</span></span>

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

<span data-ttu-id="cf8c2-178">これらのメソッドを参照するカスタム フィールドを使用して、新たに作成されたエンティティ拡張機能にフィールドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-178">We now add fields to the newly created entity extension by using custom fields that reference these methods.</span></span> 

<span data-ttu-id="cf8c2-179">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-179">[</span></span>![フィールドの追加](./media/fd-menu4.png)<span data-ttu-id="cf8c2-181">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-181">]</span></span>

<span data-ttu-id="cf8c2-182">次に、フィールドがマップされておらず、拡張機能クラスに対して作成したコードを通じて取得する必要があることを反映するためにプロパティ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-182">Next, we set the property values to reflect the fact that the field is unmapped and should be retrieved through the code that we made for the extension class.</span></span> <span data-ttu-id="cf8c2-183">リレーションを作成するとき、次の値も設定します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-183">When you create the relation, also set the following values:</span></span>

-   <span data-ttu-id="cf8c2-184">カーディナリティ: **ZeroMore**</span><span class="sxs-lookup"><span data-stu-id="cf8c2-184">Cardinality: **ZeroMore**</span></span>
-   <span data-ttu-id="cf8c2-185">関連データ エンティティ: **DimensionCombinationentity**</span><span class="sxs-lookup"><span data-stu-id="cf8c2-185">Related data entity: **DimensionCombinationentity**</span></span>
-   <span data-ttu-id="cf8c2-186">関連データ エンティティ カーディナリティ: **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="cf8c2-186">Related data entity cardinality: **ZeroOne**</span></span>
-   <span data-ttu-id="cf8c2-187">関係タイプ: **関連**</span><span class="sxs-lookup"><span data-stu-id="cf8c2-187">Relationship type: **Association**</span></span>

<span data-ttu-id="cf8c2-188">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-188">[</span></span>![関係の作成](./media/fd-menu5.png)<span data-ttu-id="cf8c2-190">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-190">]</span></span>

> [!Note]
> <span data-ttu-id="cf8c2-191">クラス名でデータ メソッドを完全に修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-191">We must fully qualify the data method with the class name.</span></span> 

<span data-ttu-id="cf8c2-192">新しい VendInvoiceTransactionentity エンティティに DimensionCombinationentity エンティティを追加する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-192">We are now ready to add the DimensionCombinationentity entity to our new VendInvoiceTransactionentity entity.</span></span> 

<span data-ttu-id="cf8c2-193">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-193">[</span></span>![DimensionCombinationentity の追加](./media/fd-menu6.png)<span data-ttu-id="cf8c2-195">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-195">]</span></span> 

<span data-ttu-id="cf8c2-196">AccountingDistributionCurrent と DimensionCombinationentity エンティティの両方が外部結合であることに注意します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-196">Notice that both the AccountingDistributionCurrent and the DimensionCombinationentity entity should be outer-joined.</span></span> 

<span data-ttu-id="cf8c2-197">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-197">[</span></span>![外部結合](./media/fd-menu7.png)<span data-ttu-id="cf8c2-199">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-199">]</span></span>

<span data-ttu-id="cf8c2-200">ここで、新しいエンティティで必須フィールドをさまざまなデータ ソースから**フィールド** ノード (つまり、新たに作成された ProductLine) にドラッグする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-200">Now, we just have to drag the required fields from the various data sources to the **Fields** node on the new entity (that is, to our newly created ProductLine).</span></span> 

<span data-ttu-id="cf8c2-201">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-201">[</span></span>![ProductLine にドラッグ](./media/fd-menu8.png)<span data-ttu-id="cf8c2-203">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-203">]</span></span>

<span data-ttu-id="cf8c2-204">エクスポートの構成時に差分更新機能を有効にするために、エンティティにキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-204">We should add a key to the entity to enable the incremental update functionality during the export configuration.</span></span> <span data-ttu-id="cf8c2-205">したがって、VendInvoiceTrans データ ソースの RecId が、たとえば VendInvoiceTransRecId と名付けられたフィールドの一部であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-205">Therefore, we must make sure that RecId from the VendInvoiceTrans data source is part of the fields named e.g. VendInvoiceTransRecId.</span></span> <span data-ttu-id="cf8c2-206">フィールドがフィールドリストに入った後、フィールドを **EntityKey** ノードにドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-206">After the field is in the field list, we can drag it to the **EntityKey** node.</span></span> 

<span data-ttu-id="cf8c2-207">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-207">[</span></span>![EntityKey にドラッグ](./media/fd-menu9.png)<span data-ttu-id="cf8c2-209">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-209">]</span></span>

<span data-ttu-id="cf8c2-210">ステージング テーブルが完全に構成されたエンティティに関連付けられていることを確認するには、ステージング テーブルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-210">To make sure that the staging table is associated with the fully configured entity, we must update it.</span></span> <span data-ttu-id="cf8c2-211">エンティティのコンテキスト メニューで、**ステージング テーブルの更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-211">On the context menu for the entity, we select **Update staging table**.</span></span> 

<span data-ttu-id="cf8c2-212">[</span><span class="sxs-lookup"><span data-stu-id="cf8c2-212">[</span></span>![ステージング テーブルの更新](./media/fd-menu10.png)<span data-ttu-id="cf8c2-214">]</span><span class="sxs-lookup"><span data-stu-id="cf8c2-214">]</span></span>

<span data-ttu-id="cf8c2-215">エンティティの作業が完了したら、それを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-215">The entity work is now complete, and we can build it.</span></span> 

> [!NOTE]
> <span data-ttu-id="cf8c2-216">このシナリオでは、LedgerDimension が DimensionCombinationentity エンティティに関連付けられました。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-216">In this scenario, a LedgerDimension was associated with the DimensionCombinationentity entity.</span></span> <span data-ttu-id="cf8c2-217">DefaultDimension があるシナリオでは、DimensionSetentity エンティティに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-217">In scenarios where there is a DefaultDimension, we must associate it with the DimensionSetentity entity.</span></span> <span data-ttu-id="cf8c2-218">必要な強化と拡張は、DimensionCombinationentity エンティティに対して行った強化と拡張と同じです。</span><span class="sxs-lookup"><span data-stu-id="cf8c2-218">The improvements and extensions that are required are identical to the improvements and extensions that we made to the DimensionCombinationentity entity.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cf8c2-219">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cf8c2-219">Additional resources</span></span>
--------

[<span data-ttu-id="cf8c2-220">Dynamics AX 7 のエンティティを自分の Azure SQL データベースにエクスポートする</span><span class="sxs-lookup"><span data-stu-id="cf8c2-220">Export Dynamics AX 7 Entities to your own Azure SQL Database</span></span>](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/27/export-dynamics-ax7-entities-to-your-own-azure-sql-database/)

