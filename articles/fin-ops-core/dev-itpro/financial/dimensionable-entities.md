---
title: 財務分析コードとして使用可能なバッキング テーブルの作成
description: このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。
author: aprilolson
manager: AnnBe
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 191363
ms.assetid: ''
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e6830a25a1c4e2532b8038926637429413884f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191568"
---
# <a name="make-backing-tables-consumable-as-financial-dimensions"></a><span data-ttu-id="dc79d-103">財務分析コードとして使用可能なバッキング テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="dc79d-103">Make backing tables consumable as financial dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc79d-104">このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-104">This topic provides the steps that you need to follow if you want to make a backing table usable as a Financial dimension.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc79d-105">再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="dc79d-105">Do not create financial dimensions that have values that are not reusable or use one-to-one dimension value combinations.</span></span> <span data-ttu-id="dc79d-106">再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="dc79d-106">Do not create financial dimensions that have values that are not reusable or use one-to-one dimension value combinations.</span></span> <span data-ttu-id="dc79d-107">ビューを、DimAttribute の分析コード値のソースとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="dc79d-107">Views cannot be used as a source of dimension values for a DimAttribute.</span></span> <span data-ttu-id="dc79d-108">これはうまくいくように見えますが、分析コードのファクト データがデータベースにインポートされるようにするため、MR が行ごとの処理にフォールバックされます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-108">Although this may seem to work, it will cause MR to fall back to row-by-row processing in order to get the dimension fact data imported to the database.</span></span> <span data-ttu-id="dc79d-109">これにより、パフォーマンスがかなり低下したり、レポートが遮断されます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-109">This results in extremely slow performance or broken reports.</span></span> 

> <span data-ttu-id="dc79d-110">財務分析コードのデータのソースとして使用する基本テーブルには、30 文字以内の固有ナチュラル キー値が必用であり、その値はそのテーブル内の 1 つの RECID を解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-110">The primary table that is to be used as a source of financial dimension data MUST have a unique natural key value of 30 characters or less, and that value MUST resolve to a single RECID within that table.</span></span> <span data-ttu-id="dc79d-111">拡張された名前列は、追加のコンテキストをユーザーに表示する場合にのみ使用され、ナチュラル キー エントリの一意性を解決するためには使用されないため、もう 1 つのソース結合 (DirPartyTable や別の場所など) から取得できます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-111">The extended Name column can come from another source join (such as DirPartyTable or elsewhere) because it is used only for displaying additional context to the user and is not used to resolve uniqueness on natural key entry.</span></span>
     
<span data-ttu-id="dc79d-112">財務分析コードは、トランザクションおよび分析プロセスに必要な再利用可能な値にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-112">Financial dimensions should be reusable values needed for transaction and analytical processes.</span></span> <span data-ttu-id="dc79d-113">これらの分析コードは、複数のトランザクションにわたって全体的な再利用を提供できるデータのソースを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-113">These dimensions should represent sources of data that can provide high level of reuse across multiple transactions.</span></span> <span data-ttu-id="dc79d-114">他の分析コード値に表示される際、高変動を表す ID データを供給するバッキング テーブルを選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="dc79d-114">Do not select a backing table that supplies identity data that represents high volatility when represented with other dimension values.</span></span> <span data-ttu-id="dc79d-115">これにより、ストレージと処理のコストが増加し、パフォーマンスと分析の価値に悪影響を及ぼします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-115">This can increase storage and processing costs and negatively impact performance and analytical value.</span></span>

<span data-ttu-id="dc79d-116">揮発性の非常に高いデータの例としては、以下のように、頻繁に増分されるタイムスタンプや識別子などがあります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-116">Examples of highly volatile data include timestamps and identifiers that are frequently incremented, such as:</span></span>

 - <span data-ttu-id="dc79d-117">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="dc79d-117">Documents</span></span>
 - <span data-ttu-id="dc79d-118">販売注文</span><span class="sxs-lookup"><span data-stu-id="dc79d-118">Sales orders</span></span>
 - <span data-ttu-id="dc79d-119">発注書</span><span class="sxs-lookup"><span data-stu-id="dc79d-119">Purchase orders</span></span>
 - <span data-ttu-id="dc79d-120">トランザクション</span><span class="sxs-lookup"><span data-stu-id="dc79d-120">Transactions</span></span>
 - <span data-ttu-id="dc79d-121">小切手</span><span class="sxs-lookup"><span data-stu-id="dc79d-121">Checks</span></span>
 - <span data-ttu-id="dc79d-122">シリアル</span><span class="sxs-lookup"><span data-stu-id="dc79d-122">Serials</span></span>
 - <span data-ttu-id="dc79d-123">チケット</span><span class="sxs-lookup"><span data-stu-id="dc79d-123">Tickets</span></span>
 - <span data-ttu-id="dc79d-124">ライセンス番号</span><span class="sxs-lookup"><span data-stu-id="dc79d-124">License numbers</span></span> 

<span data-ttu-id="dc79d-125">これらは縮退分析コードと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-125">These are referred to as degenerate dimensions.</span></span> <span data-ttu-id="dc79d-126">これらの値の追跡は、財務分析コード以外で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-126">Tracking these values should be done outside of financial dimensions.</span></span> <span data-ttu-id="dc79d-127">つまり、情報を必要とするトランザクション レコードのカスタマイズを使用する必要があります。これらの値は、財務分析コード値と共に保存しないでください。</span><span class="sxs-lookup"><span data-stu-id="dc79d-127">This means that you should use customizations for the transactional records that need information, and these values should not be stored along with the financial dimension values.</span></span>

<span data-ttu-id="dc79d-128">次の手順に従うことにより、**財務分析コード** ページの**値の使用元**のドロップダウン メニューにビューが自動的に表示され、値は**財務分析コード値**ページに入力されます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-128">By following these steps, your view will automatically appear in the **Use values from** drop-down menu on the **Financial dimensions** page, and the values will be populated on the **Financial dimension values** page.</span></span>


> [!NOTE]
> <span data-ttu-id="dc79d-129">分析コードが **OMOperatingUnit** テーブルによってサポートされている場合、手順の多くは既に完了しています。</span><span class="sxs-lookup"><span data-stu-id="dc79d-129">If your dimension is backed by the **OMOperatingUnit** table then many of the steps are already completed for you.</span></span> <span data-ttu-id="dc79d-130">「[新しい OMOperatingUnit タイプがサポートしているエンティティを追加](#add-a-new-omoperatingunit-type-backed-entity)」セクション の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dc79d-130">Follow the steps in the "[Add a new OMOperatingUnit type backed entity](#add-a-new-omoperatingunit-type-backed-entity)" section.</span></span>

## <a name="step-1-create-a-view"></a><span data-ttu-id="dc79d-131">手順 1: ビューを作成する</span><span class="sxs-lookup"><span data-stu-id="dc79d-131">Step 1: Create a view</span></span>

<span data-ttu-id="dc79d-132">最初のステップは、バッキング テーブルと同じモデルでビューを作成することです。</span><span class="sxs-lookup"><span data-stu-id="dc79d-132">The first step is to create a view in the same model as your backing table.</span></span> <span data-ttu-id="dc79d-133">以下の手順を実行する前に、**テーブルのプロパティ** ウィンドウでバッキング テーブルが **Create Rec Id Index = Yes** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-133">Before you complete the following steps, verify that the backing table has **Create Rec Id Index = Yes** in the **Table Properties** pane.</span></span> <span data-ttu-id="dc79d-134">または、テーブルに一意のインデックスがあり、RECID がそのインデックスの最初のセグメントであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dc79d-134">Alternatively, ensure that the table has a unique index and RECID is the first segment of that index.</span></span>

1.  <span data-ttu-id="dc79d-135">プロジェクトで**追加** > **新しい項目**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-135">In your project, click **Add** > **New Item**.</span></span> <span data-ttu-id="dc79d-136">**表示** を選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-136">Select **View** and then click **Add**.</span></span>
1.  <span data-ttu-id="dc79d-137">**表示** を右クリックし、**名前の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-137">Right-click **View** and select **Rename**.</span></span> <span data-ttu-id="dc79d-138">**DimAttribute**[BackingTableName] ビューに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-138">Name the view **DimAttribute**[BackingTableName].</span></span> <span data-ttu-id="dc79d-139">たとえば、DimAttributeCustTable。</span><span class="sxs-lookup"><span data-stu-id="dc79d-139">For example, DimAttributeCustTable.</span></span>
1.  <span data-ttu-id="dc79d-140">**メタデータの表示**を展開し、テーブルを画面上の**データ ソース**ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-140">Expand **View Metadata**, and then drag your table to the **Data Sources** node on the view.</span></span>
1.  <span data-ttu-id="dc79d-141">ノードの名前を **BackingTableName** から **BackingEntity** に変更します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-141">Rename the node from **BackingTableName** to **BackingEntity**.</span></span>
1.  <span data-ttu-id="dc79d-142">財務分析コードとして使用するテーブルのキー、値、および名前を識別します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-142">Identify the key, value, and name for the table that you want to use as a financial dimension.</span></span> <span data-ttu-id="dc79d-143">フィールドを検索して、BackingEntity データ ソースの一覧にドラッグし、またはデータ ソース上のフィールドにコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-143">Find the fields and drag to the BackingEntity data source list, or copy and paste the fields on the data source.</span></span> <span data-ttu-id="dc79d-144">3 つのフィールドの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-144">Rename the three fields to:</span></span>
      + <span data-ttu-id="dc79d-145">**キー** – これは代理キーで、通常は RecID です。</span><span class="sxs-lookup"><span data-stu-id="dc79d-145">**Key** – This is the surrogate key, typically the RecID.</span></span>
      + <span data-ttu-id="dc79d-146">**値** - これは、AccountNum のようなナチュラル キーです。</span><span class="sxs-lookup"><span data-stu-id="dc79d-146">**Value** - This is the natural key, for example the AccountNum.</span></span> <span data-ttu-id="dc79d-147">最大 30 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="dc79d-147">It is a string up to 30 characters.</span></span>
      + <span data-ttu-id="dc79d-148">**名前** – これは説明で、通常は**名前**または**説明**フィールドです。</span><span class="sxs-lookup"><span data-stu-id="dc79d-148">**Name** – This is the description, which is typically the **Name** or **Description** field.</span></span> <span data-ttu-id="dc79d-149">最大 60 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="dc79d-149">It is a string up to 60 characters.</span></span>
1.  <span data-ttu-id="dc79d-150">バッキング テーブルがデータを削除する場合、ビューで **範囲** を作成することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-150">You may need to create a **Range** on the view if the backing table removes data.</span></span> <span data-ttu-id="dc79d-151">たとえば、作業単位を使用し部門のみを必要とする場合、その作業単位の範囲を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-151">For example, if you are using an Operating unit and only want Department, you will want to use the range for that operating unit.</span></span>
1.  <span data-ttu-id="dc79d-152">**新しいインデックス** を右クリックし、**新しいインデックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-152">Right-click **Indexes** and select **New Index**.</span></span> <span data-ttu-id="dc79d-153">**プロパティ** ウィンドウでデータ フィールドとして **値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-153">Select **Value** as the Data field on the **Properties** pane.</span></span> <span data-ttu-id="dc79d-154">必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **いいえ** にセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-154">You can rename the index if needed, however you need to set **Allow Duplicates** to **No**.</span></span>
1. <span data-ttu-id="dc79d-155">**新しいインデックス** を右クリックし、**新しいインデックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-155">Right-click **Indexes** and select **New Index**.</span></span> <span data-ttu-id="dc79d-156">**プロパティ** ウィンドウでデータ フィールドとして **名前** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-156">Select **Name** as the Data field on the **Properties** pane.</span></span> <span data-ttu-id="dc79d-157">必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **はい** にセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-157">You can rename the index if needed, however you need to set **Allow Duplicates** to **Yes**.</span></span>
1. <span data-ttu-id="dc79d-158">**表示**をクリックし、**プロパティ** ウィンドウで、選択した参照ラベル ID に **単数形ラベル** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-158">Click **View**, and in the **Properties** pane, set the **Singular label** field to the reference label ID of your choice.</span></span> <span data-ttu-id="dc79d-159">これは、顧客などの単一の値を示すラベルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-159">This should be the label that indicates a single value, such as Customer.</span></span>
1. <span data-ttu-id="dc79d-160">**ラベル** フィールドを選択した参照ラベル ID に設定します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-160">Set the **Label** field to the reference label ID of your choice.</span></span> <span data-ttu-id="dc79d-161">これは、顧客などの複数の値を示すラベルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-161">This should be the label that indicates multiple values, such as Customers.</span></span> <span data-ttu-id="dc79d-162">この値は、**財務分析コード** ページの **値の使用元** フィールドのドロップダウン リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-162">This value will show in the drop-down list in the **Use Values from** field on the **Financial dimensions** page.</span></span>
1. <span data-ttu-id="dc79d-163">**プロパティ**ウィンドウの **TitleField1** フィールドに、**値**を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-163">Enter **Value** in the **TitleField1** field in the **Properties** pane.</span></span>
1. <span data-ttu-id="dc79d-164">**プロパティ**ウィンドウの **TitleField2** フィールドに、**名前**を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-164">Enter **Name** in the **TitleField2** field in the **Properties** pane.</span></span>
1. <span data-ttu-id="dc79d-165">バッキング テーブルのプロパティを確認し、使用している config キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-165">Review the backing table properties and identify the config key it is using.</span></span> <span data-ttu-id="dc79d-166">**表示**で、バッキング テーブルと同じ**コンフィギュレーション キー**を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-166">On **View**, enter the same **Configuration key** as the backing table.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="dc79d-167">管理者以外のユーザーに、新しいビューのセキュリティ アクセス権を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-167">Security access must be granted to non-admin users for the new view.</span></span>
  > - <span data-ttu-id="dc79d-168">オーバーレイが使用されるリリース 7.2 およびそれ以前では、**DimensionEssentials** を検索し、プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-168">For releases 7.2 and earlier where over-layering is used - Search for **DimensionEssentials** and add it to the Project.</span></span> <span data-ttu-id="dc79d-169">**DimensionEssentials** を展開し、**アクセス許可**を右クリックし、その後**新しいアクセス許可**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-169">Expand **DimensionEssentials**, right-click **Permissions**, and then select **New Permission**.</span></span> <span data-ttu-id="dc79d-170">**プロパティ** ウィンドウで、**アクセス レベル**を**読み取り**に設定します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-170">In the **Properties** pane, set the **Access Level** to **Read**.</span></span> <span data-ttu-id="dc79d-171">**セキュリティ権限**をクリックし、**読み取り**の**アクセス レベル**を**アクセス許可**ノードの下に追加します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-171">Click **Security Privilege** and add the view under the **Permissions** node with an **Access Level** of **Read**.</span></span> <span data-ttu-id="dc79d-172">これらの 1 つを使用しているモデルに拡張することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-172">You may need to extend one of these into the model that you're using.</span></span>
  > - <span data-ttu-id="dc79d-173">拡張機能が使用されているリリース 7.3 以降では、新しいビューと共にカスタム モデルで新しいセキュリティ権限を作成します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-173">For releases 7.3 and later where extensions are used - Create a new Security Privilege in your custom model alongside the new view.</span></span> <span data-ttu-id="dc79d-174">**アクセス許可** ノードを右クリックし、**新しいアクセス許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-174">Right-click the **Permissions** node, and choose **New Permission**.</span></span> <span data-ttu-id="dc79d-175">上記の手順 2 で作成した新しい DimAttribute[DimensionName] ビューの名前を入力し、**アクセス レベル** を**読み取り**に設定します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-175">Enter the name of new DimAttribute[DimensionName] view created above in step 2 and set the **Access Level** to **Read**.</span></span> <span data-ttu-id="dc79d-176">**セキュリティ職務権限 SysServerAXBasicMaintain** を検索します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-176">Search for **Security Duty SysServerAXBasicMaintain**.</span></span> <span data-ttu-id="dc79d-177">右クリックし、**拡張機能の作成** を作成します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-177">Right-click and choose **Create extension**.</span></span> <span data-ttu-id="dc79d-178">必要に応じて拡張機能の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-178">Rename the extension as appropriate.</span></span> <span data-ttu-id="dc79d-179">新たに作成された **セキュリティ特権** を **特権リスト** にドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-179">Drag-and-drop the newly created **Security Privilege** into the **Privileges list**.</span></span>  
       
14. <span data-ttu-id="dc79d-180">**表示** を右クリックし、**コードの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-180">Right-click **View** and select **View Code**.</span></span> <span data-ttu-id="dc79d-181">ビューに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-181">Add the following code to the view.</span></span> <span data-ttu-id="dc79d-182">これにより、分析コード フレームワークに登録されます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-182">This will register it in the dimension framework.</span></span> <span data-ttu-id="dc79d-183">CustTable に対して作成されたビューを使用する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-183">Here is an example using the view created for CustTable.</span></span>
      ```
      [SubscribesTo(classstr(DimensionEnabledType),
      delegatestr(DimensionEnabledType,
      registerDimensionEnabledTypeIdentifiersDelegate))]

      public static void registerDimensionEnabledTypeIdentifier(DimensionIEnabledType _dimensionEnabledType)
      {
         _dimensionEnabledType.registerViewIdentifier(tablestr(DimAttribute**CustTable**));
      }
      ```
15. <span data-ttu-id="dc79d-184">**Microsoft Dynamics 365** を選択し、**オプション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-184">Select **Microsoft Dynamics 365** and click **Options**.</span></span> <span data-ttu-id="dc79d-185">**ベスト プラクティス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-185">Select **Best Practices**.</span></span> <span data-ttu-id="dc79d-186">モデルを選択し、**Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker** が表示されるまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="dc79d-186">Select your model and then scroll until you find **Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker**.</span></span> <span data-ttu-id="dc79d-187">ルールとその子が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-187">Verify that the rule and its children are selected.</span></span>
16.  <span data-ttu-id="dc79d-188">ビューをビルドしてから同期します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-188">Build and then synchronize the view.</span></span>

## <a name="step-2-validate-that-the-view-returns-the-correct-data-in-sql"></a><span data-ttu-id="dc79d-189">手順 2: ビューが SQL で正しいデータを返すことを検証する</span><span class="sxs-lookup"><span data-stu-id="dc79d-189">Step 2: Validate that the view returns the correct data in SQL</span></span>

<span data-ttu-id="dc79d-190">この時点で SQL Server Management Studio で次のクエリを実行して、正しいデータが引き出されているかを確認をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-190">At this point you should be able to run the following query in SQL Server Management Studio to ensure that it's pulling the correct data.</span></span> <span data-ttu-id="dc79d-191">CustTable に対して作成されたビューを使用する省略例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-191">Here is an abbreviated example using the view created for CustTable.</span></span>

      select * from DIMATTRIBUTECUSTTABLE
    

| <span data-ttu-id="dc79d-192">KEY_</span><span class="sxs-lookup"><span data-stu-id="dc79d-192">KEY_</span></span>   | <span data-ttu-id="dc79d-193">値</span><span class="sxs-lookup"><span data-stu-id="dc79d-193">VALUE</span></span>    | <span data-ttu-id="dc79d-194">データ範囲 ID</span><span class="sxs-lookup"><span data-stu-id="dc79d-194">DATA AREA ID</span></span> | <span data-ttu-id="dc79d-195">パーティション</span><span class="sxs-lookup"><span data-stu-id="dc79d-195">PARTITION</span></span> | <span data-ttu-id="dc79d-196">RECID</span><span class="sxs-lookup"><span data-stu-id="dc79d-196">RECID</span></span>   | <span data-ttu-id="dc79d-197">氏名</span><span class="sxs-lookup"><span data-stu-id="dc79d-197">NAME</span></span>           | <span data-ttu-id="dc79d-198">パーティション 2</span><span class="sxs-lookup"><span data-stu-id="dc79d-198">PARTITION #2</span></span> |
|-------------|--------------|----------------|---------------|-------------|--------------------|------------------|
| <span data-ttu-id="dc79d-199">22565425322</span><span class="sxs-lookup"><span data-stu-id="dc79d-199">22565425322</span></span> | <span data-ttu-id="dc79d-200">US\_SI\_0129</span><span class="sxs-lookup"><span data-stu-id="dc79d-200">US\_SI\_0129</span></span> | <span data-ttu-id="dc79d-201">ussi</span><span class="sxs-lookup"><span data-stu-id="dc79d-201">ussi</span></span>           | <span data-ttu-id="dc79d-202">5637144576</span><span class="sxs-lookup"><span data-stu-id="dc79d-202">5637144576</span></span>    | <span data-ttu-id="dc79d-203">22565425322</span><span class="sxs-lookup"><span data-stu-id="dc79d-203">22565425322</span></span> | <span data-ttu-id="dc79d-204">Adventure Services</span><span class="sxs-lookup"><span data-stu-id="dc79d-204">Adventure Services</span></span> | <span data-ttu-id="dc79d-205">5637144576</span><span class="sxs-lookup"><span data-stu-id="dc79d-205">5637144576</span></span>       |
| <span data-ttu-id="dc79d-206">22565424579</span><span class="sxs-lookup"><span data-stu-id="dc79d-206">22565424579</span></span> | <span data-ttu-id="dc79d-207">US\_SI\_0128</span><span class="sxs-lookup"><span data-stu-id="dc79d-207">US\_SI\_0128</span></span> | <span data-ttu-id="dc79d-208">ussi</span><span class="sxs-lookup"><span data-stu-id="dc79d-208">ussi</span></span>           | <span data-ttu-id="dc79d-209">5637144576</span><span class="sxs-lookup"><span data-stu-id="dc79d-209">5637144576</span></span>    | <span data-ttu-id="dc79d-210">22565424579</span><span class="sxs-lookup"><span data-stu-id="dc79d-210">22565424579</span></span> | <span data-ttu-id="dc79d-211">アルペン エレクトロニクス</span><span class="sxs-lookup"><span data-stu-id="dc79d-211">Alpine Electronics</span></span> | <span data-ttu-id="dc79d-212">5637144576</span><span class="sxs-lookup"><span data-stu-id="dc79d-212">5637144576</span></span>       |


## <a name="step-3-override-methods-on-the-backing-table"></a><span data-ttu-id="dc79d-213">手順 3: バッキング テーブルでメソッドを上書きする</span><span class="sxs-lookup"><span data-stu-id="dc79d-213">Step 3: Override methods on the backing table</span></span>

<span data-ttu-id="dc79d-214">バッキング テーブルのナチュラル キーを削除または名前を変更するときに分析コード フレームワークと統合するには、バッキング テーブルの delete メソッドと、update または renamePrimaryKey メソッドにカスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-214">To integrate with the dimensions framework when deleting or renaming the natural key of the backing table, you must write custom code on the backing table's delete method, and on either the update or renamePrimaryKey method.</span></span> <span data-ttu-id="dc79d-215">テーブルがナチュラル キーの更新をブロックする場合、renamePrimaryKey のオーバーライドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-215">If your table blocks updates of the natural key, you will need to use the renamePrimaryKey override.</span></span> <span data-ttu-id="dc79d-216">存在しない場合は、更新メソッドでコードを格納できます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-216">If it does not, then you can put the code in the update method.</span></span> <span data-ttu-id="dc79d-217">CustTable からの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-217">Here is an example from CustTable.</span></span>

```
public void delete()
{
    if (!DimensionValidation::canDeleteEntityValue(this))
    {
        throw error(strFmt("@SYS134392", this.AccountNum));
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

## <a name="step-4-clear-caches-to-force-detection-of-the-new-view"></a><span data-ttu-id="dc79d-218">手順 4: キャッシュをクリアして新しいビューの検出を強制的する</span><span class="sxs-lookup"><span data-stu-id="dc79d-218">Step 4: Clear caches to force detection of the new view</span></span>

<span data-ttu-id="dc79d-219">分析コードとして消費できるエンティティのリストはサーバー上でキャッシュされるため、キャッシュをクリアする呼び出しが実行されるか、クライアントとサーバーの両方が再起動されるまで新しいエンティティの作成は既存のエンティティのリストに表示されません。</span><span class="sxs-lookup"><span data-stu-id="dc79d-219">Because the list of entities that can be consumed as a dimension are cached on the server, the creation of a new entity will not appear in the list of existing entities until a call to clear the caches is performed, or until both the client and the server are restarted.</span></span> <span data-ttu-id="dc79d-220">キャッシュをクリアして新しいビューをすぐに表示させるには、実行可能なクラス内で次のコード行を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc79d-220">To clear the caches and have the new view appear immediately, you must execute the following line of code within a runnable class.</span></span>

      DimensionCache::clearAllScopes();

## <a name="step-5-verify-that-the-dimension-appears-in-the-use-value-from-lookup"></a><span data-ttu-id="dc79d-221">手順 5: 分析コードが [ルックアップからの値を使用] に表示されることを確認する</span><span class="sxs-lookup"><span data-stu-id="dc79d-221">Step 5: Verify that the dimension appears in the Use Value From lookup</span></span>

<span data-ttu-id="dc79d-222">手順を完了したら、総勘定元帳の**財務分析コード** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-222">Now that you have completed the steps, navigate to the **Financial dimensions** page in the General ledger.</span></span> <span data-ttu-id="dc79d-223">**値の使用元**フィールドのドロップダウン メニューをクリックし、値が使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-223">Click the drop-down menu on the **Use Values from** field and verify that your value is available.</span></span>


## <a name="add-a-new-omoperatingunit-type-backed-entity"></a><span data-ttu-id="dc79d-224">新しい OMOperatingUnit タイプがサポートしているエンティティの追加</span><span class="sxs-lookup"><span data-stu-id="dc79d-224">Add a new OMOperatingUnit type backed entity</span></span>

<span data-ttu-id="dc79d-225">新しい組織モデル OMOperatingUnitType 列挙が追加された場合、次元として使用可能にする手順は類似していますが、次のように短くすることができます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-225">If a new Organization Model OMOperatingUnitType enumeration is added, the steps to make it consumable as a dimension are similar but can be made shorter as follows:</span></span>

1. <span data-ttu-id="dc79d-226">既存の DimAttributeOM[BackingTableName] ビューの 1 つをコピーし、適切に名前を変更して、関連するすべてのラベルとヘルプ テキストを調整します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-226">Copy one of the existing DimAttributeOM[BackingTableName] views, rename it appropriately, and then adjust all associated labels and help text.</span></span>
1. <span data-ttu-id="dc79d-227">コピーしたビューで、Datasource\BackingEntity (OMOperatingUnit) \Ranges ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-227">Expand the Datasource\BackingEntity (OMOperatingUnit)\Ranges node on the copied view.</span></span> <span data-ttu-id="dc79d-228">範囲内の値プロパティを、追加された新しい OMOperatingUnitType 列挙型に変更します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-228">Change the value property on the range to the new OMOperatingUnitType enumeration value that was just added.</span></span>
1. <span data-ttu-id="dc79d-229">プロジェクトをビルドして同期します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-229">Build and synchronize the project.</span></span>
1. <span data-ttu-id="dc79d-230">SQL でデータを検証するステップ２で始まるこのトピックの手順に従い、**値の使用**ルックアップで表示される分析コードを検証するステップ 5 まで続けます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-230">Follow the steps in this topic starting with Step 2, where you validate the data in SQL, and then continue through Step 5, where you validate that the dimension appears in the **Use Value From** lookup.</span></span>

<span data-ttu-id="dc79d-231">**OMOperatingUnitType** は **OMOperatingUnit** テーブルによってサポートされているため、削除、更新および **renamePrimaryKey** メソッドを処理するための汎用コードがすでに存在します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-231">Because the **OMOperatingUnitType** is backed by the **OMOperatingUnit** table, generic code already exists to handle the delete, update, and **renamePrimaryKey** methods.</span></span> <span data-ttu-id="dc79d-232">したがって、これらのメソッドを更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="dc79d-232">Therefore, you do not need to update these methods.</span></span>

## <a name="step-6-setting-a-dimension-to-be-self-referenced"></a><span data-ttu-id="dc79d-233">手順 6: 自己参照される分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="dc79d-233">Step 6: Setting a dimension to be self-referenced</span></span> 

<span data-ttu-id="dc79d-234">新しいエンティティのデータ エンティティも作成し、そのエンティティが既定の分析コードへの参照を持っている場合、persistEntity() メソッドにこのコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="dc79d-234">If you also want to create an data entity for your new entity, and that entity has a reference to default dimensions, add this code to the persistEntity() method.</span></span>

```
if (_entityCtx.getDatabaseOperation() == DataEntityDatabaseOperation::Insert)
{
     this.<Your entity ‘private’ RecId Dimension field> = DimensionDefaultResolver::checkAndCreateSelfReference(tablenum(<Your backing table>), this.<Your entity Key field>, this.<Your entity ‘public’ DisplayValue field>);
}
                                                                                                
e.g.

public void persistEntity(DataEntityRuntimeContext _entityCtx)
{
     if (_entityCtx.getDatabaseOperation() == DataEntityDatabaseOperation::Insert)
     {
          this.DefaultDimension = DimensionDefaultResolver::checkAndCreateSelfReference(tablenum(BankAccountTable), this.BankAccountId, this.DefaultDimensionDisplayValue);
     }

     super(_entityCtx);
}
```
> [!NOTE]
> <span data-ttu-id="dc79d-235">これにより、分析コードが自身を既定の既定値として使用するようにする場合、情報が正しい順序で作成されます。</span><span class="sxs-lookup"><span data-stu-id="dc79d-235">This ensures that if you also want the dimension to use itself as a default dimension value, the information is created in the correct sequence.</span></span>
