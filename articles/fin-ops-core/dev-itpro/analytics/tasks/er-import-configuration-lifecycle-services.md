---
title: Lifecycle Services からのコンフィギュレーションのインポート
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) コンフィギュレーションの新しいバージョンをインポートする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 636ed27c157c8322cc1be4ca8eca10ef37eb8bbc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569512"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="4f385-103">Lifecycle Services からのコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="4f385-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f385-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの [電子申告 (ER) コンフィギュレーション](../general-electronic-reporting.md#Configuration) を Microsoft Dynamics Lifecycle Services (LCS) の [プロジェクト レベルのアセット ライブラリ](../../lifecycle-services/asset-library.md) からインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f385-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="4f385-105">この例では、ER コンフィギュレーションの目的のバージョンを選択し、Litware, Inc. という名前のサンプル会社にインポートします。ER コンフィギュレーションは会社間で共有されるため、これらの手順はどの企業でも完了できます。</span><span class="sxs-lookup"><span data-stu-id="4f385-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="4f385-106">これらの手順を完了するには、まず [Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f385-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="4f385-107">LCS へのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="4f385-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="4f385-108">次のロールの 1 つを使用してアプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="4f385-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="4f385-109">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="4f385-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="4f385-110">システム管理者</span><span class="sxs-lookup"><span data-stu-id="4f385-110">System administrator</span></span>

2. <span data-ttu-id="4f385-111">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f385-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="4f385-112">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="4f385-113">現在の Dynamics 365 Finance ユーザーが、ER コンフィギュレーションをインポートするために [アクセス](../../lifecycle-services/asset-library.md#asset-library-support) するアセット ライブラリを含む LCS プロジェクトのメンバーであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f385-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="4f385-114">Finance で使用されているドメインとは異なるドメインを表す ER リポジトリから LCS プロジェクトにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4f385-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="4f385-115">試行すると、LCS プロジェクトの空の一覧が表示され、LCS のプロジェクト レベルのアセット ライブラリから ER コンフィギュレーションをインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4f385-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="4f385-116">ER コンフィギュレーションのインポートに使用される ER リポジトリからプロジェクト レベルのアセット ライブラリにアクセスするには、現在の Finance インスタンスがプロビジョニングされているテナント (ドメイン) に属するユーザーの資格情報を使用して Finance にサインインします。</span><span class="sxs-lookup"><span data-stu-id="4f385-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="4f385-117">データ モデル コンフィギュレーションの共有バージョンの削除</span><span class="sxs-lookup"><span data-stu-id="4f385-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="4f385-118">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**サンプル モデルのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="4f385-119">サンプル データ モデル コンフィギュレーションの最初のバージョンを作成し、[Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了したときに、LCS に公開しました。</span><span class="sxs-lookup"><span data-stu-id="4f385-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="4f385-120">この手順では、ER コンフィギュレーションのそのバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="4f385-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="4f385-121">次に、このトピックの後半でそのバージョンを LCS からインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f385-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="4f385-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4f385-123">この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="4f385-124">この状態は、コンフィギュレーションが LCS に公開されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="4f385-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="4f385-125">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-125">Select **Change status**.</span></span>
4. <span data-ttu-id="4f385-126">**中止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="4f385-127">選択したバージョンの状態を **共有** から **中止** に変更することにより、バージョンを削除できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4f385-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="4f385-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-128">Select **OK**.</span></span>
6. <span data-ttu-id="4f385-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4f385-130">この例では、状態が **中止** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="4f385-131">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-131">Select **Delete**.</span></span>
8. <span data-ttu-id="4f385-132">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-132">Select **Yes**.</span></span>

    <span data-ttu-id="4f385-133">選択されたデータ モデル コンフィギュレーションのドラフト バージョン 2 だけが使用可能になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f385-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="4f385-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f385-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="4f385-135">データ モデル コンフィギュレーションの共有バージョンを LCS からインポートする</span><span class="sxs-lookup"><span data-stu-id="4f385-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="4f385-136">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f385-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="4f385-137">**コンフィギュレーション プロバイダー** セクションで、**Litware, Inc.** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="4f385-138">**Litware, Inc.** タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="4f385-139">これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4f385-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="4f385-140">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-140">Select **Open**.</span></span>

    <span data-ttu-id="4f385-141">この例では、**LCS** リポジトリを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="4f385-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="4f385-142">LCS プロジェクトと選択した ER リポジトリがアクセスするアセット ライブラリへの [アクセス権](#accessconditions) が必要です。</span><span class="sxs-lookup"><span data-stu-id="4f385-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="4f385-143">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4f385-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="4f385-144">この例では、バージョンの一覧の **サンプル モデル コンフィギュレーション** の最初のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="4f385-145">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-145">Select **Import**.</span></span>
7. <span data-ttu-id="4f385-146">**はい** を選択して、LCS からの選択したバージョンのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f385-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="4f385-147">選択したバージョンが正常にインポートされたことを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f385-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="4f385-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f385-148">Close the page.</span></span>
9. <span data-ttu-id="4f385-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4f385-149">Close the page.</span></span>
10. <span data-ttu-id="4f385-150">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="4f385-151">ツリーで、**サンプル モデル コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="4f385-152">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4f385-153">この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f385-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="4f385-154">選択したデータ モデル コンフィギュレーションの共有バージョン 1 も使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4f385-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]