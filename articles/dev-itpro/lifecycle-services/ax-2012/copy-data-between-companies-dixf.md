---
title: "Dynamics AX 会社間でのデータのコピー"
description: "Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、顧客などのエンティティを 1 つの Microsoft Dynamics AX の法人 (会社) から他にコピーすることができます。 この例では、Contoso データ セットの CEC 会社に CEU 会社の特定の顧客グループ内の顧客グループをエクスポートします。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 17821
ms.assetid: cd9b30d2-d4e0-4da7-9408-34bda5888070
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 58ff855888be0a7b06eae372bb31f2442ef09b03
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="copy-data-between-dynamics-ax-companies"></a><span data-ttu-id="a7404-104">Dynamics AX 会社間でのデータのコピー</span><span class="sxs-lookup"><span data-stu-id="a7404-104">Copy data between Dynamics AX companies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7404-105">Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、顧客などのエンティティを 1 つの Microsoft Dynamics AX の法人 (会社) から他にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="a7404-105">You can use the Microsoft Dynamics AX 2012 Data Import/Export Framework to copy an entity, such as customers, from one Microsoft Dynamics AX legal entity (company) to another.</span></span> <span data-ttu-id="a7404-106">この例では、Contoso データ セットの CEC 会社に CEU 会社の特定の顧客グループ内の顧客グループをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="a7404-106">In this example, we will export customers in a specific customer group from the CEU company to the CEC company in the Contoso data set.</span></span>

<span data-ttu-id="a7404-107">**注:** このチュートリアルは、Microsoft Dynamics AX 2012 R2 または Microsoft Dynamics AX 2012 R3 の累積的な更新プログラム 7 に付属しているデータのインポート/エクスポート フレームワークのバージョンのユーザーを対象としていません。</span><span class="sxs-lookup"><span data-stu-id="a7404-107">**Note: **This walkthrough is not intended for users of the versions of the Data Import/Export Framework that ship with cumulative update 7 for Microsoft Dynamics AX 2012 R2 or Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="a7404-108">これらのユーザーは、トピック [[企業間でのエンティティ データのコピーと比較 (DIXF、DMF)](copy-compare-entity-data-between-companies-dixf.md)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7404-108">Those users should refer to the topic [Copying and comparing entity data between companies (DIXF, DMF)](copy-compare-entity-data-between-companies-dixf.md).</span></span> <span data-ttu-id="a7404-109">このチュートリアルでは、次の作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7404-109">This walkthrough illustrates the following tasks:</span></span>

-   <span data-ttu-id="a7404-110">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="a7404-110">Define the format of your source data</span></span>
-   <span data-ttu-id="a7404-111">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="a7404-111">Define a processing group</span></span>
-   <span data-ttu-id="a7404-112">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="a7404-112">Process data from source to staging</span></span>
-   <span data-ttu-id="a7404-113">会社を切り替えて別の法人にデータをコピー</span><span class="sxs-lookup"><span data-stu-id="a7404-113">Switch companies to copy data to another legal entity</span></span>
-   <span data-ttu-id="a7404-114">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="a7404-114">Validate the data in staging</span></span>
-   <span data-ttu-id="a7404-115">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="a7404-115">Validate the data in target</span></span>

<span data-ttu-id="a7404-116">次の図は、エクスポートおよびインポート処理中にデータが取るパスを示しています。</span><span class="sxs-lookup"><span data-stu-id="a7404-116">The following diagram illustrates the path that data takes during the export and import processes.</span></span> <span data-ttu-id="a7404-117">[![WalkthroughCopyDataBetweenAXCompanies1](./media/walkthroughcopydatabetweenaxcompanies1.jpg)](./media/walkthroughcopydatabetweenaxcompanies1.jpg)</span><span class="sxs-lookup"><span data-stu-id="a7404-117">[![WalkthroughCopyDataBetweenAXCompanies1](./media/walkthroughcopydatabetweenaxcompanies1.jpg)](./media/walkthroughcopydatabetweenaxcompanies1.jpg)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a7404-118">前提条件</span><span class="sxs-lookup"><span data-stu-id="a7404-118">Prerequisites</span></span>
<span data-ttu-id="a7404-119">このチュートリアルを完了するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="a7404-119">To complete this walkthrough you will need:</span></span>

-   <span data-ttu-id="a7404-120">Microsoft Dynamics AX 2012 または Microsoft Dynamics AX 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a7404-120">Microsoft Dynamics AX 2012 or Microsoft Dynamics AX 2012 R2</span></span>
-   <span data-ttu-id="a7404-121">データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="a7404-121">Data Import/Export Framework</span></span>
-   <span data-ttu-id="a7404-122">Microsoft Dynamics AX 2012 または Microsoft Dynamics AX 2012 R2 のデモ データ</span><span class="sxs-lookup"><span data-stu-id="a7404-122">Demo data for Microsoft Dynamics AX 2012 or Microsoft Dynamics AX 2012 R2</span></span>

## <a name="define-the-format-of-your-source-data"></a><span data-ttu-id="a7404-123">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="a7404-123">Define the format of your source data</span></span>
1.  <span data-ttu-id="a7404-124">**データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。</span><span class="sxs-lookup"><span data-stu-id="a7404-124">Open **Data Import/Export Framework** &gt; **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="a7404-125">**新規**をクリックし、名前と説明を入力します。次に、**タイプ** リストから **AX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-125">Click **New**, enter a name and a description, and then select **AX** from the **Type** list.</span></span>

## <a name="define-a-processing-group-to-export-data-from-microsoft-dynamics-ax"></a><span data-ttu-id="a7404-126">Microsoft Dynamics AX からデータをエクスポートする処理グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="a7404-126">Define a processing group to export data from Microsoft Dynamics AX</span></span>
1.  <span data-ttu-id="a7404-127">会社を **CEU** に変更します。</span><span class="sxs-lookup"><span data-stu-id="a7404-127">Change the company to **CEU**.</span></span>
2.  <span data-ttu-id="a7404-128">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7404-128">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then click **New** to create a new processing group.</span></span>
3.  <span data-ttu-id="a7404-129">グループ名を **Export-Cust** に設定し、説明を追加します。</span><span class="sxs-lookup"><span data-stu-id="a7404-129">Set the group name to **Export-Cust** and add a description.</span></span>
4.  <span data-ttu-id="a7404-130">処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-130">Click **Entities** to select the entities to include in the processing group.</span></span>
    1.  <span data-ttu-id="a7404-131">**処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、エンティティに対して**顧客**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-131">In the **Select entities for processing group** form, click **New**, and then, for an entity name, select **Customer**.</span></span>
    2.  <span data-ttu-id="a7404-132">**ソース データ形式**フィールドで、作成した Microsoft Dynamics AX のソース データ形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-132">In the **Source data format** field, select the Microsoft Dynamics AX source data format that you created.</span></span>
    3.  <span data-ttu-id="a7404-133">**選択**をクリックし、**DMFCustomerTargetEntity** フォーム内の**範囲**タブで、**フィールド**の**顧客グループ**、および**基準**の **20** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-133">Click **Select**, and then in the **DMFCustomerTargetEntity** form, on the **Range** tab, for **Field**, select **Customer group**, and for **Criteria**, select **20**, and then click **OK**.</span></span>
    4.  <span data-ttu-id="a7404-134">**処理グループのエンティティの選択** フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a7404-134">Close the **Select entities for processing group** form.</span></span>

## <a name="process-data-from-source-to-staging"></a><span data-ttu-id="a7404-135">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="a7404-135">Process data from source to staging</span></span>
1.  <span data-ttu-id="a7404-136">**処理グループ** フォームで、作成したエクスポート顧客グループを選択して**ステージング データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-136">In the **Processing group** form, select the Export-Cust group that you created, and click **Get staging data**.</span></span> <span data-ttu-id="a7404-137">**ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="a7404-137">The **Create a job ID for the staging data job** form opens.</span></span>
2.  <span data-ttu-id="a7404-138">既定では、ジョブの ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a7404-138">By default, an ID for the job is generated.</span></span> <span data-ttu-id="a7404-139">必要に応じて、ID を変更して説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a7404-139">If needed, you can modify the ID and add a description.</span></span> <span data-ttu-id="a7404-140">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-140">Click **OK**.</span></span> <span data-ttu-id="a7404-141">**ステージング データ実行フォーム**が開きます。</span><span class="sxs-lookup"><span data-stu-id="a7404-141">The **Staging data execution form** opens.</span></span>
3.  <span data-ttu-id="a7404-142">**ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。</span><span class="sxs-lookup"><span data-stu-id="a7404-142">In the **Get data from source to staging** form, click **OK** to run immediately.</span></span> <span data-ttu-id="a7404-143">ソース データはステージング テーブルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a7404-143">The source data is copied to the staging tables.</span></span>

## <a name="validate-the-data-in-staging"></a><span data-ttu-id="a7404-144">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="a7404-144">Validate the data in staging</span></span>
1.  <span data-ttu-id="a7404-145">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-145">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history**, and then select the job that ran.</span></span>
2.  <span data-ttu-id="a7404-146">**ステージング データの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-146">Click **View staging data**.</span></span>
3.  <span data-ttu-id="a7404-147">ソースと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-147">Review the staging data to validate that it matches the source.</span></span>
4.  <span data-ttu-id="a7404-148">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-148">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>

## <a name="switch-companies-to-copy-data-to-another-company"></a><span data-ttu-id="a7404-149">会社を切り替えて別の会社にデータをコピー</span><span class="sxs-lookup"><span data-stu-id="a7404-149">Switch companies to copy data to another company</span></span>
1.  <span data-ttu-id="a7404-150">**CEC** 会社に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a7404-150">Switch to the **CEC** company.</span></span>
2.  <span data-ttu-id="a7404-151">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-151">In **Data Import/Export Framework**, click **Common** &gt; **Processing group**, and then select the processing group to work with.</span></span>
3.  <span data-ttu-id="a7404-152">**データをターゲットにコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-152">Click **Copy data to target**.</span></span> <span data-ttu-id="a7404-153">**実行するジョブ ID を選択** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="a7404-153">The **Select a job ID to run** form opens.</span></span>
4.  <span data-ttu-id="a7404-154">ジョブを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-154">Select a job and click **OK**.</span></span> <span data-ttu-id="a7404-155">**ターゲット データ実行** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="a7404-155">The **Target data execution** form opens.</span></span>
5.  <span data-ttu-id="a7404-156">**実行**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-156">Click **Run**, and then click **OK**.</span></span> <span data-ttu-id="a7404-157">データはターゲット エンティティにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a7404-157">The data is copied to the target entity.</span></span>

## <a name="validate-the-data-in-target"></a><span data-ttu-id="a7404-158">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="a7404-158">Validate the data in target</span></span>
<span data-ttu-id="a7404-159">元の会社からの顧客データが次のいずれかの方法で表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-159">Verify that the customer data from the original company is displayed in either of the following ways:</span></span>

-   <span data-ttu-id="a7404-160">ステージング データの表示:</span><span class="sxs-lookup"><span data-stu-id="a7404-160">View staging data:</span></span>
    1.  <span data-ttu-id="a7404-161">**データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴** &gt; **ステージング データの表示**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7404-161">In **Data Import/Export Framework**, click **Common** &gt; **Processing group** &gt; **Execution history** &gt; **View staging data**, and then select the job that ran.</span></span>
    2.  <span data-ttu-id="a7404-162">ソースと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-162">Review the staging data to validate that it matches the source.</span></span>
    3.  <span data-ttu-id="a7404-163">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-163">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>
-   <span data-ttu-id="a7404-164">CEU 会社からの顧客データが **すべての顧客フォーム** に表示されるようになったこと確認します。</span><span class="sxs-lookup"><span data-stu-id="a7404-164">Verify that the customer data from the CEU company is now displayed in the **All Customers form**.</span></span> <span data-ttu-id="a7404-165">**売掛金勘定** &gt; **共通** &gt; **顧客** &gt; **すべての顧客**フォームの順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7404-165">Click **Accounts receivable** &gt; **Common** &gt; **Customer** &gt; **All Customers **form.</span></span>





