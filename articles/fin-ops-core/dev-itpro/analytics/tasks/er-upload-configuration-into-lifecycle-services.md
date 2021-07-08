---
title: Lifecycle Services へのコンフィギュレーションのアップロード
description: このトピックでは、新しい電子申告 (ER) のコンフィギュレーションを作成して、Microsoft Dynamics Lifecycle Services (LCS) にアップロードする方法について説明します。
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270562"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="11928-103">Lifecycle Services へのコンフィギュレーションのアップロード</span><span class="sxs-lookup"><span data-stu-id="11928-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11928-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、新しい [電子申告 (ER) コンフィギュレーション](../general-electronic-reporting.md#Configuration) を作成し、Microsoft Dynamics Lifecycle Services (LCS) の [プロジェクト レベルのアセット ライブラリ](../../lifecycle-services/asset-library.md) にアップロードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="11928-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11928-105">ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)予定です。</span><span class="sxs-lookup"><span data-stu-id="11928-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="11928-106">詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11928-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="11928-107">この例では、コンフィギュレーションを作成し、それを Litware, Inc. という名前のサンプル会社の LCS にアップロードします。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はどの企業でも完了できます。</span><span class="sxs-lookup"><span data-stu-id="11928-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="11928-108">これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11928-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="11928-109">LCS へのアクセスも必要です。</span><span class="sxs-lookup"><span data-stu-id="11928-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="11928-110">次のロールの 1 つを使用してアプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="11928-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="11928-111">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="11928-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="11928-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="11928-112">System administrator</span></span>

2. <span data-ttu-id="11928-113">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11928-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="11928-114">**Litware, Inc.** を選択し、**アクティブ** としてマークします。</span><span class="sxs-lookup"><span data-stu-id="11928-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="11928-115">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="11928-116">現在の Dynamics 365 Finance ユーザーが、ER コンフィギュレーションをインポートするために使用される [アセット ライブラリ](../../lifecycle-services/asset-library.md#asset-library-support) を含む LCS プロジェクトのメンバーであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="11928-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="11928-117">Finance で使用されているドメインとは異なるドメインを表す ER リポジトリから LCS プロジェクトにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="11928-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="11928-118">試行すると、LCS プロジェクトの空の一覧が表示され、LCS のプロジェクト レベルのアセット ライブラリから ER コンフィギュレーションをインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="11928-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="11928-119">ER コンフィギュレーションのインポートに使用される ER リポジトリからプロジェクト レベルのアセット ライブラリにアクセスするには、現在の Finance インスタンスがプロビジョニングされているテナント (ドメイン) に属するユーザーの資格情報を使用して Finance にサインインします。</span><span class="sxs-lookup"><span data-stu-id="11928-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="11928-120">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="11928-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="11928-121">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11928-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="11928-122">**コンフィギュレーション** ページで、**コンフィギュレーションの作成** を選択して、ドロップ ダウンのダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="11928-123">この例では、電子ドキュメントのサンプル データ モデルを含むコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="11928-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="11928-124">このデータ モデルのコンフィギュレーションは、LCS に後でアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="11928-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="11928-125">**名前** フィールドに、**サンプル モデル コンフィギュレーション** と入力します。</span><span class="sxs-lookup"><span data-stu-id="11928-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="11928-126">**説明** フィールドに、**サンプル モデル コンフィギュレーション** と入力します。</span><span class="sxs-lookup"><span data-stu-id="11928-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="11928-127">**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="11928-128">**モデル デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="11928-129">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-129">Select **New**.</span></span>
8. <span data-ttu-id="11928-130">**名前** フィールドに、**エントリ ポイント** を入力します。</span><span class="sxs-lookup"><span data-stu-id="11928-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="11928-131">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-131">Select **Add**.</span></span>
10. <span data-ttu-id="11928-132">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-132">Select **Save**.</span></span>
11. <span data-ttu-id="11928-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11928-133">Close the page.</span></span>
12. <span data-ttu-id="11928-134">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-134">Select **Change status**.</span></span>
13. <span data-ttu-id="11928-135">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-135">Select **Complete**.</span></span>
14. <span data-ttu-id="11928-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-136">Select **OK**.</span></span>
15. <span data-ttu-id="11928-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11928-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="11928-138">新しいリポジトリの登録</span><span class="sxs-lookup"><span data-stu-id="11928-138">Register a new repository</span></span>

1. <span data-ttu-id="11928-139">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11928-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="11928-140">**コンフィギュレーション プロバイダー** セクションで、**Litware, Inc.** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="11928-141">**Litware, Inc.** タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="11928-142">これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="11928-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="11928-143">**追加** をクリックして、ドロップダウン ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="11928-144">新しいリポジトリを追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="11928-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="11928-145">**コンフィギュレーション リポジトリ入力** フィールドに、**LCS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="11928-146">**レポジトリを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="11928-147">**プロジェクト** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="11928-148">この例の場合、目的の LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="11928-149">プロジェクトに [アクセス](#accessconditions) できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="11928-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="11928-150">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-150">Select **OK**.</span></span>

    <span data-ttu-id="11928-151">新しいリポジトリ エントリを完了します。</span><span class="sxs-lookup"><span data-stu-id="11928-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="11928-152">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="11928-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="11928-153">この例の場合、**LCS** リポジトリ レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="11928-154">登録されているリポジトリが現在のプロバイダーによってマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="11928-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="11928-155">つまり、そのプロバイダーが所有するコンフィギュレーションのみをこのリポジトリに配置し、選択した LCS プロジェクトにアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="11928-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="11928-156">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-156">Select **Open**.</span></span>

    <span data-ttu-id="11928-157">ER コンフィギュレーションの一覧を表示するためにリポジトリを開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="11928-158">選択したプロジェクトが ER コンフィギュレーションの共有に使用されていない場合、一覧は空になります。</span><span class="sxs-lookup"><span data-stu-id="11928-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="11928-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11928-159">Close the page.</span></span>
12. <span data-ttu-id="11928-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11928-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="11928-161">LC へコンフィギュレーションをアップロードする</span><span class="sxs-lookup"><span data-stu-id="11928-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="11928-162">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11928-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="11928-163">**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**サンプル モデルのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="11928-164">すでに完了している作成済みのコンフィギュレーションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11928-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="11928-165">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="11928-166">この例の場合、状態が **完了** となっている選択したコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="11928-167">**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-167">Select **Change status**.</span></span>
5. <span data-ttu-id="11928-168">**共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-168">Select **Share**.</span></span>

    <span data-ttu-id="11928-169">コンフィギュレーションが LCS で公開されると、コンフィギュレーションの状態が **完了** から **共有** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="11928-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="11928-170">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-170">Select **OK**.</span></span>
7. <span data-ttu-id="11928-171">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="11928-172">この例の場合、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="11928-173">選択したバージョンの状態が **完了** から **共有** に変更されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="11928-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="11928-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="11928-174">Close the page.</span></span>
9. <span data-ttu-id="11928-175">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-175">Select **Repositories**.</span></span>

    <span data-ttu-id="11928-176">これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="11928-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="11928-177">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-177">Select **Open**.</span></span>

    <span data-ttu-id="11928-178">この例では、**LCS** リポジトリを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="11928-179">選択したコンフィギュレーションが、選択した LCS プロジェクトのアセットとして表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="11928-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="11928-180"><https://lcs.dynamics.com> に移動して LCS を開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="11928-181">以前にリポジトリの登録に使用したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="11928-182">プロジェクトのアセット ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="11928-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="11928-183">**GER コンフィギュレーション** アセット タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="11928-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="11928-184">アップロードした ER コンフィギュレーションがリストされます。</span><span class="sxs-lookup"><span data-stu-id="11928-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="11928-185">プロバイダーがこの LCS プロジェクトにアクセスできる場合に、アップロードされた LCS コンフィギュレーションは、別のインスタンスにインポートできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="11928-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
