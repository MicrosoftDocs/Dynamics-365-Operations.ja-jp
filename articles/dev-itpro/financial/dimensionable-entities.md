---
title: "財務分析コードとして使用可能なバッキング テーブルの作成"
description: "このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。"
author: aprilolson
manager: AnnBe
ms.date: 04/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 191363
ms.assetid: 
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 645255266e99b5d096b6ce1ae7a48ea00da46543
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="make-a-backing-table-be-consumable-as-a-financial-dimension"></a><span data-ttu-id="570e2-103">財務分析コードとして使用可能なバッキング テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="570e2-103">Make a backing table be consumable as a Financial dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="570e2-104">このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="570e2-104">This topic provides the steps that you need to follow if you want to make a backing table usable as a Financial dimension.</span></span>

> <span data-ttu-id="570e2-105">[**!重要**] 再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しません。</span><span class="sxs-lookup"><span data-stu-id="570e2-105">[**!IMPORTANT**] Do not create financial dimensions that have values that are not reusable or use one-to-one dimension value combinations.</span></span> 
-   <span data-ttu-id="570e2-106">財務分析コードは、トランザクションおよび分析プロセスに必要な再利用可能な値にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-106">Financial dimensions should be reusable values needed for transaction and analytical processes.</span></span> <span data-ttu-id="570e2-107">これらの分析コードは、複数のトランザクションにわたって全体的な再利用を提供できるデータのソースを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-107">These dimensions should represent sources of data that can provide high level of reuse across multiple transactions.</span></span> <span data-ttu-id="570e2-108">他の分析コード値に表示される際、高変動を表す ID データを供給するバッキング テーブルを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="570e2-108">Do not select a backing table that supplies identity data that represents high volatility when represented with other dimension values.</span></span> <span data-ttu-id="570e2-109">これにより、ストレージと処理のコストが増加し、パフォーマンスと分析の価値に悪影響を及ぼします。</span><span class="sxs-lookup"><span data-stu-id="570e2-109">This can increase storage and processing costs and negatively impact performance and analytical value.</span></span>

<span data-ttu-id="570e2-110">揮発性の高いデータの例には、次のような頻繁に増分されるタイムスタンプと識別子が含まれます。- ドキュメント - 販売注文 - 発注書 - トランザクション - 小切手 - シリアル - チケット - ライセンス番号</span><span class="sxs-lookup"><span data-stu-id="570e2-110">Examples of highly volatile data include timestamps and identifiers that are frequently incremented, such as: - Documents - Sales orders - Purchase orders - Transactions - Checks - Serials - Tickets - License numbers</span></span> 

<span data-ttu-id="570e2-111">これらは縮退分析コードと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="570e2-111">These are referred to as degenerate dimensions.</span></span> <span data-ttu-id="570e2-112">これらの値の追跡は、財務分析コード以外で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-112">Tracking these values should be done outside of financial dimensions.</span></span> <span data-ttu-id="570e2-113">つまり、情報を必要とするトランザクション レコードのカスタマイズを使用する必要があります。これらの値は、財務分析コード値と共に保存しないでください。</span><span class="sxs-lookup"><span data-stu-id="570e2-113">This means that you should use customizations for the transactional records that need information, and these values should not be stored along with the financial dimension values.</span></span>


<span data-ttu-id="570e2-114">次の手順に従うことにより、**財務分析コード** ページの**値の使用元**のドロップダウン メニューにビューが自動的に表示され、値は**財務分析コード値**ページに入力されます。</span><span class="sxs-lookup"><span data-stu-id="570e2-114">By following these steps, your view will automatically appear in the **Use values from** drop-down menu on the **Financial dimensions** page, and the values will be populated on the **Financial dimension values** page.</span></span>


> [!NOTE]
> <span data-ttu-id="570e2-115">分析コードが **OMOperatingUnit** テーブルによってサポートされている場合、手順の多くは既に完了しています。</span><span class="sxs-lookup"><span data-stu-id="570e2-115">If your dimension is backed by the **OMOperatingUnit** table then many of the steps are already completed for you.</span></span> <span data-ttu-id="570e2-116">「[新しい OMOperatingUnit タイプがサポートしているエンティティを追加](#add-a-new-omoperatingunit-type-backed-entity)」セクション の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="570e2-116">Follow the steps in the "[Add a new OMOperatingUnit type backed entity](#add-a-new-omoperatingunit-type-backed-entity)" section.</span></span>

## <a name="step-1-create-a-view"></a><span data-ttu-id="570e2-117">手順 1: ビューを作成する</span><span class="sxs-lookup"><span data-stu-id="570e2-117">Step 1: Create a view</span></span>

<span data-ttu-id="570e2-118">最初のステップは、バッキング テーブルと同じモデルでビューを作成することです。</span><span class="sxs-lookup"><span data-stu-id="570e2-118">The first step is to create a view in the same model as your backing table.</span></span> <span data-ttu-id="570e2-119">以下の手順を実行する前に、**テーブルのプロパティ** ウィンドウでバッキング テーブルが **Create Rec Id Index = Yes** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="570e2-119">Before you complete the following steps, verify that the backing table has **Create Rec Id Index = Yes** in the **Table Properties** pane.</span></span> <span data-ttu-id="570e2-120">または、テーブルに一意のインデックスがあり、RECID がそのインデックスの最初のセグメントであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="570e2-120">Alternatively, ensure that the table has a unique index and RECID is the first segment of that index.</span></span>

1.  <span data-ttu-id="570e2-121">プロジェクトで**追加** > **新しい項目**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="570e2-121">In your project, click **Add** > **New Item**.</span></span> <span data-ttu-id="570e2-122">**表示** を選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="570e2-122">Select **View** and then click **Add**.</span></span>
1.  <span data-ttu-id="570e2-123">**表示** を右クリックし、**名前の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-123">Right-click **View** and select **Rename**.</span></span> <span data-ttu-id="570e2-124">ビューに **DimAttribute**[BackingTableName] と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="570e2-124">Name the view **DimAttribute**[BackingTableName].</span></span> <span data-ttu-id="570e2-125">たとえば、DimAttributeCustTable。</span><span class="sxs-lookup"><span data-stu-id="570e2-125">For example, DimAttributeCustTable.</span></span>
1.  <span data-ttu-id="570e2-126">**メタデータの表示**を展開し、テーブルを画面上の**データ ソース**ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="570e2-126">Expand **View Metadata**, and then drag your table to the **Data Sources** node on the view.</span></span>
1.  <span data-ttu-id="570e2-127">ノードの名前を **BackingTableName** から **BackingEntity** に変更します。</span><span class="sxs-lookup"><span data-stu-id="570e2-127">Rename the node from **BackingTableName** to **BackingEntity**.</span></span>
1.  <span data-ttu-id="570e2-128">財務分析コードとして使用するテーブルのキー、値、および名前を識別します。</span><span class="sxs-lookup"><span data-stu-id="570e2-128">Identify the key, value, and name for the table that you want to use as a financial dimension.</span></span> <span data-ttu-id="570e2-129">フィールドを検索して、BackingEntity データ ソースの一覧にドラッグし、またはデータ ソース上のフィールドにコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="570e2-129">Find the fields and drag to the BackingEntity data source list, or copy and paste the fields on the data source.</span></span> <span data-ttu-id="570e2-130">3 つのフィールドの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="570e2-130">Rename the three fields to:</span></span>
      + <span data-ttu-id="570e2-131">**キー** – これは代理キーで、通常は RecID です。</span><span class="sxs-lookup"><span data-stu-id="570e2-131">**Key** – This is the surrogate key, typically the RecID.</span></span>
      + <span data-ttu-id="570e2-132">**値** - これは、AccountNum のようなナチュラル キーです。</span><span class="sxs-lookup"><span data-stu-id="570e2-132">**Value** - This is the natural key, for example the AccountNum.</span></span> <span data-ttu-id="570e2-133">最大 30 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="570e2-133">It is a string up to 30 characters.</span></span>
      + <span data-ttu-id="570e2-134">**名前** – これは説明で、通常は**名前**または**説明**フィールドです。</span><span class="sxs-lookup"><span data-stu-id="570e2-134">**Name** – This is the description, which is typically the **Name** or **Description** field.</span></span> <span data-ttu-id="570e2-135">最大 60 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="570e2-135">It is a string up to 60 characters.</span></span>
1.  <span data-ttu-id="570e2-136">バッキング テーブルがデータを削除する場合、ビューで **範囲** を作成することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-136">You may need to create a **Range** on the view if the backing table removes data.</span></span> <span data-ttu-id="570e2-137">たとえば、作業単位を使用し部門のみを必要とする場合、その作業単位の範囲を使用します。</span><span class="sxs-lookup"><span data-stu-id="570e2-137">For example, if you are using an Operating unit and only want Department, you will want to use the range for that operating unit.</span></span>
1.  <span data-ttu-id="570e2-138">**新しいインデックス** を右クリックし、**新しいインデックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-138">Right-click **Indexes** and select **New Index**.</span></span> <span data-ttu-id="570e2-139">**プロパティ** ウィンドウでデータ フィールドとして **値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-139">Select **Value** as the Data field on the **Properties** pane.</span></span> <span data-ttu-id="570e2-140">必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **いいえ** にセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-140">You can rename the index if needed, however you need to set **Allow Duplicates** to **No**.</span></span>
1. <span data-ttu-id="570e2-141">**新しいインデックス** を右クリックし、**新しいインデックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-141">Right-click **Indexes** and select **New Index**.</span></span> <span data-ttu-id="570e2-142">**プロパティ** ウィンドウでデータ フィールドとして **名前** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-142">Select **Name** as the Data field on the **Properties** pane.</span></span> <span data-ttu-id="570e2-143">必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **はい** にセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-143">You can rename the index if needed, however you need to set **Allow Duplicates** to **Yes**.</span></span>
1. <span data-ttu-id="570e2-144">**表示**をクリックし、**プロパティ** ウィンドウで、選択した参照ラベル ID に **単数形ラベル** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="570e2-144">Click **View**, and in the **Properties** pane, set the **Singular label** field to the reference label ID of your choice.</span></span> <span data-ttu-id="570e2-145">これは、顧客などの単一の値を示すラベルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-145">This should be the label that indicates a single value, such as Customer.</span></span>
1. <span data-ttu-id="570e2-146">**ラベル** フィールドを選択した参照ラベル ID に設定します。</span><span class="sxs-lookup"><span data-stu-id="570e2-146">Set the **Label** field to the reference label ID of your choice.</span></span> <span data-ttu-id="570e2-147">これは、顧客などの複数の値を示すラベルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-147">This should be the label that indicates multiple values, such as Customers.</span></span> <span data-ttu-id="570e2-148">この値は、**財務分析コード** ページの **Use Values from** フィールドのドロップダウン リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="570e2-148">This value will show in the drop-down list in the **Use Values from** field on the **Financial dimensions** page.</span></span>
1. <span data-ttu-id="570e2-149">**プロパティ**ウィンドウの **TitleField1** フィールドに、**値**を入力します。</span><span class="sxs-lookup"><span data-stu-id="570e2-149">Enter **Value** in the **TitleField1** field in the **Properties** pane.</span></span>
1. <span data-ttu-id="570e2-150">**プロパティ**ウィンドウの **TitleField2** フィールドに、**名前**を入力します。</span><span class="sxs-lookup"><span data-stu-id="570e2-150">Enter **Name** in the **TitleField2** field in the **Properties** pane.</span></span>
1. <span data-ttu-id="570e2-151">バッキング テーブルのプロパティを確認し、使用している config キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="570e2-151">Review the backing table properties and identify the config key it is using.</span></span> <span data-ttu-id="570e2-152">**表示**で、バッキング テーブルと同じ**コンフィギュレーション キー**を入力します。</span><span class="sxs-lookup"><span data-stu-id="570e2-152">On **View**, enter the same **Configuration key** as the backing table.</span></span>
1. <span data-ttu-id="570e2-153">**DimensionEssentials** を検索してプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="570e2-153">Search for **DimensionEssentials** and add it to the Project.</span></span> <span data-ttu-id="570e2-154">**DimensionEssentials** を展開し、**アクセス許可**を右クリックし、その後**新しいアクセス許可**を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-154">Expand **DimensionEssentials**, right-click **Permissions**, and then select **New Permission**.</span></span> <span data-ttu-id="570e2-155">**プロパティ** ウィンドウで、**アクセス レベル**を**読み取り**に設定します。</span><span class="sxs-lookup"><span data-stu-id="570e2-155">In the **Properties** pane, set the **Access Level** to **Read**.</span></span> <span data-ttu-id="570e2-156">**セキュリティ権限**をクリックし、**読み取り**の**アクセス レベル**を**アクセス許可**ノードの下に追加します。</span><span class="sxs-lookup"><span data-stu-id="570e2-156">Click **Security Privilege** and add the view under the **Permissions** node with an **Access Level** of **Read**.</span></span> <span data-ttu-id="570e2-157">これらの 1 つを使用しているモデルに拡張することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-157">You may need to extend one of these into the model that you're using.</span></span>
1. <span data-ttu-id="570e2-158">**表示** を右クリックし、**コードの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-158">Right-click **View** and select **View Code**.</span></span> <span data-ttu-id="570e2-159">ビューに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="570e2-159">Add the following code to the view.</span></span> <span data-ttu-id="570e2-160">これにより、分析コード フレームワークに登録されます。</span><span class="sxs-lookup"><span data-stu-id="570e2-160">This will register it in the dimension framework.</span></span> <span data-ttu-id="570e2-161">CustTable に対して作成されたビューを使用する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="570e2-161">Here is an example using the view created for CustTable.</span></span>
      ```
      [SubscribesTo(classstr(DimensionEnabledType),
      delegatestr(DimensionEnabledType,
      registerDimensionEnabledTypeIdentifiersDelegate))]

      public static void registerDimensionEnabledTypeIdentifier(DimensionIEnabledType _dimensionEnabledType)
      {
         _dimensionEnabledType.registerViewIdentifier(tablestr(DimAttribute**CustTable**));
      }
      ```
1. <span data-ttu-id="570e2-162">**Microsoft Dynamics 365** を選択して **オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="570e2-162">Select **Microsoft Dynamics 365** and click **Options**.</span></span> <span data-ttu-id="570e2-163">**ベスト プラクティス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="570e2-163">Select **Best Practices**.</span></span> <span data-ttu-id="570e2-164">モデルを選択し、**Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker** が表示されるまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="570e2-164">Select your model and then scroll until you find **Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker**.</span></span> <span data-ttu-id="570e2-165">ルールとその子が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="570e2-165">Verify that the rule and its children are selected.</span></span>
1.  <span data-ttu-id="570e2-166">ビューをビルドしてから同期します。</span><span class="sxs-lookup"><span data-stu-id="570e2-166">Build and then synchronize the view.</span></span>

## <a name="step-2-validate-that-the-view-returns-the-correct-data-in-sql"></a><span data-ttu-id="570e2-167">手順 2: ビューが SQL で正しいデータを返すことを検証する</span><span class="sxs-lookup"><span data-stu-id="570e2-167">Step 2: Validate that the view returns the correct data in SQL</span></span>

<span data-ttu-id="570e2-168">この時点で SQL Server Management Studio で次のクエリを実行して、正しいデータが引き出されているかを確認をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-168">At this point you should be able to run the following query in SQL Server Management Studio to ensure that it's pulling the correct data.</span></span> <span data-ttu-id="570e2-169">CustTable に対して作成されたビューを使用する省略例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="570e2-169">Here is an abbreviated example using the view created for CustTable.</span></span>

      select * from DIMATTRIBUTECUSTTABLE
    

| <span data-ttu-id="570e2-170">KEY_</span><span class="sxs-lookup"><span data-stu-id="570e2-170">KEY_</span></span>   | <span data-ttu-id="570e2-171">値</span><span class="sxs-lookup"><span data-stu-id="570e2-171">VALUE</span></span>    | <span data-ttu-id="570e2-172">データ範囲 ID</span><span class="sxs-lookup"><span data-stu-id="570e2-172">DATA AREA ID</span></span> | <span data-ttu-id="570e2-173">パーティション</span><span class="sxs-lookup"><span data-stu-id="570e2-173">PARTITION</span></span> | <span data-ttu-id="570e2-174">RECID</span><span class="sxs-lookup"><span data-stu-id="570e2-174">RECID</span></span>   | <span data-ttu-id="570e2-175">氏名</span><span class="sxs-lookup"><span data-stu-id="570e2-175">NAME</span></span>           | <span data-ttu-id="570e2-176">パーティション 2</span><span class="sxs-lookup"><span data-stu-id="570e2-176">PARTITION #2</span></span> |
|-------------|--------------|----------------|---------------|-------------|--------------------|------------------|
| <span data-ttu-id="570e2-177">22565425322</span><span class="sxs-lookup"><span data-stu-id="570e2-177">22565425322</span></span> | <span data-ttu-id="570e2-178">US\_SI\_0129</span><span class="sxs-lookup"><span data-stu-id="570e2-178">US\_SI\_0129</span></span> | <span data-ttu-id="570e2-179">ussi</span><span class="sxs-lookup"><span data-stu-id="570e2-179">ussi</span></span>           | <span data-ttu-id="570e2-180">5637144576</span><span class="sxs-lookup"><span data-stu-id="570e2-180">5637144576</span></span>    | <span data-ttu-id="570e2-181">22565425322</span><span class="sxs-lookup"><span data-stu-id="570e2-181">22565425322</span></span> | <span data-ttu-id="570e2-182">Adventure Services</span><span class="sxs-lookup"><span data-stu-id="570e2-182">Adventure Services</span></span> | <span data-ttu-id="570e2-183">5637144576</span><span class="sxs-lookup"><span data-stu-id="570e2-183">5637144576</span></span>       |
| <span data-ttu-id="570e2-184">22565424579</span><span class="sxs-lookup"><span data-stu-id="570e2-184">22565424579</span></span> | <span data-ttu-id="570e2-185">US\_SI\_0128</span><span class="sxs-lookup"><span data-stu-id="570e2-185">US\_SI\_0128</span></span> | <span data-ttu-id="570e2-186">ussi</span><span class="sxs-lookup"><span data-stu-id="570e2-186">ussi</span></span>           | <span data-ttu-id="570e2-187">5637144576</span><span class="sxs-lookup"><span data-stu-id="570e2-187">5637144576</span></span>    | <span data-ttu-id="570e2-188">22565424579</span><span class="sxs-lookup"><span data-stu-id="570e2-188">22565424579</span></span> | <span data-ttu-id="570e2-189">アルペン エレクトロニクス</span><span class="sxs-lookup"><span data-stu-id="570e2-189">Alpine Electronics</span></span> | <span data-ttu-id="570e2-190">5637144576</span><span class="sxs-lookup"><span data-stu-id="570e2-190">5637144576</span></span>       |


## <a name="step-3-override-methods-on-the-backing-table"></a><span data-ttu-id="570e2-191">手順 3: バッキング テーブルでメソッドを上書きする</span><span class="sxs-lookup"><span data-stu-id="570e2-191">Step 3: Override methods on the backing table</span></span>

<span data-ttu-id="570e2-192">バッキング テーブルのナチュラル キーを削除または名前を変更するときに分析コード フレームワークと統合するには、バッキング テーブルの delete メソッドと、update または renamePrimaryKey メソッドにカスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-192">To integrate with the dimensions framework when deleting or renaming the natural key of the backing table, you must write custom code on the backing table's delete method, and on either the update or renamePrimaryKey method.</span></span> <span data-ttu-id="570e2-193">テーブルがナチュラル キーの更新をブロックする場合、renamePrimaryKey のオーバーライドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-193">If your table blocks updates of the natural key, you will need to use the renamePrimaryKey override.</span></span> <span data-ttu-id="570e2-194">存在しない場合は、更新メソッドでコードを格納できます。</span><span class="sxs-lookup"><span data-stu-id="570e2-194">If it does not, then you can put the code in the update method.</span></span> <span data-ttu-id="570e2-195">CustTable からの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="570e2-195">Here is an example from CustTable.</span></span>

```
public void delete()
{
    if (!DimensionValidation::canDeleteEntityValue(this))
    {
        throw error(strFmt("\@SYS134392", this.AccountNum));
    }
      
    ttsbegin;
    DimensionAttributeValue::updateForEntityValueDelete(this);
    ttscommit;
}
   
public void update()
{
    Common originalRecord = this.orig();
    super();
    DimensionValueRename::syncRenamedValue(this, originalRecord);
}
   
public void renamePrimaryKey()
{
    Common originalRecord = this.orig();
    super();
    DimensionValueRename::syncRenamedValue(this, originalRecord);
}
```

## <a name="step-4-clear-caches-to-force-detection-of-the-new-view"></a><span data-ttu-id="570e2-196">手順 4: キャッシュをクリアして新しいビューの検出を強制的する</span><span class="sxs-lookup"><span data-stu-id="570e2-196">Step 4: Clear caches to force detection of the new view</span></span>

<span data-ttu-id="570e2-197">分析コードとして消費できるエンティティのリストはサーバー上でキャッシュされるため、キャッシュをクリアする呼び出しが実行されるか、クライアントとサーバーの両方が再起動されるまで新しいエンティティの作成は既存のエンティティのリストに表示されません。</span><span class="sxs-lookup"><span data-stu-id="570e2-197">Because the list of entities that can be consumed as a dimension are cached on the server, the creation of a new entity will not appear in the list of existing entities until a call to clear the caches is performed, or until both the client and the server are restarted.</span></span> <span data-ttu-id="570e2-198">キャッシュをクリアして新しいビューをすぐに表示させるには、実行可能なクラス内で次のコード行を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="570e2-198">To clear the caches and have the new view appear immediately, you must execute the following line of code within a runnable class.</span></span>

      DimensionCache::clearAllScopes();

## <a name="step-5-verify-that-the-dimension-appears-in-the-use-value-from-lookup"></a><span data-ttu-id="570e2-199">手順 5: 分析コードが [ルックアップからの値を使用] に表示されることを確認する</span><span class="sxs-lookup"><span data-stu-id="570e2-199">Step 5: Verify that the dimension appears in the Use Value From lookup</span></span>

<span data-ttu-id="570e2-200">手順を完了したら、総勘定元帳の**財務分析コード** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="570e2-200">Now that you have completed the steps, navigate to the **Financial dimensions** page in the General ledger.</span></span> <span data-ttu-id="570e2-201">**値の使用元**フィールドのドロップダウン メニューをクリックし、値が使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="570e2-201">Click the drop-down menu on the **Use Values from** field and verify that your value is available.</span></span>


## <a name="add-a-new-omoperatingunit-type-backed-entity"></a><span data-ttu-id="570e2-202">新しい OMOperatingUnit タイプがサポートしているエンティティの追加</span><span class="sxs-lookup"><span data-stu-id="570e2-202">Add a new OMOperatingUnit type backed entity</span></span>

<span data-ttu-id="570e2-203">新しい組織モデル OMOperatingUnitType 列挙が追加された場合、次元として使用可能にする手順は類似していますが、次のように短くすることができます。</span><span class="sxs-lookup"><span data-stu-id="570e2-203">If a new Organization Model OMOperatingUnitType enumeration is added, the steps to make it consumable as a dimension are similar but can be made shorter as follows:</span></span>

1. <span data-ttu-id="570e2-204">既存の DimAttributeOM [BackingTableName] ビューの 1 つをコピーし、適切に名前を変更して、関連するすべてのラベルとヘルプ テキストを調整します。</span><span class="sxs-lookup"><span data-stu-id="570e2-204">Copy one of the existing DimAttributeOM[BackingTableName] views, rename it appropriately, and then adjust all associated labels and help text.</span></span>
1. <span data-ttu-id="570e2-205">コピーしたビューで、Datasource\BackingEntity (OMOperatingUnit) \Ranges ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="570e2-205">Expand the Datasource\BackingEntity (OMOperatingUnit)\Ranges node on the copied view.</span></span> <span data-ttu-id="570e2-206">範囲内の値プロパティを、追加された新しい OMOperatingUnitType 列挙型に変更します。</span><span class="sxs-lookup"><span data-stu-id="570e2-206">Change the value property on the range to the new OMOperatingUnitType enumeration value that was just added.</span></span>
1. <span data-ttu-id="570e2-207">プロジェクトをビルドして同期します。</span><span class="sxs-lookup"><span data-stu-id="570e2-207">Build and synchronize the project.</span></span>
1. <span data-ttu-id="570e2-208">SQL でデータを検証するステップ２で始まるこのトピックの手順に従い、**値の使用**ルックアップで表示される分析コードを検証するステップ 5 まで続けます。</span><span class="sxs-lookup"><span data-stu-id="570e2-208">Follow the steps in this topic starting with Step 2, where you validate the data in SQL, and then continue through Step 5, where you validate that the dimension appears in the **Use Value From** lookup.</span></span>

<span data-ttu-id="570e2-209">**OMOperatingUnitType** は **OMOperatingUnit** テーブルによってサポートされているため、削除、更新および **renamePrimaryKey** メソッドを処理するための汎用コードがすでに存在します。</span><span class="sxs-lookup"><span data-stu-id="570e2-209">Because the **OMOperatingUnitType** is backed by the **OMOperatingUnit** table, generic code already exists to handle the delete, update, and **renamePrimaryKey** methods.</span></span> <span data-ttu-id="570e2-210">したがって、これらのメソッドを更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="570e2-210">Therefore, you do not need to update these methods.</span></span>

