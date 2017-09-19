--- 
title: "電子申告 (ER) 用に Lifecycle Services にコンフィギュレーションをアップロードする"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、新しい電子申告 (ER) コンフィギュレーションを作成し、Microsoft Lifecycle Services (LCS) にアップロードする方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0681ff81ea673e90b3d281a8e8836e0afb9f5f0
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="c19e3-103">電子申告 (ER) 用に Lifecycle Services にコンフィギュレーションをアップロードする</span><span class="sxs-lookup"><span data-stu-id="c19e3-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c19e3-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、新しい電子申告 (ER) コンフィギュレーションを作成し、Microsoft Lifecycle Services (LCS) にアップロードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c19e3-105">この例では、コンフィギュレーションを作成し、それをサンプル会社 Litware, Inc. の LCS にアップロードします。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c19e3-106">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19e3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="c19e3-107">LCS へのアクセスは、次の手順の完了にも必要です。</span><span class="sxs-lookup"><span data-stu-id="c19e3-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="c19e3-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c19e3-109">「Litware, Inc.」 を選択して</span><span class="sxs-lookup"><span data-stu-id="c19e3-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="c19e3-110">有効と設定します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-110">and set it as active.</span></span>
3. <span data-ttu-id="c19e3-111">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c19e3-112">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="c19e3-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="c19e3-113">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="c19e3-114">電子ドキュメントのサンプル データ モデルを含むコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="c19e3-115">このデータ モデルのコンフィギュレーションは、LCS に後でアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="c19e3-116">[名前] フィールドに、「サンプル モデル コンフィギュレーション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="c19e3-117">サンプル モデルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c19e3-117">Sample model configuration</span></span>  
3. <span data-ttu-id="c19e3-118">[説明] フィールドに、「サンプル モデル コンフィギュレーション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="c19e3-119">サンプル モデルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c19e3-119">Sample model configuration</span></span>  
4. <span data-ttu-id="c19e3-120">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-120">Click Create configuration.</span></span>
5. <span data-ttu-id="c19e3-121">[モデル デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-121">Click Model designer.</span></span>
6. <span data-ttu-id="c19e3-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-122">Click New.</span></span>
7. <span data-ttu-id="c19e3-123">[名前] フィールドに、「エントリ ポイント」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="c19e3-124">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="c19e3-124">Entry point</span></span>  
8. <span data-ttu-id="c19e3-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-125">Click Add.</span></span>
9. <span data-ttu-id="c19e3-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-126">Click Save.</span></span>
10. <span data-ttu-id="c19e3-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-127">Close the page.</span></span>
11. <span data-ttu-id="c19e3-128">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-128">Click Change status.</span></span>
12. <span data-ttu-id="c19e3-129">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-129">Click Complete.</span></span>
13. <span data-ttu-id="c19e3-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="c19e3-131">新しいリポジトリの登録</span><span class="sxs-lookup"><span data-stu-id="c19e3-131">Register a new  repository</span></span>
1. <span data-ttu-id="c19e3-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-132">Close the page.</span></span>
2. <span data-ttu-id="c19e3-133">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-133">Click Repositories.</span></span>
    * <span data-ttu-id="c19e3-134">これにより、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます 。</span><span class="sxs-lookup"><span data-stu-id="c19e3-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="c19e3-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="c19e3-136">これにより、新しいリポジトリを追加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c19e3-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="c19e3-137">[コンフィギュレーション リポジトリ タイプ] フィールドで [LCS] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="c19e3-138">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-138">Click Create repository.</span></span>
6. <span data-ttu-id="c19e3-139">[プロジェクト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="c19e3-140">必要な LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-140">Select the desired LCS project.</span></span> <span data-ttu-id="c19e3-141">プロジェクトにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19e3-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="c19e3-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-142">Click OK.</span></span>
    * <span data-ttu-id="c19e3-143">新しいリポジトリ エントリを完了します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="c19e3-144">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c19e3-145">[LCS リポジトリ] レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="c19e3-146">登録済リポジトリが現行プロバイダーによってマークされていることは、プロバイダーによって所有されているコンフィギュレーションだけがこのリポジトリに配置されること、したがって、選択された LCS プロジェクトにアップロードされることを意味することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c19e3-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="c19e3-147">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-147">Click Open.</span></span>
    * <span data-ttu-id="c19e3-148">ER コンフィギュレーションの一覧を表示するためにリポジトリを開きます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="c19e3-149">ER コンフィギュレーションの共有に、このプロジェクトが使用されていない場合は空になります。</span><span class="sxs-lookup"><span data-stu-id="c19e3-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="c19e3-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-150">Close the page.</span></span>
11. <span data-ttu-id="c19e3-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="c19e3-152">コンフィギュレーションの LCS へのアップロード</span><span class="sxs-lookup"><span data-stu-id="c19e3-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="c19e3-153">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-153">Click Configurations.</span></span>
2. <span data-ttu-id="c19e3-154">ツリーで、「サンプル モデル コンフィギュレーション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="c19e3-155">完了している作成されたコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="c19e3-156">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c19e3-157">「完了済」の状態の選択されたコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="c19e3-158">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-158">Click Change status.</span></span>
5. <span data-ttu-id="c19e3-159">[共有] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-159">Click Share.</span></span>
    * <span data-ttu-id="c19e3-160">コンフィギュレーションの状態は、LCS で公開されると「完了」から「共有」に変更します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="c19e3-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-161">Click OK.</span></span>
7. <span data-ttu-id="c19e3-162">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c19e3-163">「共有」という状態のコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c19e3-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="c19e3-164">選択されたバージョンの状態が「完了」から「共有」に変更されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c19e3-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="c19e3-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-165">Close the page.</span></span>
9. <span data-ttu-id="c19e3-166">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-166">Click Repositories.</span></span>
    * <span data-ttu-id="c19e3-167">これにより、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます 。</span><span class="sxs-lookup"><span data-stu-id="c19e3-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="c19e3-168">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c19e3-168">Click Open.</span></span>
    * <span data-ttu-id="c19e3-169">LCS リポジトリを選択し、開きます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="c19e3-170">選択されたコンフィギュレーションが、選択された LCS プロジェクトの資産として表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c19e3-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="c19e3-171">https://lcs.dynamics.com から LCS を開きます。</span><span class="sxs-lookup"><span data-stu-id="c19e3-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="c19e3-172">リポジトリの登録のために以前に使用されたプロジェクトを開きます。このプロジェクトの「アセット ライブラリ」を開き、「GER コンフィギュレーション」資産タイプの中身を展開します – アップロードされた ER コンフィギュレーションが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c19e3-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="c19e3-173">プロバイダーがこの LCS プロジェクトにアクセスできる場合は、アップロードされた LCS コンフィギュレーションは別の Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition インスタンスにインポートできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c19e3-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

