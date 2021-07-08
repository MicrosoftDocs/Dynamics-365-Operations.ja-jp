---
title: Lifecycle Services からのコンフィギュレーションのインポート
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) コンフィギュレーションの新しいバージョンをインポートする方法について説明します。
author: NickSelin
ms.date: 06/17/2021
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
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270840"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="9e474-103">Lifecycle Services からのコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="9e474-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e474-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの [電子申告 (ER) コンフィギュレーション](../general-electronic-reporting.md#Configuration) を Microsoft Dynamics Lifecycle Services (LCS) の [プロジェクト レベルのアセット ライブラリ](../../lifecycle-services/asset-library.md) からインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e474-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e474-105">ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)予定です。</span><span class="sxs-lookup"><span data-stu-id="9e474-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="9e474-106">詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e474-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="9e474-107">この例では、ER コンフィギュレーションの目的のバージョンを選択し、Litware, Inc. という名前のサンプル会社にインポートします。ER コンフィギュレーションは会社間で共有されるため、これらの手順はどの企業でも完了できます。</span><span class="sxs-lookup"><span data-stu-id="9e474-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="9e474-108">これらの手順を完了するには、まず [Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e474-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="9e474-109">LCS へのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="9e474-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="9e474-110">次のロールの 1 つを使用してアプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="9e474-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="9e474-111">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="9e474-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="9e474-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="9e474-112">System administrator</span></span>

2. <span data-ttu-id="9e474-113">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e474-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="9e474-114">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="9e474-115">現在の Dynamics 365 Finance ユーザーが、ER コンフィギュレーションをインポートするために [アクセス](../../lifecycle-services/asset-library.md#asset-library-support) するアセット ライブラリを含む LCS プロジェクトのメンバーであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e474-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="9e474-116">Finance で使用されているドメインとは異なるドメインを表す ER リポジトリから LCS プロジェクトにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9e474-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="9e474-117">試行すると、LCS プロジェクトの空の一覧が表示され、LCS のプロジェクト レベルのアセット ライブラリから ER コンフィギュレーションをインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9e474-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="9e474-118">ER コンフィギュレーションのインポートに使用される ER リポジトリからプロジェクト レベルのアセット ライブラリにアクセスするには、現在の Finance インスタンスがプロビジョニングされているテナント (ドメイン) に属するユーザーの資格情報を使用して Finance にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9e474-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="9e474-119">データ モデル コンフィギュレーションの共有バージョンの削除</span><span class="sxs-lookup"><span data-stu-id="9e474-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="9e474-120">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**サンプル モデルのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="9e474-121">サンプル データ モデル コンフィギュレーションの最初のバージョンを作成し、[Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了したときに、LCS に公開しました。</span><span class="sxs-lookup"><span data-stu-id="9e474-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="9e474-122">この手順では、ER コンフィギュレーションのそのバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="9e474-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="9e474-123">次に、このトピックの後半でそのバージョンを LCS からインポートします。</span><span class="sxs-lookup"><span data-stu-id="9e474-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="9e474-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9e474-125">この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="9e474-126">この状態は、コンフィギュレーションが LCS に公開されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="9e474-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="9e474-127">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-127">Select **Change status**.</span></span>
4. <span data-ttu-id="9e474-128">**中止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="9e474-129">選択したバージョンの状態を **共有** から **中止** に変更することにより、バージョンを削除できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9e474-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="9e474-130">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-130">Select **OK**.</span></span>
6. <span data-ttu-id="9e474-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9e474-132">この例では、状態が **中止** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="9e474-133">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-133">Select **Delete**.</span></span>
8. <span data-ttu-id="9e474-134">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-134">Select **Yes**.</span></span>

    <span data-ttu-id="9e474-135">選択されたデータ モデル コンフィギュレーションのドラフト バージョン 2 だけが使用可能になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e474-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="9e474-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e474-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="9e474-137">データ モデル コンフィギュレーションの共有バージョンを LCS からインポートする</span><span class="sxs-lookup"><span data-stu-id="9e474-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="9e474-138">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e474-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="9e474-139">**コンフィギュレーション プロバイダー** セクションで、**Litware, Inc.** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="9e474-140">**Litware, Inc.** タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="9e474-141">これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9e474-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="9e474-142">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-142">Select **Open**.</span></span>

    <span data-ttu-id="9e474-143">この例では、**LCS** リポジトリを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="9e474-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="9e474-144">LCS プロジェクトと選択した ER リポジトリがアクセスするアセット ライブラリへの [アクセス権](#accessconditions) が必要です。</span><span class="sxs-lookup"><span data-stu-id="9e474-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="9e474-145">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9e474-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="9e474-146">この例では、バージョンの一覧の **サンプル モデル コンフィギュレーション** の最初のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="9e474-147">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-147">Select **Import**.</span></span>
7. <span data-ttu-id="9e474-148">**はい** を選択して、LCS からの選択したバージョンのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="9e474-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="9e474-149">選択したバージョンが正常にインポートされたことを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e474-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="9e474-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e474-150">Close the page.</span></span>
9. <span data-ttu-id="9e474-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e474-151">Close the page.</span></span>
10. <span data-ttu-id="9e474-152">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="9e474-153">ツリーで、**サンプル モデル コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="9e474-154">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="9e474-155">この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e474-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="9e474-156">選択したデータ モデル コンフィギュレーションの共有バージョン 1 も使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9e474-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
