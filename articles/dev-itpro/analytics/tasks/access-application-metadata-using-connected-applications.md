---
title: 接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする
description: このトピックの手順では、Regulatory configuration service (RCS) のユーザーが Finance and Operations のメタデータを使用して、新しい電子申告 (ER) モデルのマッピングをデザインする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d3581f6ae2d91b9648da3ba69e6b1d36cd08196
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727055"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="e8a50-103">接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="e8a50-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8a50-104">次の手順では、システム管理者または電子申告開発者ロールの Regulatory configuration service (RCS) ユーザーが、Dynamics 365 for Finance and Operations アプリケーションのメタデータを使用して、電子申告 (ER) モデルのマッピングをデザインする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e8a50-105">アプリケーションのメタデータは、RCS 接続されたアプリケーションを使用してオンラインでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="e8a50-106">サンプル ER モデルマッピングは、対外貿易トランザクションにアクセスするようにコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="e8a50-107">これらの手順を完了するには、まず RCS でトピックにある手順[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md)を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8a50-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="e8a50-108">トピック [ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする](access-application-metadata-er-configuration.md)の手順を完了していない場合は、[電子申告例のページ](https://go.microsoft.com/fwlink/?linkid=862266)に移動し、次の ER コンフィギュレーションをダウンロードして保存します。対外貿易メタデータ .xml、対外貿易モデル .xml、対外貿易マッピング .xml。その後、手順のステップを完了してください。</span><span class="sxs-lookup"><span data-stu-id="e8a50-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8a50-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="e8a50-109">Prerequisites</span></span>
1. <span data-ttu-id="e8a50-110">**すべてのワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="e8a50-111">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e8a50-112">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md)という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8a50-112">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="e8a50-113">必要な ER コンフィギュレーションの取得</span><span class="sxs-lookup"><span data-stu-id="e8a50-113">Get required ER configurations</span></span>
1. <span data-ttu-id="e8a50-114">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="e8a50-115">[(RCS) ER コンフィギュレーションを使用したアプリケーション メタデータへのアクセス](access-application-metadata-er-configuration.md)手順のステップを既に完了している場合、現在の RCS インスタンスで必要なすべての ER コンフィギュレーション (対外貿易メタデータ、モデルおよびマッピングのコンフィギュレーション) は、既に存在しています。</span><span class="sxs-lookup"><span data-stu-id="e8a50-115">If you already completed the steps in the [(RCS) Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="e8a50-116">この下位タスクの残りのすべての手順はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="e8a50-117">**交換**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="e8a50-118">**XML ファイルから読み込む**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="e8a50-119">**参照**をクリックし、**対外貿易メタデータ .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="e8a50-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="e8a50-120">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-120">Click **OK**.</span></span> 
7. <span data-ttu-id="e8a50-121">**交換**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="e8a50-122">**XML ファイルから読み込む**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="e8a50-123">**参照**をクリックし、**対外貿易モデル .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="e8a50-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="e8a50-124">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-124">Click **OK**.</span></span> 
11. <span data-ttu-id="e8a50-125">**交換**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="e8a50-126">**XML ファイルから読み込む**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="e8a50-127">**参照**をクリックし、**対外貿易マッピング .xml** ファイルを選択する。</span><span class="sxs-lookup"><span data-stu-id="e8a50-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="e8a50-128">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-128">Click **OK**.</span></span> 

## <a name="register-connected-dynamics-365-for-finance-and-operations-application"></a><span data-ttu-id="e8a50-129">接続された Dynamics 365 for Finance and Operations アプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="e8a50-129">Register connected Dynamics 365 for Finance and Operations application</span></span>
1. <span data-ttu-id="e8a50-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-130">Close the page.</span></span> 
2. <span data-ttu-id="e8a50-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-131">Close the page.</span></span> 
3. <span data-ttu-id="e8a50-132">**すべてのワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="e8a50-133">**接続アプリケーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="e8a50-134">コンフィギュレーションされたアプリケーションが Azura に基づいており、現在の RCS ユーザーがアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="e8a50-135">また、現在の RCS ユーザーが、選択されたアプリケーションにアクセスでき、アプリケーションのメタデータにアクセスするための権限を持つユーザーとして登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8a50-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="e8a50-136">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-136">Click **New**.</span></span> 
7. <span data-ttu-id="e8a50-137">**名前**フィールドに、MyConnectedApp と入力します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="e8a50-138">**アプリケーション** フィールドに、https:// mycompany.operations.dynamics.com と入力します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="e8a50-139">**テナント** フィールドに、mycompany.onmicrosoft.com と入力します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="e8a50-140">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-140">Click **Save**.</span></span> 
11. <span data-ttu-id="e8a50-141">コンフィギュレーションされているアプリケーションへの接続を確認するときは、**リモート アプリケーションへの接続**ページで、**ここをクリックして、選択したリモート アプリケーションに接続する**のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="e8a50-142">**接続を確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="e8a50-143">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-143">Click **Close**.</span></span> 
14. <span data-ttu-id="e8a50-144">接続検証に成功すると、現在のグリッドでコンフィギュレーションされているアプリケーションのバージョンとテナントの詳細が更新されます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="e8a50-145">既存のモデル マッピング コンフィギュレーションを確認する</span><span class="sxs-lookup"><span data-stu-id="e8a50-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="e8a50-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-146">Close the page.</span></span> 
2. <span data-ttu-id="e8a50-147">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="e8a50-148">ツリーで、**対外貿易モデル**を展開します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="e8a50-149">ツリーで、**対外貿易モデル\対外貿易マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="e8a50-150">**前提条件**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-150">Expand the **Prerequisites** section.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a50-151">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="e8a50-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="e8a50-152">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="e8a50-153">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="e8a50-154">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="e8a50-155">ツリーで、**Dynamics 365 for Operations\ テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="e8a50-156">**ルートの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="e8a50-157">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-157">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a50-158">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="e8a50-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="e8a50-159">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="e8a50-160">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="e8a50-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-161">Close the page.</span></span> 
13. <span data-ttu-id="e8a50-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="e8a50-163">接続しているアプリケーションをモデルマッピングに割り当てる</span><span class="sxs-lookup"><span data-stu-id="e8a50-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="e8a50-164">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="e8a50-165">**MyConnectedApp** アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-165">Select **MyConnectedApp** application.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a50-166">現在、このマッピングは、選択した接続アプリケーションのメタデータを参照します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="e8a50-167">同じマッピングがメタデータ コンフィギュレーションと接続されたアプリケーションを同時に参照する場合、接続されているアプリケーションのメタデータが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="e8a50-168">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="e8a50-169">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="e8a50-170">ツリーで、**Dynamics 365 for Operations\ テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="e8a50-171">**ルートの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="e8a50-172">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-172">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a50-173">このマッピングは、割り当てられた接続アプリケーションのすべてのメタデータを使用するため、2 つ以上のアプリケーション テーブルが提供されました。</span><span class="sxs-lookup"><span data-stu-id="e8a50-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="e8a50-174">**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="e8a50-175">**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8a50-175">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a50-176">このマッピングに割り当てられた接続アプリケーションのメタデータの詳細を使用して、説明されているデータ ソース項目でデータ モデルの要素が正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="e8a50-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="e8a50-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-177">Close the page.</span></span> 
11. <span data-ttu-id="e8a50-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8a50-178">Close the page.</span></span> 

<span data-ttu-id="e8a50-179">異なるバージョンのアプリケーションのメタデータを使用してこのモデル マッピングを評価する必要がある場合は、接続されている別のアプリケーションを登録してこのモデル マッピングに割り当て、新しいメタデータに対してそれを検証します。</span><span class="sxs-lookup"><span data-stu-id="e8a50-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
