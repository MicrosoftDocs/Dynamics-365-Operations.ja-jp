---
title: "分析コード"
description: "さまざまな分析コードのパターンをサポートするために、分析コードを含む他のエンティティのデータ ソースとして使用できる一連のフレームワーク データ エンティティが作成されています。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 13461
ms.assetid: c2431895-0751-4a2a-96cb-f7df76c88f66
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: de4cd9b87cd98f962939dacbc14afece95b5f063
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="dimensions"></a><span data-ttu-id="6610d-103">分析コード</span><span class="sxs-lookup"><span data-stu-id="6610d-103">Dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6610d-104">さまざまな分析コードのパターンをサポートするために、分析コードを含む他のエンティティのデータ ソースとして使用できる一連のフレームワーク データ エンティティが作成されています。</span><span class="sxs-lookup"><span data-stu-id="6610d-104">To support different dimension patterns, a set of framework data entities has been created that can be used as data sources in other entities that involve dimensions.</span></span>

<a name="the-sfk-and-the-natural-key"></a><span data-ttu-id="6610d-105">SFK とナチュラル キー</span><span class="sxs-lookup"><span data-stu-id="6610d-105">The SFK and the Natural key</span></span>
---------------------------

<span data-ttu-id="6610d-106">さまざまな分析コードのパターンをサポートするために、分析コードを含む他のエンティティのデータ ソースとして使用できる一連のフレームワーク データ エンティティが作成されています。</span><span class="sxs-lookup"><span data-stu-id="6610d-106">To support different dimension patterns, a set of framework data entities has been created that can be used as data sources in other entities that involve dimensions.</span></span> <span data-ttu-id="6610d-107">データ エンティティのこの入れ子が発生すると、分析コードのデータ エンティティの代理外部キー (SFK) およびナチュラル キーは別に処理されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-107">When this nesting of data entities occurs, the surrogate foreign key (SFK) and natural key of the dimensions data entity are treated differently.</span></span> <span data-ttu-id="6610d-108">次の表では、違いについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6610d-108">The following table describes the differences.</span></span>

| <span data-ttu-id="6610d-109">キー タイプ</span><span class="sxs-lookup"><span data-stu-id="6610d-109">Key type</span></span>    | <span data-ttu-id="6610d-110">アクセス モディファイア</span><span class="sxs-lookup"><span data-stu-id="6610d-110">Access modifier</span></span> | <span data-ttu-id="6610d-111">ディメンション エンティティが別のエンティティのデータ ソースである場合の説明</span><span class="sxs-lookup"><span data-stu-id="6610d-111">Description, when the dimension entity is a data source on another entity</span></span>|
|-------------|-----------------|--------------------------------------------------------------------------|
| <span data-ttu-id="6610d-112">SFK</span><span class="sxs-lookup"><span data-stu-id="6610d-112">SFK</span></span>         | <span data-ttu-id="6610d-113">private</span><span class="sxs-lookup"><span data-stu-id="6610d-113">private</span></span>         | <span data-ttu-id="6610d-114">任意の SFK と同様に、分析コードの SFK は外部データ エンティティでプライベート フィールドとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-114">As with any SFK, the SFK of the dimension is defined on the outer data entity as a private field.</span></span>  |
| <span data-ttu-id="6610d-115">ナチュラル キー</span><span class="sxs-lookup"><span data-stu-id="6610d-115">Natural key</span></span> | <span data-ttu-id="6610d-116">public</span><span class="sxs-lookup"><span data-stu-id="6610d-116">public</span></span>          | <span data-ttu-id="6610d-117">分析コード エンティティのナチュラル キーは、分析コード属性値のパブリック文字列として公開されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-117">The natural key of the dimension entity is exposed as a public string of dimension attribute values.</span></span> <span data-ttu-id="6610d-118">値は連結されていますが、アカウント デリミタで区切られています。</span><span class="sxs-lookup"><span data-stu-id="6610d-118">The values are concatenated together but are separated by the account delimiter.</span></span> <span data-ttu-id="6610d-119">アカウントの区切り記号は、パーティションごとに定義されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-119">The account delimiter is defined per partition.</span></span> <span data-ttu-id="6610d-120">連結された文字列が表示値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-120">The concatenated string is used as a display value.</span></span> <span data-ttu-id="6610d-121">このドキュメントで後で説明するように、エンティティの一部のフィールドに接尾語として “DisplayValue” という句が追加さます。</span><span class="sxs-lookup"><span data-stu-id="6610d-121">The phrase “DisplayValue” is appended as a suffix to some fields of an entity, as explained later in this document.</span></span> |

## <a name="reads-and-writes"></a><span data-ttu-id="6610d-122">読み取りおよび書き込み</span><span class="sxs-lookup"><span data-stu-id="6610d-122">Reads and writes</span></span>
<span data-ttu-id="6610d-123">**読み取り:** 外部データ エンティティの読み取りでは、フレームワークの分析コードのエンティティを使用して、パブリック表示値が計算列から取得されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-123">**Read:** On a read of the outer data entity, the public display value will be retrieved from a computed column by using the dimension entity of the framework.</span></span> <span data-ttu-id="6610d-124">読み取りは計算列が使用されるため、エクスポート シナリオでは X++ ロジックは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6610d-124">Because the read uses a computed column, it doesn't require any X++ logic for export scenarios.</span></span> <span data-ttu-id="6610d-125">**書き込み:** 作成またはエンティティ インスタンスの値の更新で、公開表示値は、プライベート フィールドと一致するように SFK に解決されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-125">**Write:** On the creation or update of entity instance values, the public display value is resolved to the SFK to match the private field.</span></span>

### <a name="examples"></a><span data-ttu-id="6610d-126">例</span><span class="sxs-lookup"><span data-stu-id="6610d-126">Examples</span></span>

<span data-ttu-id="6610d-127">**DimensionEntityTestEntity** は、1 つ以上の分析コード パターンを持つテスト エンティティです。</span><span class="sxs-lookup"><span data-stu-id="6610d-127">**DimensionEntityTestEntity** is a test entity that has more than one dimension pattern.</span></span> <span data-ttu-id="6610d-128">既定の分析コードについては、**DimensionDefault** および **DimensionDefaultDisplayValue** フィールドに注目し、残りは無視できます。</span><span class="sxs-lookup"><span data-stu-id="6610d-128">For the default dimension, you can focus on the **DimensionDefault** and **DimensionDefaultDisplayValue** fields, and ignore the rest.</span></span>

#### <a name="read-example"></a><span data-ttu-id="6610d-129">読み取りの例</span><span class="sxs-lookup"><span data-stu-id="6610d-129">Read example</span></span>

<span data-ttu-id="6610d-130">[![例の読み取り](./media/suba.png)](./media/suba.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-130">[![Read example](./media/suba.png)](./media/suba.png)</span></span>

#### <a name="write-example"></a><span data-ttu-id="6610d-131">例の記述</span><span class="sxs-lookup"><span data-stu-id="6610d-131">Write example</span></span>

<span data-ttu-id="6610d-132">エンティティは既定の分析コード フィールド、**DimensionDefaultDisplayValue** を公開します。</span><span class="sxs-lookup"><span data-stu-id="6610d-132">The entity exposes a default dimension field, **DimensionDefaultDisplayValue**.</span></span> <span data-ttu-id="6610d-133">これは、表示値フィールドです。</span><span class="sxs-lookup"><span data-stu-id="6610d-133">This is a display value field.</span></span> <span data-ttu-id="6610d-134">このフィールドは、ユーザー インターフェイスのセグメント化された入力コントロールのような、連結された文字列値に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6610d-134">You can set this field to a concatenated string value that is similar to the segmented entry control of the user interface.</span></span> 

<span data-ttu-id="6610d-135">[![例を記述](./media/subb.png)](./media/subb.png)**DisplayValue** は実行時に**DefaultDimension** に解決します。</span><span class="sxs-lookup"><span data-stu-id="6610d-135">[![Write example](./media/subb.png)](./media/subb.png) **DisplayValue** resolves to **DefaultDimension** at run time.</span></span>

## <a name="create-an-entity-by-using-a-wizard"></a><span data-ttu-id="6610d-136">ウィザードを使用してエンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="6610d-136">Create an entity by using a wizard</span></span>
<span data-ttu-id="6610d-137">このセクションでは、ウィザードを使用してデータ エンティティを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6610d-137">This section describes how to create a data entity by using a wizard.</span></span> <span data-ttu-id="6610d-138">そのウィザードを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6610d-138">We recommend that you use the wizard.</span></span> <span data-ttu-id="6610d-139">分析コードの SFK フィールドを選択することのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="6610d-139">It requires only that you select the SFK field of the dimension.</span></span> <span data-ttu-id="6610d-140">ウィザードは、必要なデータ ソース、フィールド、リレーションをすべて正しく設定します。</span><span class="sxs-lookup"><span data-stu-id="6610d-140">The wizard creates the required data source, fields, and relations that have all the correct settings.</span></span>

1. <span data-ttu-id="6610d-141">**ファイル** &gt; **新規** &gt; **プロジェクト**とクリックして、新しい Microsoft Dynamics 365 for Finance and Operations プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6610d-141">Click **File** &gt; **New** &gt; **Project** to create a new Microsoft Dynamics 365 for Finance and Operations project.</span></span>
2. <span data-ttu-id="6610d-142">ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-142">In Solution Explorer, right-click your project, and then click **Properties**.</span></span> <span data-ttu-id="6610d-143">プロジェクトの **プロパティ ページ** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="6610d-143">The **Property Pages** dialog box for your project opens.</span></span>
3. <span data-ttu-id="6610d-144">**プロパティ ページ** ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6610d-144">In the **Property Pages** dialog box, follow these steps:</span></span>
   1.  <span data-ttu-id="6610d-145">**モデル**プロパティの値を**アプリケーション スイート単体テスト**に変更し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-145">Change the value of the **Model** property to **Application Suite Unit tests**, and then click **OK**.</span></span> <span data-ttu-id="6610d-146">このプロパティはプロジェクトごとに 1 回のみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6610d-146">You must set this property only one time per project.</span></span>
   2.  <span data-ttu-id="6610d-147">**ビルドでのデータベースの同期**プロパティの値を **True** に変更し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-147">Change the value of the **Synchronize database on build** property to **True**, and then click **OK**.</span></span> <span data-ttu-id="6610d-148">このプロパティはプロジェクトごとに 1 回のみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6610d-148">You must set this property only one time per project.</span></span>

   <span data-ttu-id="6610d-149">[![プロジェクト プロパティの設定](./media/dim2.png)](./media/dim2.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-149">[![Setting the project properties](./media/dim2.png)](./media/dim2.png)</span></span>

4. <span data-ttu-id="6610d-150">**DimensionTestEntity** という名前の新しいエンティティを作成し、プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="6610d-150">Create a new entity that is named **DimensionTestEntity**, and add it to the project.</span></span> <span data-ttu-id="6610d-151">**追加** ボタンをクリックすると、**データ エンティティ ビュー** ウィザードが起動します。</span><span class="sxs-lookup"><span data-stu-id="6610d-151">When you click the **Add** button, the **Data Entity View** wizard starts.</span></span> <span data-ttu-id="6610d-152">**インストール済み** で、**Dynamics 365 アーティファクト** を選択してから **データ モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6610d-152">Under **Installed**, then select **Dynamics 365 Artifacts**, then selec **Data Model**.</span></span> <span data-ttu-id="6610d-153">リストから **データ エンティティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6610d-153">Select **Data Entity** from the list.</span></span> <span data-ttu-id="6610d-154">**注記:** データ エンティティおよびその他の項目について説明する名前付け規則のドキュメントは発展し続けています。</span><span class="sxs-lookup"><span data-stu-id="6610d-154">**Note:** A naming convention document is evolving that covers data entities and other items.</span></span>
5. <span data-ttu-id="6610d-155">次のスクリーン ショットに表示される作成するデータ エンティティのプロパティ値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6610d-155">Specify the property values for the data entity that you're creating, as shown in the following screen shot.</span></span> <span data-ttu-id="6610d-156">**注記:** 最も重要なフィールドは **DimensionEntityTestTable** を選択する**プライマリ データ ソース**です。</span><span class="sxs-lookup"><span data-stu-id="6610d-156">**Note:** The most important field is **Primary data source**, where you select **DimensionEntityTestTable**.</span></span>

   <span data-ttu-id="6610d-157">[![エンティティ プロパティの設定](./media/dim4.png)](./media/dim4.png)**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-157">[![Setting the entity properties](./media/dim4.png)](./media/dim4.png) Click **Next**.</span></span>

6. <span data-ttu-id="6610d-158">プライマリ データ ソース、**DimensionEntityTestTable** からエンティティにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6610d-158">Add fields to the entity from the primary data source, **DimensionEntityTestTable**:</span></span>
   1.  <span data-ttu-id="6610d-159">すべてのフィールドの選択を解除するには、**すべて選択**チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="6610d-159">Clear the **Select all** check box to deselect all fields.</span></span> 

       <span data-ttu-id="6610d-160">[![すべてのフィールドの選択解除](./media/dim5.png)](./media/dim5.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-160">[![Deselecting all fields](./media/dim5.png)](./media/dim5.png)</span></span>

   2.  <span data-ttu-id="6610d-161">次の各フィールドのチェック ボックスを手動で選択します。</span><span class="sxs-lookup"><span data-stu-id="6610d-161">Manually select the check box for each of the following fields:</span></span>
       -   <span data-ttu-id="6610d-162">FieldDimensionDefault</span><span class="sxs-lookup"><span data-stu-id="6610d-162">FieldDimensionDefault</span></span>
       -   <span data-ttu-id="6610d-163">FieldAlternativeKey</span><span class="sxs-lookup"><span data-stu-id="6610d-163">FieldAlternativeKey</span></span>

       <span data-ttu-id="6610d-164">[![エンティティのフィールドの選択](./media/dim6.png)](./media/dim6.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-164">[![Selecting fields for the entity](./media/dim6.png)](./media/dim6.png)</span></span>

   3.  <span data-ttu-id="6610d-165">新しいデータ エンティティをプロジェクトに追加するには、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-165">Click **Finish** to add the new data entity to your project.</span></span> <span data-ttu-id="6610d-166">エンティティのノードは、ソリューション エクスプローラーで表示されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-166">A node for the entity appears in Solution Explorer.</span></span> 

       <span data-ttu-id="6610d-167">[![ソリューション エクスプ ローラー内のエンティティ ノード](./media/dim7.png)](./media/dim7.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-167">[![The entity node in Solution Explorer](./media/dim7.png)](./media/dim7.png)</span></span>

7. <span data-ttu-id="6610d-168">**ビルド** &gt; **ソリューションのビルド**とクリックし、プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="6610d-168">Click **Build** &gt; **Build Solution** to build your project.</span></span>
8. <span data-ttu-id="6610d-169">**エラー** ウィンドウで、エラーなくビルドが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6610d-169">In the **Errors** pane, verify that the build was completed without any errors.</span></span> <span data-ttu-id="6610d-170">プロセスのこのステージでは、警告が容認されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-170">At this stage in the process, warnings are tolerated.</span></span>
9. <span data-ttu-id="6610d-171">**DimensionTestEntity** のプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="6610d-171">Validate the properties of **DimensionTestEntity**.</span></span> <span data-ttu-id="6610d-172">ソリューション エクスプローラーで、**DimensionTestEntity** ノードを選択し、**プロパティ** ウィンドウの値を、次のスクリーンショットの値と比較します。</span><span class="sxs-lookup"><span data-stu-id="6610d-172">In Solution Explorer, select the **DimensionTestEntity** node, and compare the values in the **Properties** pane values to the values in the following screen shot.</span></span> 

   <span data-ttu-id="6610d-173">[![プロパティ](./media/dim8.png)](./media/dim8.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-173">[![Properties](./media/dim8.png)](./media/dim8.png)</span></span>

10. <span data-ttu-id="6610d-174">ソリューション エクスプローラーで、**DimensionTestEntity** ノードを右クリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6610d-174">In Solution Explorer, right-click the **DimensionTestEntity** node, and then click **Open**.</span></span> <span data-ttu-id="6610d-175">エンティティのデザイナーが中央のウィンドウに開きます。</span><span class="sxs-lookup"><span data-stu-id="6610d-175">The designer for the entity opens in the middle pane.</span></span> 

    <span data-ttu-id="6610d-176">[![エンティティ デザイナー](./media/dim9.png)](./media/dim9.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-176">[![Entity designer](./media/dim9.png)](./media/dim9.png)</span></span>

11. <span data-ttu-id="6610d-177">**DimensionTestEntity** のデザイナーで、**フィールド** &gt; **FieldDimensionDefaultDisplayValue** と展開し、**FieldDimensionDefaultDisplayValue** フィールドのノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6610d-177">In the designer for **DimensionTestEntity**, expand **Fields** &gt; **FieldDimensionDefaultDisplayValue**, and select the node for the **FieldDimensionDefaultDisplayValue** field.</span></span>
12. <span data-ttu-id="6610d-178">**プロパティ** ウィンドウで、**AccessModifier** プロパティの値を**プライベート**から**パブリック**に変更します。</span><span class="sxs-lookup"><span data-stu-id="6610d-178">In the **Properties** pane, change the value of the **AccessModifier** property from **Private** to **Public**.</span></span> 

    <span data-ttu-id="6610d-179">[![AccessModifier プロパティの設定](./media/dim10.png)](./media/dim10.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-179">[![Setting the AccessModifier property](./media/dim10.png)](./media/dim10.png)</span></span>

13. <span data-ttu-id="6610d-180">データ エンティティで **persistEntity** メソッドをオーバーライドし、次の X++ コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="6610d-180">Override the **persistEntity** method on the data entity, and enter the following X++ code.</span></span> 

    <span data-ttu-id="6610d-181">[![persistEntity メソッドを上書きします](./media/dim11.png)](./media/dim11.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-181">[![Overriding the persistEntity method](./media/dim11.png)](./media/dim11.png)</span></span>

14. <span data-ttu-id="6610d-182">テストでは、既存の単位テスト クラス、**DimensionEntityTest** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6610d-182">For testing, see the existing unit test class, **DimensionEntityTest**.</span></span>

## <a name="manually-configure-and-understand-default-dimensions"></a><span data-ttu-id="6610d-183">既定の分析コードを手動で構成して理解する</span><span class="sxs-lookup"><span data-stu-id="6610d-183">Manually configure and understand default dimensions</span></span>
<span data-ttu-id="6610d-184">このセクションでは、新しいエンティティに分析コード データソースを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6610d-184">This section describes how to add a dimension data source to a new entity.</span></span> <span data-ttu-id="6610d-185">新しいエンティティでは、分析コード テーブルの分析コード表示値が必要です。</span><span class="sxs-lookup"><span data-stu-id="6610d-185">The new entity requires the dimension display value from the dimension tables.</span></span>

1.  <span data-ttu-id="6610d-186">新しいエンティティで、次のスクリーン ショットに表示されるプロパティ値が含まれるデータ ソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="6610d-186">On a new entity, create a data source that has the property values that are shown in the following screen shot.</span></span> <span data-ttu-id="6610d-187">特に、次の表に記載されているプロパティの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="6610d-187">In particular, notice the settings for the properties that are described in the following table.</span></span>

    | <span data-ttu-id="6610d-188">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="6610d-188">Property name</span></span> | <span data-ttu-id="6610d-189">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="6610d-189">Property value</span></span>            | <span data-ttu-id="6610d-190">説明</span><span class="sxs-lookup"><span data-stu-id="6610d-190">Description</span></span>           |
    |---------------|---------------------------|-----------------------|
    | <span data-ttu-id="6610d-191">追加を許可</span><span class="sxs-lookup"><span data-stu-id="6610d-191">Allow Add</span></span>     | <span data-ttu-id="6610d-192">無</span><span class="sxs-lookup"><span data-stu-id="6610d-192">No</span></span>                        |                       |
    | <span data-ttu-id="6610d-193">読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="6610d-193">Is Read Only</span></span>  | <span data-ttu-id="6610d-194">有</span><span class="sxs-lookup"><span data-stu-id="6610d-194">Yes</span></span>                       |                       |
    | <span data-ttu-id="6610d-195">結合モード</span><span class="sxs-lookup"><span data-stu-id="6610d-195">Join Mode</span></span>     | <span data-ttu-id="6610d-196">OuterJoin</span><span class="sxs-lookup"><span data-stu-id="6610d-196">OuterJoin</span></span>                 |                       |
    | <span data-ttu-id="6610d-197">氏名</span><span class="sxs-lookup"><span data-stu-id="6610d-197">Name</span></span>          | <span data-ttu-id="6610d-198">FieldDimensionDefaultDAVS</span><span class="sxs-lookup"><span data-stu-id="6610d-198">FieldDimensionDefaultDAVS</span></span> | <span data-ttu-id="6610d-199">値は、4 文字のリテラル「DAVS」をデータ ソースの SFK フィールドの名前に追加することによって導出されます。</span><span class="sxs-lookup"><span data-stu-id="6610d-199">The value is derived by appending the four-character literal "DAVS" to the name of the SFK field from the data source.</span></span>                                         |
    | <span data-ttu-id="6610d-200">テーブル</span><span class="sxs-lookup"><span data-stu-id="6610d-200">Table</span></span>         | <span data-ttu-id="6610d-201">DimensionSetEntity</span><span class="sxs-lookup"><span data-stu-id="6610d-201">DimensionSetEntity</span></span>        | <span data-ttu-id="6610d-202">データ ソースのデータ エンティティに選択した名前。</span><span class="sxs-lookup"><span data-stu-id="6610d-202">The name that you chose for the data entity for the data source.</span></span> <span data-ttu-id="6610d-203">ここで示される値、**DimensionSetEntity** は、DefaultDimension パターンのフレームワーク分析コード データ エンティティです。</span><span class="sxs-lookup"><span data-stu-id="6610d-203">The value that is shown here, **DimensionSetEntity**, is a framework dimension data entity for the DefaultDimension pattern.</span></span> |

    <span data-ttu-id="6610d-204">[![データ ソース プロパティ](./media/dim12.png)](./media/dim12.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-204">[![Data source properties](./media/dim12.png)](./media/dim12.png)</span></span>

2.  <span data-ttu-id="6610d-205">分析コード SFK のプライベート フィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="6610d-205">Create a private field for the dimension SFK.</span></span> <span data-ttu-id="6610d-206">このエンティティ フィールドでは、ソース フィールドは、**FieldDimensionDefault**SFK フィールドです。</span><span class="sxs-lookup"><span data-stu-id="6610d-206">For this entity field, the source field is the **FieldDimensionDefault** SFK field.</span></span>

    <span data-ttu-id="6610d-207">[![dim13fixed](./media/dim13fixed.png)](./media/dim13fixed.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-207">[![dim13fixed](./media/dim13fixed.png)](./media/dim13fixed.png)</span></span>

3.  <span data-ttu-id="6610d-208">分析コード表示値のパブリック フィールドを作成し、前の手順で作成したデータ ソースにバインドします。</span><span class="sxs-lookup"><span data-stu-id="6610d-208">Create a public field for the dimension display value, and bind it to the data source that you created in a previous step.</span></span> <span data-ttu-id="6610d-209">分析コード表示値フィールドの名前は、12 文字のリテラル「DisplayValue」が付加されるプライベート フィールド名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6610d-209">The name of the dimension display value field must be the private field name, to which the twelve-character literal “DisplayValue” is appended.</span></span>

    <span data-ttu-id="6610d-210">[![dim14fixed](./media/dim14fixed.png)](./media/dim14fixed.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-210">[![dim14fixed](./media/dim14fixed.png)](./media/dim14fixed.png)</span></span>

4.  <span data-ttu-id="6610d-211">エンティティ リレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6610d-211">Add an entity relation.</span></span> <span data-ttu-id="6610d-212">エンティティ リレーションはエンティティ間の OData ナビゲーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6610d-212">An entity relation will enable OData navigation between entities.</span></span> <span data-ttu-id="6610d-213">リレーションの名前は、「DimensionSet」が付加されたプライベート分析コード フィールド名の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6610d-213">The name of the relation should be the name of the private dimension field name, to which “DimensionSet” is appended.</span></span> <span data-ttu-id="6610d-214">**DimensionSetEntity** のパブリック名は **DimensionSet** です。</span><span class="sxs-lookup"><span data-stu-id="6610d-214">The public name for **DimensionSetEntity** is **DimensionSet**.</span></span> <span data-ttu-id="6610d-215">したがって、そのエンティティへのナビゲーションには意味のある名前が必要です。</span><span class="sxs-lookup"><span data-stu-id="6610d-215">Therefore, the navigation to that entity should have a meaningful name.</span></span> <span data-ttu-id="6610d-216">適切な選択は、SFK に "DimensionSet"をたした分析コードの名前です。</span><span class="sxs-lookup"><span data-stu-id="6610d-216">A good choice is the name of the dimension SFK plus “DimensionSet.”</span></span>

    <span data-ttu-id="6610d-217">[![dim15fixed](./media/dim15fixed.png)](./media/dim15fixed.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-217">[![dim15fixed](./media/dim15fixed.png)](./media/dim15fixed.png)</span></span>

5.  <span data-ttu-id="6610d-218">**persistEntity** メソッドをオーバーライドし、次の X++ コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="6610d-218">Override the **persistEntity** method, and enter the following X++ code.</span></span> 

    <span data-ttu-id="6610d-219">[![persistEntity メソッドを上書きします](./media/dim16.png)](./media/dim16.png)</span><span class="sxs-lookup"><span data-stu-id="6610d-219">[![Overriding the persistEntity method](./media/dim16.png)](./media/dim16.png)</span></span>





