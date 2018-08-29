---
title: "Dynamics AX インスタンス間でのデータのコピー"
description: "このトピックでは、データ インポート/エクスポート フレームワーク (DIXF) を使用して Dynamics AX インスタンス間でデータをコピーする方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 20251
ms.assetid: f608a318-106e-4edb-8a6f-c7a753a27640
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 680ebdaec7e624ca5da9cef5f444b0fa1da52e5e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="copy-data-between-dynamics-ax-instances"></a><span data-ttu-id="b2dc7-103">Dynamics AX インスタンス間でのデータのコピー</span><span class="sxs-lookup"><span data-stu-id="b2dc7-103">Copy data between Dynamics AX instances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2dc7-104">このチュートリアルでは、次の作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-104">This walkthrough illustrates the following tasks:</span></span>

-   <span data-ttu-id="b2dc7-105">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="b2dc7-105">Define the format of your source data</span></span>
-   <span data-ttu-id="b2dc7-106">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="b2dc7-106">Define a processing group</span></span>
-   <span data-ttu-id="b2dc7-107">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="b2dc7-107">Process data from source to staging</span></span>
-   <span data-ttu-id="b2dc7-108">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="b2dc7-108">Validate the data in staging</span></span>
-   <span data-ttu-id="b2dc7-109">データをファイルへエクスポート</span><span class="sxs-lookup"><span data-stu-id="b2dc7-109">Export the data to a file</span></span>
-   <span data-ttu-id="b2dc7-110">データのインポート</span><span class="sxs-lookup"><span data-stu-id="b2dc7-110">Import the data</span></span>
-   <span data-ttu-id="b2dc7-111">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="b2dc7-111">Validate the data in target</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2dc7-112">前提条件</span><span class="sxs-lookup"><span data-stu-id="b2dc7-112">Prerequisites</span></span>
<span data-ttu-id="b2dc7-113">このチュートリアルを完了するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-113">To complete this walkthrough you will need:</span></span>

-   <span data-ttu-id="b2dc7-114">Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="b2dc7-114">Microsoft Dynamics AX 2012, Microsoft Dynamics AX 2012 R2, or Microsoft Dynamics AX 2012 R3</span></span>
-   <span data-ttu-id="b2dc7-115">データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b2dc7-115">Data Import/Export Framework</span></span>
-   <span data-ttu-id="b2dc7-116">Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3 のデモ データ</span><span class="sxs-lookup"><span data-stu-id="b2dc7-116">Demo data for Microsoft Dynamics AX 2012, Microsoft Dynamics AX 2012 R2, or Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="b2dc7-117">次の図は、エクスポートおよびインポート処理中にデータが取るパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-117">The following diagram illustrates the path that data takes during the export and import processes.</span></span> <span data-ttu-id="b2dc7-118">[![WalkthroughCopyDataBetweenAXInstances1](./media/walkthroughcopydatabetweenaxinstances1.jpg)](./media/walkthroughcopydatabetweenaxinstances1.jpg)</span><span class="sxs-lookup"><span data-stu-id="b2dc7-118">[![WalkthroughCopyDataBetweenAXInstances1](./media/walkthroughcopydatabetweenaxinstances1.jpg)](./media/walkthroughcopydatabetweenaxinstances1.jpg)</span></span>

## <a name="define-the-format-of-your-source-data"></a><span data-ttu-id="b2dc7-119">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="b2dc7-119">Define the format of your source data</span></span>
1.  <span data-ttu-id="b2dc7-120">**データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-120">Open **Data Import/Export Framework** &gt; **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="b2dc7-121">**新規**をクリックし、名前と説明を入力します。次に、**タイプ** リストから **AX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-121">Click **New**, enter a name and a description, and then select **AX** from the **Type** list.</span></span>

## <a name="define-a-processing-group-to-export-data-from-microsoft-dynamics-ax"></a><span data-ttu-id="b2dc7-122">Microsoft Dynamics AX からデータをエクスポートする処理グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-122">Define a processing group to export data from Microsoft Dynamics AX</span></span>
1.  <span data-ttu-id="b2dc7-123">会社を **CEU** に変更します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-123">Change the company to **CEU**.</span></span>
2.  <span data-ttu-id="b2dc7-124">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-124">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then click **New** to create a new processing group.</span></span>
3.  <span data-ttu-id="b2dc7-125">グループ名を Export-Cust に設定し、説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-125">Set the group name to Export-Cust and add a description.</span></span>
4.  <span data-ttu-id="b2dc7-126">処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-126">Click **Entities** to select the entities to include in the processing group.</span></span>
    1.  <span data-ttu-id="b2dc7-127">**処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、エンティティに対して**顧客**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-127">In the **Select entities for processing group** form, click **New**, and then, for an entity name, select **Customer**.</span></span>
    2.  <span data-ttu-id="b2dc7-128">**ソース データ形式**フィールドで、作成した Microsoft Dynamics AX のソース データ形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-128">In the **Source data format** field, select the Microsoft Dynamics AX source data format that you created.</span></span>
    3.  <span data-ttu-id="b2dc7-129">**選択**ボタンをクリックします。次に **DMFCustomerTargetEntity** フォームの**範囲**タブで、**フィールド**を**作成日時**と選択します。**基準**に &gt; 9/1/2007 と入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-129">Click the **Select** button, and then in the **DMFCustomerTargetEntity** form, on the **Range** tab, for **Field**, choose **Created date and time**, and for **Criteria**, enter &gt; 9/1/2007, and then click **OK**.</span></span>
    4.  <span data-ttu-id="b2dc7-130">**処理グループのエンティティの選択** フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-130">Close the **Select entities for processing group** form.</span></span>

## <a name="process-data-from-source-to-staging"></a><span data-ttu-id="b2dc7-131">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="b2dc7-131">Process data from source to staging</span></span>
1.  <span data-ttu-id="b2dc7-132">**処理グループ** フォームで、作成したエクスポート顧客グループを選択して**ステージング データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-132">In the **Processing group** form, select the Export-Cust group that you created, and click **Get staging data**.</span></span> <span data-ttu-id="b2dc7-133">**ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-133">The **Create a job ID for the staging data job** form opens.</span></span>
2.  <span data-ttu-id="b2dc7-134">既定では、ジョブの ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-134">By default, an ID for the job is generated.</span></span> <span data-ttu-id="b2dc7-135">必要に応じて、ID を変更して説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-135">If needed, you can modify the ID and add a description.</span></span> <span data-ttu-id="b2dc7-136">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-136">Click **OK**.</span></span> <span data-ttu-id="b2dc7-137">**ステージング データ実行** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-137">The **Staging data execution** form opens.</span></span>
3.  <span data-ttu-id="b2dc7-138">**ステージング データ実行**フォームで、**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-138">In the **Staging data execution** form, click **Run**.</span></span> <span data-ttu-id="b2dc7-139">**ソースからステージングにデータを取得** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-139">The **Get data from source to staging** form opens.</span></span>
4.  <span data-ttu-id="b2dc7-140">**ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-140">In the **Get data from source to staging** form, click **OK** to run immediately.</span></span> <span data-ttu-id="b2dc7-141">ソース データはステージング テーブルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-141">The source data is copied to the staging tables.</span></span>

## <a name="validate-the-data-in-staging"></a><span data-ttu-id="b2dc7-142">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="b2dc7-142">Validate the data in staging</span></span>
1.  <span data-ttu-id="b2dc7-143">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-143">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="b2dc7-144">**ステージング データの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-144">Click **View staging data**.</span></span>
3.  <span data-ttu-id="b2dc7-145">ソースと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-145">Review the staging data to validate that it matches the source.</span></span>
4.  <span data-ttu-id="b2dc7-146">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-146">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>

## <a name="export-the-data-to-a-file"></a><span data-ttu-id="b2dc7-147">データをファイルへエクスポート</span><span class="sxs-lookup"><span data-stu-id="b2dc7-147">Export the data to a file</span></span>
1.  <span data-ttu-id="b2dc7-148">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-148">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then select the processing group to work with.</span></span>
2.  <span data-ttu-id="b2dc7-149">**AX にエクスポート**をクリックし、ファイル名を入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-149">Click **Export to AX**, enter a file name, and then click **OK**.</span></span> <span data-ttu-id="b2dc7-150">処理グループによって識別される .dat ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-150">A .dat file of the data identified by the processing group is created.</span></span>

## <a name="import-the-data"></a><span data-ttu-id="b2dc7-151">データのインポート</span><span class="sxs-lookup"><span data-stu-id="b2dc7-151">Import the data</span></span>
1.  <span data-ttu-id="b2dc7-152">データをインポートしたい Microsoft Dynamics AX のインスタンスに接続されているクライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-152">Open a client that is connected to the instance of Microsoft Dynamics AX that you want to import data into.</span></span>
2.  <span data-ttu-id="b2dc7-153">現在の会社がデータのインポート先であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-153">Validate that the current company is the one that you want to import the data into.</span></span>
3.  <span data-ttu-id="b2dc7-154">**システム管理** &gt; **共通** &gt; **データのエクスポート/インポート** &gt; **インポート**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-154">Click **System administration** &gt; **Common** &gt; **Data export/import** &gt; **Import**.</span></span>
4.  <span data-ttu-id="b2dc7-155">**一般**タブで、インポートするデータ ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-155">On the **General** tab, select the data file that you want to import.</span></span>
5.  <span data-ttu-id="b2dc7-156">**バッチ**タブで、インポート ファイルを処理するバッチ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-156">On the **Batch** tab, select the batch group that you want the import file to be processed with.</span></span> <span data-ttu-id="b2dc7-157">すべてのインポート ジョブはバッチ タスクとして実行します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-157">All import jobs are run as batch tasks.</span></span>

## <a name="validate-the-data-in-target"></a><span data-ttu-id="b2dc7-158">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="b2dc7-158">Validate the data in target</span></span>
<span data-ttu-id="b2dc7-159">元のインスタンスからの顧客データが **すべての顧客** フォームに表示されるようになったこと確認します。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-159">Verify that the customer data from the original instance is now displayed in the **All Customers** form.</span></span> <span data-ttu-id="b2dc7-160">**売掛金勘定** &gt; **共通** &gt; **顧客** &gt; **すべての顧客**フォームの順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2dc7-160">Click **Accounts receivable** &gt; **Common** &gt; **Customer** &gt; **All Customers **form.</span></span>




