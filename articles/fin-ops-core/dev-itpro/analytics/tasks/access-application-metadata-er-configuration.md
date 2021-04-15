---
title: ER コンフィギュレーションを使用したアプリケーション メタデータへのアクセス
description: このトピックでは、Regulatory Configuration Service のユーザーが、メタデータを使用して、新しい電子申告モデル マッピングをデザインする方法について説明します。
author: NickSelin
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 261c208b5906e313293d837dda20b2fe6dd649d6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749342"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="ab9d5-103">ER コンフィギュレーションを使用したアプリケーション メタデータへのアクセス</span><span class="sxs-lookup"><span data-stu-id="ab9d5-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab9d5-104">次の手順では、システム管理者または電子申告開発者ロールの Regulatory configuration service (RCS) ユーザーが、 アプリケーションのメタデータを使用して、電子申告 (ER) モデルのマッピングをデザインする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="ab9d5-105">アプリケーション メタデータには、対外貿易トランザクションにアクセスするためのサンプル メタデータ セットを含む ER メタデータ コンフィギュレーションを使用してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="ab9d5-106">これらの手順を完了するには、RCS で最初に[コンフィギュレーション プロバイダーを作成して有効とマークする](er-configuration-provider-mark-it-active-2016-11.md)のトピックにある手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="ab9d5-107">次に、トピック [RCS で使用するアプリケーション メタデータの準備](prepare-application-metadata-rcs.md)の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab9d5-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="ab9d5-108">Prerequisites</span></span>
1. <span data-ttu-id="ab9d5-109">**すべてのワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ab9d5-110">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ab9d5-111">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="ab9d5-112">メタデータ コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="ab9d5-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="ab9d5-113">**メタデータ コンフィギュレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="ab9d5-114">メタデータを含む ER メタデータ コンフィギュレーションをインポートします。これは対外貿易ビジネスのための電子ドキュメントを生成するようコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="ab9d5-115">この ER メタデータ コンフィギュレーションは、[RCS で使用されるアプリケーション メタデータを準備する](prepare-application-metadata-rcs.md) の手順が完了した時に、XML ファイルとしてエクスポートされました。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="ab9d5-116">**交換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="ab9d5-117">**XML ファイルから読み込む** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="ab9d5-118">**参照** をクリックし、'対外貿易 metadata.xml' ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="ab9d5-119">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-119">Click **OK**.</span></span> 
7. <span data-ttu-id="ab9d5-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="ab9d5-121">データ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="ab9d5-121">Create data model configuration</span></span>
1. <span data-ttu-id="ab9d5-122">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="ab9d5-123">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="ab9d5-124">**名前** フィールドに、「対外貿易モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="ab9d5-125">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="ab9d5-126">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="ab9d5-127">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="ab9d5-128">**名称** のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="ab9d5-129">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-129">Click **Add**.</span></span> 
9. <span data-ttu-id="ab9d5-130">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="ab9d5-131">**名前** フィールドに、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="ab9d5-132">**品目タイプ** フィールドで、**レコード リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="ab9d5-133">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="ab9d5-134">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="ab9d5-135">**名前** フィールドに、「コモディティ コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="ab9d5-136">**品目タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="ab9d5-137">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="ab9d5-138">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="ab9d5-139">**名前** フィールドに、「請求金額」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="ab9d5-140">**品目タイプ** フィールドで、**実数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="ab9d5-141">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="ab9d5-142">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="ab9d5-143">**名前** フィールドに、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="ab9d5-144">**品目タイプ** フィールドで、**日付** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="ab9d5-145">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="ab9d5-146">**ルート参照** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="ab9d5-147">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="ab9d5-148">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="ab9d5-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-149">Close the page.</span></span> 
29.    <span data-ttu-id="ab9d5-150">**状態の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="ab9d5-151">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="ab9d5-152">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="ab9d5-153">モデル マッピング コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="ab9d5-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="ab9d5-154">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="ab9d5-155">**新規** フィールドに、「データ モデル対外貿易モデルに基づいたモデル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="ab9d5-156">**名前** フィールドに、「対外貿易マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="ab9d5-157">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="ab9d5-158">**前提条件** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="ab9d5-159">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="ab9d5-160">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-160">Click **New**.</span></span> 
8. <span data-ttu-id="ab9d5-161">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="ab9d5-162">**必要条件のコンポーネント タイプ** フィールドで、**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="ab9d5-163">**対外貿易メタデータ** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="ab9d5-164">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="ab9d5-165">'対外貿易メタデータ' コンフィギュレーションのバージョン 1 への参照を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="ab9d5-166">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="ab9d5-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-167">Close the page.</span></span> 
14.    <span data-ttu-id="ab9d5-168">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="ab9d5-169">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="ab9d5-170">ツリーで、**Dynamics 365 for Operations\ テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="ab9d5-171">**ルートの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="ab9d5-172">**名前** フィールドに、「イントラスタット」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="ab9d5-173">**イントラスタット** テーブル レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="ab9d5-174">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab9d5-175">現在使用されているメタデータ セットに追加されたテーブルは 2 つだけなので、2 つのテーブルのみが提供されています。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="ab9d5-176">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="ab9d5-177">ツリーで、**イントラスタット** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="ab9d5-178">ツリーで、**イントラスタット \AmountMST** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="ab9d5-179">ツリーで、**トランザクション = イントラスタット** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="ab9d5-180">ツリーで、**トランザクション = イントラスタット \Invoiced amount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="ab9d5-181">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="ab9d5-182">ツリーで、**イントラスタット \TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="ab9d5-183">ツリーで、**トランザクション = イントラスタット \Date** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="ab9d5-184">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="ab9d5-185">ツリーで、**イントラスタット\>リレーション** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="ab9d5-186">ツリーで、**イントラスタット\>リレーション\イントラスタットコモディティ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="ab9d5-187">ツリーで、**イントラスタット\>リレーション\イントラスタットコモディティ\コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="ab9d5-188">ツリーで、**トランザクション = イントラスタット\コモディティ コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="ab9d5-189">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="ab9d5-190">**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab9d5-191">参照された ER メタデータ コンフィギュレーションのアプリケーション メタデータの詳細を使用して説明されているデータ ソース項目によって、データ モデルの要素が正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="ab9d5-192">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="ab9d5-193">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-193">Close the page.</span></span> 
38.    <span data-ttu-id="ab9d5-194">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-194">Close the page.</span></span> 
39.    <span data-ttu-id="ab9d5-195">必要に応じて、既存のメタデータセットを拡張し、ER メタデータコンフィギュレーションの新しい完成したバージョンをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="ab9d5-196">その後、それを RCS にインポートし、インポートしたメタデータ コンフィギュレーションの新しいバージョンを参照するように構成されたモデル マッピング コンフィギュレーションの前提条件を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab9d5-197">アプリケーション メタデータに関する情報を取得するこの方法は、ローカルに展開されたアプリケーションで利用できる唯一の方法です (ローカル ビジネス データ (LBD)、またはオンプレミスの場合、配置モデルが使用されます)。</span><span class="sxs-lookup"><span data-stu-id="ab9d5-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]