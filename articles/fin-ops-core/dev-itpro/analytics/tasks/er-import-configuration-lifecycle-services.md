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
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142389"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="eb276-103">Lifecycle Services からのコンフィギュレーションの ER インポート</span><span class="sxs-lookup"><span data-stu-id="eb276-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb276-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの電子申告 (ER) コンフィギュレーションを Microsoft Lifecycle Services (LCS) からインポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="eb276-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="eb276-105">この例では、ER コンフィギュレーションの必要なバージョンを選択し、サンプル会社の Litware, Inc. 用にインポートします。ER コンフィギュレーションは会社間で共有されるため、これらのステップはすべての会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="eb276-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="eb276-106">これらの手順を完了するには、まず 「Lifecycle Services に ER 構成をアップロードする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb276-106">To complete these steps, you must first complete the steps in the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="eb276-107">LCS へのアクセスは、次の手順の完了にも必要です。</span><span class="sxs-lookup"><span data-stu-id="eb276-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="eb276-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eb276-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="eb276-109">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="eb276-110">データ モデルのコンフィギュレーションの共有バージョンの削除</span><span class="sxs-lookup"><span data-stu-id="eb276-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="eb276-111">ツリーで、「サンプル モデル コンフィギュレーション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="eb276-112">サンプル データ モデル構成の最初のバージョンが作成され、「Lifecycle Services に ER 構成をアップロードする」 に記載のを進める過程で LCS に公開されました。</span><span class="sxs-lookup"><span data-stu-id="eb276-112">The first version of a sample data model configuration has been created and published to LCS during the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="eb276-113">この手順では、ER コンフィギュレーションのこのバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="eb276-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="eb276-114">サンプル データ モデルのコンフィギュレーションのこのバージョンは、LCS からインポートされます。</span><span class="sxs-lookup"><span data-stu-id="eb276-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="eb276-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb276-116">状態が 「共有」 となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-116">Select the version of this configuration that is in the 'Shared' status.</span></span> <span data-ttu-id="eb276-117">この状態は、コンフィギュレーションが LCS に公開されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="eb276-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="eb276-118">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-118">Click Change status.</span></span>
4. <span data-ttu-id="eb276-119">[中止] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-119">Click Discontinue.</span></span>
    * <span data-ttu-id="eb276-120">選択したバージョンの状態を 「共有」 から 「中止」 に変更し、削除できるようにします。</span><span class="sxs-lookup"><span data-stu-id="eb276-120">Change the status of the selected version from 'Shared' to 'Discontinued' to make it available for deletion.</span></span>  
5. <span data-ttu-id="eb276-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-121">Click OK.</span></span>
6. <span data-ttu-id="eb276-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb276-123">状態が 「中止」 となっている構成ののバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-123">Select the version of this configuration that has a status of 'Discontinued'.</span></span>  
7. <span data-ttu-id="eb276-124">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-124">Click Delete.</span></span>
8. <span data-ttu-id="eb276-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-125">Click Yes.</span></span>
    * <span data-ttu-id="eb276-126">選択されたデータ モデルのコンフィギュレーションのドラフト バージョン 2 だけが使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eb276-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="eb276-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb276-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="eb276-128">データ モデルのコンフィギュレーションの共有バージョンを LCS からインポートする</span><span class="sxs-lookup"><span data-stu-id="eb276-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="eb276-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="eb276-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eb276-130">「Litware, Inc.」 のリポジトリ一覧を開きます</span><span class="sxs-lookup"><span data-stu-id="eb276-130">Open the list of repositories for the 'Litware, Inc.'</span></span> <span data-ttu-id="eb276-131">。</span><span class="sxs-lookup"><span data-stu-id="eb276-131">configuration provider.</span></span>  
2. <span data-ttu-id="eb276-132">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-132">Click Repositories.</span></span>
3. <span data-ttu-id="eb276-133">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-133">Click Open.</span></span>
    * <span data-ttu-id="eb276-134">LCS リポジトリを選択し、開きます。</span><span class="sxs-lookup"><span data-stu-id="eb276-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="eb276-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="eb276-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eb276-136">バージョンの一覧の「サンプル モデル コンフィギュレーション」の最初のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="eb276-137">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-137">Click Import.</span></span>
6. <span data-ttu-id="eb276-138">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-138">Click Yes.</span></span>
    * <span data-ttu-id="eb276-139">LCS から 選択されたバージョンのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="eb276-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="eb276-140">情報メッセージ (フォームの上部) により、選択されたバージョンのインポートが正常に完了したことを確認できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eb276-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="eb276-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb276-141">Close the page.</span></span>
8. <span data-ttu-id="eb276-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb276-142">Close the page.</span></span>
9. <span data-ttu-id="eb276-143">[コンフィギュレーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb276-143">Click Configurations.</span></span>
10. <span data-ttu-id="eb276-144">ツリーで、「サンプル モデル コンフィギュレーション」を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="eb276-145">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eb276-146">状態が 「共有」 となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eb276-146">Select the version of this configuration that has a status of 'Shared'.</span></span>  
    * <span data-ttu-id="eb276-147">なお、選択されたデータ モデルのコンフィギュレーションの共有バージョン 1 も使用できようになっています。</span><span class="sxs-lookup"><span data-stu-id="eb276-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

