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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 273653
ms.assetid: 119610df-3975-43ce-830b-84fe58266321
ms.search.region: Global
ms.author: pbj
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 092f7e566c6ac14421e772f538a61af6fa0ef2d7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552516"
---
# <a name="create-read-only-entities-that-expose-financial-dimensions"></a><span data-ttu-id="6d173-103">財務分析コードを公開する読み取り専用エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="6d173-103">Create read-only entities that expose financial dimensions</span></span>
<span data-ttu-id="6d173-104">"[!include [banner](../includes/banner.md)]"</span><span class="sxs-lookup"><span data-stu-id="6d173-104">"[!include [banner](../includes/banner.md)]"</span></span>


<span data-ttu-id="6d173-105">このトピックでは、登録されている登録済のトランザクションのエンティティを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d173-105">In this topic, we describe how to build an entity for registered transactions that are registered.</span></span> 

> [!NOTE] 
> <span data-ttu-id="6d173-106">このトピックは、ソリューション アーキテクチャ チームの Per Baarsoe Jorgensen から得たものです。</span><span class="sxs-lookup"><span data-stu-id="6d173-106">This topic comes from Per Baarsoe Jorgensen of the Solutions Architecture team.</span></span> <span data-ttu-id="6d173-107">顧客と作業時に発生した実際のシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="6d173-107">It describes a real-world scenario that we have encountered as we work with customers.</span></span> 

<span data-ttu-id="6d173-108">配分を使用して適用された財務分析コードと共にすべての仕入先請求明細行のトランザクションを公開しなければならないシナリオを考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="6d173-108">Imagine a scenario where we must expose all vendor invoice line transactions together with the financial dimensions that were applied through the distributions.</span></span> <span data-ttu-id="6d173-109">サード パーティのツールによる簡単な消費が不可欠なので、このシナリオ用のエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d173-109">Because easy consumption by a third-party tool is essential, we will create an entity for this scenario.</span></span> <span data-ttu-id="6d173-110">結果として、エンティティは他の関連するエンティティと結合する必要はなく、単独で値を提供できるべきです。</span><span class="sxs-lookup"><span data-stu-id="6d173-110">As a result, the entity should not have to be joined with other related entities but should be able to provide value on its own.</span></span>

<span data-ttu-id="6d173-111">これらの要件を満たすために、サンプル エンティティを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6d173-111">We will walk through the process of creating a sample entity to meet these requirements.</span></span> <span data-ttu-id="6d173-112">(これらの手順はすでに文書化されているため、Microsoft Azure DevOps との統合の手順は省略します。)</span><span class="sxs-lookup"><span data-stu-id="6d173-112">(We will leave out instructions for integrating with Microsoft Azure DevOps, because those steps are already well documented.)</span></span>

## <a name="create-a-basic-entity"></a><span data-ttu-id="6d173-113">基本エンティティの作成</span><span class="sxs-lookup"><span data-stu-id="6d173-113">Create a basic entity</span></span>
<span data-ttu-id="6d173-114">最初のステップは、**新しい品目** を選択して、プロジェクト内に新しい要素を作成することです。.</span><span class="sxs-lookup"><span data-stu-id="6d173-114">The first step is to create a new element in a project by selecting **New Item**.</span></span> 

<span data-ttu-id="6d173-115">[</span><span class="sxs-lookup"><span data-stu-id="6d173-115">[</span></span>![新しい項目](./media/fd-basic.png)<span data-ttu-id="6d173-117">]</span><span class="sxs-lookup"><span data-stu-id="6d173-117">]</span></span>

<span data-ttu-id="6d173-118">開いているフォームで、データ モデルの**データ エンティティ**要素のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d173-118">In the form that opens, under Data Model, we select the **Data Entity** element type.</span></span>

<span data-ttu-id="6d173-119">[</span><span class="sxs-lookup"><span data-stu-id="6d173-119">[</span></span>![データ要素](./media/fd-element.png)<span data-ttu-id="6d173-121">]</span><span class="sxs-lookup"><span data-stu-id="6d173-121">]</span></span>

> [!NOTE] 
> <span data-ttu-id="6d173-122">後で名前を変更できないためエンティティに名前を付けるときは注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="6d173-122">Be careful when you name the entity, because you can’t rename it later.</span></span>

<span data-ttu-id="6d173-123">次に、データ エンティティ ウィザードで、適切なプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d173-123">Next, in the Data Entity wizard, we select the appropriate primary data source.</span></span> <span data-ttu-id="6d173-124">シナリオでは、このデータ ソースは VendInvoiceTrans です。</span><span class="sxs-lookup"><span data-stu-id="6d173-124">For our scenario, this data source is VendInvoiceTrans.</span></span>

<span data-ttu-id="6d173-125">[</span><span class="sxs-lookup"><span data-stu-id="6d173-125">[</span></span>![データ エンティティ ウィザード](./media/fd-wizard.png)<span data-ttu-id="6d173-127">]</span><span class="sxs-lookup"><span data-stu-id="6d173-127">]</span></span>

<span data-ttu-id="6d173-128">VendInvoiceTrans の場合のように、ウィザードは自然キーを持たないテーブルを受け入れません。</span><span class="sxs-lookup"><span data-stu-id="6d173-128">The wizard doesn’t accept tables that don’t have a natural key, as is the case with VendInvoiceTrans.</span></span> <span data-ttu-id="6d173-129">したがって、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-129">Therefore, we receive the following error message.</span></span>

<span data-ttu-id="6d173-130">[</span><span class="sxs-lookup"><span data-stu-id="6d173-130">[</span></span>![ナチュラル キーのエラー](./media/fd-error.png)<span data-ttu-id="6d173-132">]</span><span class="sxs-lookup"><span data-stu-id="6d173-132">]</span></span>

<span data-ttu-id="6d173-133">この問題を回避するには、VendGroup などの自然なキーが関連付けられている他のプライマリ データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d173-133">The workaround is to select any other primary data source that has a natural key associated, such as VendGroup.</span></span>

<span data-ttu-id="6d173-134">このデータ ソースは実際には必要ないので、フィールドも必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6d173-134">Because we don’t really need this data source, we also don’t need any fields for it.</span></span> <span data-ttu-id="6d173-135">したがって、**すべて選択** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="6d173-135">Therefore, we clear the **Select all** check box.</span></span>

<span data-ttu-id="6d173-136">[</span><span class="sxs-lookup"><span data-stu-id="6d173-136">[</span></span>![すべての選択を解除](./media/fd-wizard2.png)<span data-ttu-id="6d173-138">]</span><span class="sxs-lookup"><span data-stu-id="6d173-138">]</span></span>

<span data-ttu-id="6d173-139">最後に、**完了**をクリックして、エンティティのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d173-139">Finally, we create the template for our entity by clicking **Finish**.</span></span>

## <a name="customize-the-basic-entity"></a><span data-ttu-id="6d173-140">基本的なエンティティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="6d173-140">Customize the basic entity</span></span>
<span data-ttu-id="6d173-141">エンティティ、ステージング テーブル、およびセキュリティ資産が作成され、カスタム エンティティを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6d173-141">The entity, staging table, and security assets have been created, and we can now produce our custom entity.</span></span> <span data-ttu-id="6d173-142">プロジェクトでは、デザイナーで VendorInvoiceTransactionDetailsEntity エンティティを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d173-142">In the project, we open the VendorInvoiceTransactionDetailsEntity entity in the designer.</span></span> 

<span data-ttu-id="6d173-143">[</span><span class="sxs-lookup"><span data-stu-id="6d173-143">[</span></span>![デザイナーの VendorInvoiceTransactionDetailsEntity](./media/fd-designer.png)<span data-ttu-id="6d173-145">]</span><span class="sxs-lookup"><span data-stu-id="6d173-145">]</span></span>

<span data-ttu-id="6d173-146">デザイナーで、ウィザードに適用したダミー テーブル (VendGroup) を、トランザクション テーブル VendInvoiceTrans に変えます。</span><span class="sxs-lookup"><span data-stu-id="6d173-146">In the designer, we replace the dummy table (VendGroup) that we applied in the wizard with the transaction table VendInvoiceTrans.</span></span> <span data-ttu-id="6d173-147">フィールドの追加を選択しなかったため、エンティティのフィールドを削除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6d173-147">Because we didn't choose to add the fields, we don't have to remove fields in the entity.</span></span>

<span data-ttu-id="6d173-148">[</span><span class="sxs-lookup"><span data-stu-id="6d173-148">[</span></span>![データ エンティティのタイプ](./media/fd-menu.png)<span data-ttu-id="6d173-150">]</span><span class="sxs-lookup"><span data-stu-id="6d173-150">]</span></span>
> [!NOTE] 
> <span data-ttu-id="6d173-151">このエンティティを使用してトランザクション データを公開するため、エンティティを読み取り専用としてマークすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="6d173-151">Because we are exposing transactional data by using this entity, it's important that we mark the entity as read-only.</span></span> <span data-ttu-id="6d173-152">そのため、トップ ノードで **Is read only** プロパティを **Yes** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d173-152">Therefore, we set the **Is read only** property to **Yes** on the top node.</span></span> <span data-ttu-id="6d173-153">勘定配布はバージョン管理されているため、クエリを実行するときに現在のバージョンのみが返されることが重要です。</span><span class="sxs-lookup"><span data-stu-id="6d173-153">Because accounting distributions are versioned, it's important that only the current version be returned when we query.</span></span> <span data-ttu-id="6d173-154">したがって、この部分を複数のエンティティ間で簡単に再利用できるようにするビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d173-154">Therefore, we create a view that makes this part easily reusable across multiple entities.</span></span> 

<span data-ttu-id="6d173-155">[</span><span class="sxs-lookup"><span data-stu-id="6d173-155">[</span></span>![VendInvoiceTrans と置き換え](./media/fd-menu2.png)<span data-ttu-id="6d173-157">]</span><span class="sxs-lookup"><span data-stu-id="6d173-157">]</span></span>

<span data-ttu-id="6d173-158">プロパティで、**ReferenceDistribution** に **0** の範囲フィルター値、**ReferenceRole** に **1** の範囲フィルター値を代入します。</span><span class="sxs-lookup"><span data-stu-id="6d173-158">In the properties, we assign **ReferenceDistribution** a range filter value of **0** and **ReferenceRole** a range filter value of **1**.</span></span> <span data-ttu-id="6d173-159">AccountDistributionReverse データ ソースの結合モード プロパティは、**NoExistsJoin** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-159">The join mode property for the AccountDistributionReverse data source must be **NoExistsJoin**.</span></span> <span data-ttu-id="6d173-160">新しいビューを配置した後、現在作成している VendorInvoiceTransactionDetailsEntity エンティティに追加できます。</span><span class="sxs-lookup"><span data-stu-id="6d173-160">After the new view is in place, we can add it to the VendorInvoiceTransactionDetailsEntity entity that we are currently building.</span></span> 

<span data-ttu-id="6d173-161">[</span><span class="sxs-lookup"><span data-stu-id="6d173-161">[</span></span>![VendorInvoiceTransactionDetailsEntity の追加](./media/fd-menu3.png)<span data-ttu-id="6d173-163">]</span><span class="sxs-lookup"><span data-stu-id="6d173-163">]</span></span>

## <a name="expose-financial-dimensions-as-fields"></a><span data-ttu-id="6d173-164">財務分析コードをフィールドとして公開</span><span class="sxs-lookup"><span data-stu-id="6d173-164">Expose financial dimensions as fields</span></span>
<span data-ttu-id="6d173-165">次の重要なステップは、財務分析コードをエンティティ上の異なるフィールドとして公開することです。</span><span class="sxs-lookup"><span data-stu-id="6d173-165">The next important step is to expose the financial dimensions as separate fields on the entity.</span></span> <span data-ttu-id="6d173-166">シナリオは転記済トランザクションの上に構築されるため、フィールドを DimensionCombinationentity エンティティに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-166">Because our scenario builds on top of a posted transaction, we must add the fields to the DimensionCombinationentity entity.</span></span> <span data-ttu-id="6d173-167">拡張機能による方法を使用して復元力のある方法で調整を行います。これにより、コード ベースを新しいバージョンに今後アップグレードするとき、必要なメンテナンスは最小限になります。</span><span class="sxs-lookup"><span data-stu-id="6d173-167">We want to make the adjustments in a resilient manner by using the extension approach, so that minimal maintenance will be required when we upgrade the code base to newer versions in the future.</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-version-1611"></a><span data-ttu-id="6d173-168">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="6d173-168">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition version 1611</span></span>

<span data-ttu-id="6d173-169">バージョン 1611 以降については、Microsoft Visual Studio (**Dynamics 365** &gt; **アドイン** &gt; **Odata の財務分析コードの追加**) で利用できるウィザードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-169">For version 1611 or later, you should use the wizard that is available in Microsoft Visual Studio (at **Dynamics 365** &gt; **Addins** &gt; **Add financial dimensions for Odata**).</span></span> <span data-ttu-id="6d173-170">手順については、「[Microsoft Excel テンプレートに分析コードを追加する](dimensions-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d173-170">For instructions, see [Add dimensions to the Microsoft Excel template](dimensions-overview.md).</span></span>

### <a name="earlier-versions"></a><span data-ttu-id="6d173-171">以前のバージョン</span><span class="sxs-lookup"><span data-stu-id="6d173-171">Earlier versions</span></span>

<span data-ttu-id="6d173-172">以前のバージョンで作業している場合、ここで説明されている手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-172">If you're working with earlier versions, you must complete the steps that are outlined here.</span></span> <span data-ttu-id="6d173-173">最初に、エンティティ拡張機能自体を追加します。</span><span class="sxs-lookup"><span data-stu-id="6d173-173">First, we add the entity extension itself.</span></span> <span data-ttu-id="6d173-174">コンテキスト メニュー (ショートカット メニュー) で **拡張機能を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d173-174">Select **Create extension** on the context menu (shortcut menu).</span></span> <span data-ttu-id="6d173-175">次に、データを取得するコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d173-175">Next, we create the code that retrieves the data.</span></span> <span data-ttu-id="6d173-176">エンティティ拡張子が既に確立されているため、新しいクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-176">Because the entity extension is already in place, we must create a new class.</span></span> <span data-ttu-id="6d173-177">次の例では、**ProductLine** という名前の任意の分析コードを追加します。.</span><span class="sxs-lookup"><span data-stu-id="6d173-177">The following example adds code for an arbitrary dimension that is named **ProductLine**.</span></span>

  <span data-ttu-id="6d173-178">[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) {str sqlStatement;</span><span class="sxs-lookup"><span data-stu-id="6d173-178">[ExtensionOf(dataentityviewstr(DimensionCombinationentity))] public final class DimensionCombinationentity_Extension { private static server str getEmptyOrDimensionValueSqlString(str _attributeName) { str sqlStatement;</span></span>

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

<span data-ttu-id="6d173-179">これらのメソッドを参照するカスタム フィールドを使用して、新たに作成されたエンティティ拡張機能にフィールドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6d173-179">We now add fields to the newly created entity extension by using custom fields that reference these methods.</span></span> 

<span data-ttu-id="6d173-180">[</span><span class="sxs-lookup"><span data-stu-id="6d173-180">[</span></span>![フィールドの追加](./media/fd-menu4.png)<span data-ttu-id="6d173-182">]</span><span class="sxs-lookup"><span data-stu-id="6d173-182">]</span></span>

<span data-ttu-id="6d173-183">次に、フィールドがマップされておらず、拡張機能クラスに対して作成したコードを通じて取得する必要があることを反映するためにプロパティ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6d173-183">Next, we set the property values to reflect the fact that the field is unmapped and should be retrieved through the code that we made for the extension class.</span></span> <span data-ttu-id="6d173-184">リレーションを作成するとき、次の値も設定します。</span><span class="sxs-lookup"><span data-stu-id="6d173-184">When you create the relation, also set the following values:</span></span>

-   <span data-ttu-id="6d173-185">カーディナリティ: **ZeroMore**</span><span class="sxs-lookup"><span data-stu-id="6d173-185">Cardinality: **ZeroMore**</span></span>
-   <span data-ttu-id="6d173-186">関連データ エンティティ: **DimensionCombinationentity**</span><span class="sxs-lookup"><span data-stu-id="6d173-186">Related data entity: **DimensionCombinationentity**</span></span>
-   <span data-ttu-id="6d173-187">関連データ エンティティ カーディナリティ: **ZeroOne**</span><span class="sxs-lookup"><span data-stu-id="6d173-187">Related data entity cardinality: **ZeroOne**</span></span>
-   <span data-ttu-id="6d173-188">関係タイプ: **関連**</span><span class="sxs-lookup"><span data-stu-id="6d173-188">Relationship type: **Association**</span></span>

<span data-ttu-id="6d173-189">[</span><span class="sxs-lookup"><span data-stu-id="6d173-189">[</span></span>![関係の作成](./media/fd-menu5.png)<span data-ttu-id="6d173-191">]</span><span class="sxs-lookup"><span data-stu-id="6d173-191">]</span></span>

> [!Note]
> <span data-ttu-id="6d173-192">クラス名でデータ メソッドを完全に修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-192">We must fully qualify the data method with the class name.</span></span> 

<span data-ttu-id="6d173-193">新しい VendInvoiceTransactionentity エンティティに DimensionCombinationentity エンティティを追加する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="6d173-193">We are now ready to add the DimensionCombinationentity entity to our new VendInvoiceTransactionentity entity.</span></span> 

<span data-ttu-id="6d173-194">[</span><span class="sxs-lookup"><span data-stu-id="6d173-194">[</span></span>![DimensionCombinationentity の追加](./media/fd-menu6.png)<span data-ttu-id="6d173-196">]</span><span class="sxs-lookup"><span data-stu-id="6d173-196">]</span></span> 

<span data-ttu-id="6d173-197">AccountingDistributionCurrent と DimensionCombinationentity エンティティの両方が外部結合であることに注意します。</span><span class="sxs-lookup"><span data-stu-id="6d173-197">Notice that both the AccountingDistributionCurrent and the DimensionCombinationentity entity should be outer-joined.</span></span> 

<span data-ttu-id="6d173-198">[</span><span class="sxs-lookup"><span data-stu-id="6d173-198">[</span></span>![外部結合](./media/fd-menu7.png)<span data-ttu-id="6d173-200">]</span><span class="sxs-lookup"><span data-stu-id="6d173-200">]</span></span>

<span data-ttu-id="6d173-201">ここで、新しいエンティティで必須フィールドをさまざまなデータ ソースから**フィールド** ノード (つまり、新たに作成された ProductLine) にドラッグする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-201">Now, we just have to drag the required fields from the various data sources to the **Fields** node on the new entity (that is, to our newly created ProductLine).</span></span> 

<span data-ttu-id="6d173-202">[</span><span class="sxs-lookup"><span data-stu-id="6d173-202">[</span></span>![ProductLine にドラッグ](./media/fd-menu8.png)<span data-ttu-id="6d173-204">]</span><span class="sxs-lookup"><span data-stu-id="6d173-204">]</span></span>

<span data-ttu-id="6d173-205">エクスポートの構成時に差分更新機能を有効にするために、エンティティにキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-205">We should add a key to the entity to enable the incremental update functionality during the export configuration.</span></span> <span data-ttu-id="6d173-206">したがって、VendInvoiceTrans データ ソースの RecId が、たとえば VendInvoiceTransRecId と名付けられたフィールドの一部であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-206">Therefore, we must make sure that RecId from the VendInvoiceTrans data source is part of the fields named e.g. VendInvoiceTransRecId.</span></span> <span data-ttu-id="6d173-207">フィールドがフィールドリストに入った後、フィールドを **EntityKey** ノードにドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="6d173-207">After the field is in the field list, we can drag it to the **EntityKey** node.</span></span> 

<span data-ttu-id="6d173-208">[</span><span class="sxs-lookup"><span data-stu-id="6d173-208">[</span></span>![EntityKey にドラッグ](./media/fd-menu9.png)<span data-ttu-id="6d173-210">]</span><span class="sxs-lookup"><span data-stu-id="6d173-210">]</span></span>

<span data-ttu-id="6d173-211">ステージング テーブルが完全に構成されたエンティティに関連付けられていることを確認するには、ステージング テーブルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-211">To make sure that the staging table is associated with the fully configured entity, we must update it.</span></span> <span data-ttu-id="6d173-212">エンティティのコンテキスト メニューで、**ステージング テーブルの更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d173-212">On the context menu for the entity, we select **Update staging table**.</span></span> 

<span data-ttu-id="6d173-213">[</span><span class="sxs-lookup"><span data-stu-id="6d173-213">[</span></span>![ステージング テーブルの更新](./media/fd-menu10.png)<span data-ttu-id="6d173-215">]</span><span class="sxs-lookup"><span data-stu-id="6d173-215">]</span></span>

<span data-ttu-id="6d173-216">エンティティの作業が完了したら、それを構築することができます。</span><span class="sxs-lookup"><span data-stu-id="6d173-216">The entity work is now complete, and we can build it.</span></span> 

> [!NOTE]
> <span data-ttu-id="6d173-217">このシナリオでは、LedgerDimension が DimensionCombinationentity エンティティに関連付けられました。</span><span class="sxs-lookup"><span data-stu-id="6d173-217">In this scenario, a LedgerDimension was associated with the DimensionCombinationentity entity.</span></span> <span data-ttu-id="6d173-218">DefaultDimension があるシナリオでは、DimensionSetentity エンティティに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d173-218">In scenarios where there is a DefaultDimension, we must associate it with the DimensionSetentity entity.</span></span> <span data-ttu-id="6d173-219">必要な強化と拡張は、DimensionCombinationentity エンティティに対して行った強化と拡張と同じです。</span><span class="sxs-lookup"><span data-stu-id="6d173-219">The improvements and extensions that are required are identical to the improvements and extensions that we made to the DimensionCombinationentity entity.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6d173-220">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6d173-220">Additional resources</span></span>
--------

[<span data-ttu-id="6d173-221">Dynamics AX 7 のエンティティを自分の Azure SQL データベースにエクスポートする</span><span class="sxs-lookup"><span data-stu-id="6d173-221">Export Dynamics AX 7 Entities to your own Azure SQL Database</span></span>](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/27/export-dynamics-ax7-entities-to-your-own-azure-sql-database/)


