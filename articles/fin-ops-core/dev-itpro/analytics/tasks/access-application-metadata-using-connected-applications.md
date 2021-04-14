---
title: 接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする
description: このトピックの手順では、Regulatory Configuration Service のユーザーが、メタデータを使用して、新しい電子申告モデル マッピングをデザインする方法について説明します。
author: NickSelin
ms.date: 06/29/2019
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
ms.openlocfilehash: 0b113f0db1d44dc5fbda30e10d62ff939550f299
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748696"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="0c1e9-103">接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="0c1e9-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c1e9-104">次の手順では、システム管理者または電子申告開発者ロールの Regulatory configuration service (RCS) ユーザーが、Finance and Operations アプリケーションのメタデータを使用して、電子申告 (ER) モデルのマッピングをデザインする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="0c1e9-105">アプリケーションのメタデータは、RCS 接続されたアプリケーションを使用してオンラインでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="0c1e9-106">サンプル ER モデルマッピングは、対外貿易トランザクションにアクセスするようにコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="0c1e9-107">これらの手順を完了するには、まず、RCS で [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="0c1e9-108">トピック [ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする](access-application-metadata-er-configuration.md)の手順を完了していない場合は、[電子申告例のページ](https://go.microsoft.com/fwlink/?linkid=862266)に移動し、次の ER コンフィギュレーションをダウンロードして保存します。対外貿易メタデータ .xml、対外貿易モデル .xml、対外貿易マッピング .xml。その後、手順のステップを完了してください。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0c1e9-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="0c1e9-109">Prerequisites</span></span>
1. <span data-ttu-id="0c1e9-110">**すべてのワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="0c1e9-111">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="0c1e9-112">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="0c1e9-113">必要な ER コンフィギュレーションの取得</span><span class="sxs-lookup"><span data-stu-id="0c1e9-113">Get required ER configurations</span></span>
1. <span data-ttu-id="0c1e9-114">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="0c1e9-115">[ER コンフィギュレーションを使用したアプリケーション メタデータへのアクセス](access-application-metadata-er-configuration.md)手順のステップを既に完了している場合、現在の RCS インスタンスで必要なすべての ER コンフィギュレーション (対外貿易メタデータ、モデルおよびマッピングのコンフィギュレーション) は、既に存在しています。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="0c1e9-116">この下位タスクの残りのすべての手順はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="0c1e9-117">**交換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="0c1e9-118">**XML ファイルから読み込む** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="0c1e9-119">**参照** をクリックし、**対外貿易メタデータ .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="0c1e9-120">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-120">Click **OK**.</span></span> 
7. <span data-ttu-id="0c1e9-121">**交換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="0c1e9-122">**XML ファイルから読み込む** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="0c1e9-123">**参照** をクリックし、**対外貿易モデル .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="0c1e9-124">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-124">Click **OK**.</span></span> 
11. <span data-ttu-id="0c1e9-125">**交換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="0c1e9-126">**XML ファイルから読み込む** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="0c1e9-127">**参照** をクリックし、**対外貿易マッピング .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="0c1e9-128">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="0c1e9-129">接続されたアプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="0c1e9-129">Register a connected application</span></span>
1. <span data-ttu-id="0c1e9-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-130">Close the page.</span></span> 
2. <span data-ttu-id="0c1e9-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-131">Close the page.</span></span> 
3. <span data-ttu-id="0c1e9-132">**すべてのワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="0c1e9-133">**接続アプリケーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="0c1e9-134">コンフィギュレーションされたアプリケーションが Azure に基づいており、現在の RCS ユーザーがアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="0c1e9-135">また、現在の RCS ユーザーが、選択されたアプリケーションにアクセスでき、アプリケーションのメタデータにアクセスする権限を与える役割を果たすこのアプリケーションのユーザーとして登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="0c1e9-136">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-136">Click **New**.</span></span> 
7. <span data-ttu-id="0c1e9-137">**名前** フィールドに、MyConnectedApp と入力します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="0c1e9-138">**アプリケーション** フィールドに、https:// mycompany.operations.dynamics.com と入力します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="0c1e9-139">**テナント** フィールドに、'mycompany.onmicrosoft.com' と入力します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="0c1e9-140">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-140">Click **Save**.</span></span> 
11. <span data-ttu-id="0c1e9-141">コンフィギュレーションされているアプリケーションへの接続を確認するときは、**リモート アプリケーションへの接続** ページで、**ここをクリックして、選択したリモート アプリケーションに接続する** のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="0c1e9-142">**接続を確認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="0c1e9-143">**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-143">Click **Close**.</span></span> 
14. <span data-ttu-id="0c1e9-144">接続検証に成功すると、現在のグリッドでコンフィギュレーションされているアプリケーションのバージョンとテナントの詳細が更新されます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="0c1e9-145">既存のモデル マッピング コンフィギュレーションを確認する</span><span class="sxs-lookup"><span data-stu-id="0c1e9-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="0c1e9-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-146">Close the page.</span></span> 
2. <span data-ttu-id="0c1e9-147">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="0c1e9-148">ツリーで、**対外貿易モデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="0c1e9-149">ツリーで、**対外貿易モデル\対外貿易マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="0c1e9-150">**前提条件** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0c1e9-151">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0c1e9-152">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="0c1e9-153">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="0c1e9-154">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="0c1e9-155">ツリーで、**Dynamics 365 for Operations\ テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="0c1e9-156">**ルートの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="0c1e9-157">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0c1e9-158">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0c1e9-159">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="0c1e9-160">**キャンセル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="0c1e9-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-161">Close the page.</span></span> 
13. <span data-ttu-id="0c1e9-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="0c1e9-163">接続しているアプリケーションをモデルマッピングに割り当てる</span><span class="sxs-lookup"><span data-stu-id="0c1e9-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="0c1e9-164">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="0c1e9-165">**MyConnectedApp** アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0c1e9-166">現在、このマッピングは、選択した接続アプリケーションのメタデータを参照します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="0c1e9-167">同じマッピングがメタデータ コンフィギュレーションと接続されたアプリケーションを同時に参照する場合、接続されているアプリケーションのメタデータが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="0c1e9-168">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="0c1e9-169">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="0c1e9-170">ツリーで、**Dynamics 365 for Operations\ テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="0c1e9-171">**ルートの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="0c1e9-172">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0c1e9-173">このマッピングは、割り当てられた接続アプリケーションのすべてのメタデータを使用するため、2 つ以上のアプリケーション テーブルが提供されました。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="0c1e9-174">**キャンセル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="0c1e9-175">**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0c1e9-176">このマッピングに割り当てられた接続アプリケーションのメタデータの詳細を使用して、説明されているデータ ソース項目でデータ モデルの要素が正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="0c1e9-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-177">Close the page.</span></span> 
11. <span data-ttu-id="0c1e9-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-178">Close the page.</span></span> 

<span data-ttu-id="0c1e9-179">異なるバージョンのアプリケーションのメタデータを使用してこのモデル マッピングを評価する必要がある場合は、接続されている別のアプリケーションを登録してこのモデル マッピングに割り当て、新しいメタデータに対してそれを検証します。</span><span class="sxs-lookup"><span data-stu-id="0c1e9-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]