---
title: Lifecycle Services からのコンフィギュレーションの ER インポート
description: 次の手順では、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの電子申告 (ER) コンフィギュレーションを Microsoft Lifecycle Services (LCS) からインポートする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184833"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="7d9e4-103">Lifecycle Services からのコンフィギュレーションの ER インポート</span><span class="sxs-lookup"><span data-stu-id="7d9e4-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d9e4-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの電子申告 (ER) コンフィギュレーションを Microsoft Lifecycle Services (LCS) からインポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7d9e4-105">この例では、ER コンフィギュレーションの必要なバージョンを選択し、サンプル会社の Litware, Inc. 用にインポートします。ER コンフィギュレーションは会社間で共有されるため、これらのステップはすべての会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="7d9e4-106">これらの手順を完了するには、先に「Lifecycle Services への ER コンフィギュレーションのアップロード」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="7d9e4-107">LCS へのアクセスは、次の手順の完了にも必要です。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="7d9e4-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7d9e4-109">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="7d9e4-110">データ モデルのコンフィギュレーションの共有バージョンの削除</span><span class="sxs-lookup"><span data-stu-id="7d9e4-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="7d9e4-111">ツリーで、「サンプル モデル コンフィギュレーション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="7d9e4-112">サンプル データ モデルのコンフィギュレーションの最初のバージョンが作成され、「Lifecycle Services への ER コンフィギュレーションのアップロード」手順中に LCS に公開されました。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="7d9e4-113">この手順では、ER コンフィギュレーションのこのバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="7d9e4-114">サンプル データ モデルのコンフィギュレーションのこのバージョンは、LCS からインポートされます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="7d9e4-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7d9e4-116">「共有」状態にあるコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="7d9e4-117">この状態は、コンフィギュレーションが LCS に公開されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="7d9e4-118">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-118">Click Change status.</span></span>
4. <span data-ttu-id="7d9e4-119">[中止] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-119">Click Discontinue.</span></span>
    * <span data-ttu-id="7d9e4-120">選択されたバージョンの状態を「共有」から「中止」に変更し、削除できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="7d9e4-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-121">Click OK.</span></span>
6. <span data-ttu-id="7d9e4-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7d9e4-123">「中止」状態にあるコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="7d9e4-124">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-124">Click Delete.</span></span>
8. <span data-ttu-id="7d9e4-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-125">Click Yes.</span></span>
    * <span data-ttu-id="7d9e4-126">選択されたデータ モデルのコンフィギュレーションのドラフト バージョン 2 だけが使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="7d9e4-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="7d9e4-128">データ モデルのコンフィギュレーションの共有バージョンを LCS からインポートする</span><span class="sxs-lookup"><span data-stu-id="7d9e4-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="7d9e4-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d9e4-130">「Litware, Inc.」コンフィギュレーション プロバイダーのリポジトリの一覧を開きます</span><span class="sxs-lookup"><span data-stu-id="7d9e4-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="7d9e4-131">。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-131">configuration provider.</span></span>  
2. <span data-ttu-id="7d9e4-132">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-132">Click Repositories.</span></span>
3. <span data-ttu-id="7d9e4-133">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-133">Click Open.</span></span>
    * <span data-ttu-id="7d9e4-134">LCS リポジトリを選択し、開きます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="7d9e4-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d9e4-136">バージョンの一覧の「サンプル モデル コンフィギュレーション」の最初のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="7d9e4-137">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-137">Click Import.</span></span>
6. <span data-ttu-id="7d9e4-138">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-138">Click Yes.</span></span>
    * <span data-ttu-id="7d9e4-139">LCS から 選択されたバージョンのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="7d9e4-140">情報メッセージ (フォームの上部) により、選択されたバージョンのインポートが正常に完了したことを確認できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="7d9e4-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-141">Close the page.</span></span>
8. <span data-ttu-id="7d9e4-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-142">Close the page.</span></span>
9. <span data-ttu-id="7d9e4-143">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-143">Click Configurations.</span></span>
10. <span data-ttu-id="7d9e4-144">ツリーで、「サンプル モデル コンフィギュレーション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="7d9e4-145">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7d9e4-146">「共有」状態にあるコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="7d9e4-147">なお、選択されたデータ モデルのコンフィギュレーションの共有バージョン 1 も使用できようになっています。</span><span class="sxs-lookup"><span data-stu-id="7d9e4-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  
