---
title: Lifecycle Services (LCS) のアセット ライブラリ
description: このトピックでは、Lifecycle Services (LCS) のアセット ライブラリ機能について説明します。
author: laneswenka
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 266824
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c1496ce3884c478b4e833512f4f2e1349f8961c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881700"
---
# <a name="asset-library-in-lifecycle-services-lcs"></a><span data-ttu-id="e4f2c-103">Lifecycle Services (LCS) のアセット ライブラリ</span><span class="sxs-lookup"><span data-stu-id="e4f2c-103">Asset library in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4f2c-104">アセット ライブラリは、Microsoft Dynamics Lifecycle Services (LCS) のテナントに関連付けられているさまざまな資産の保管場所です。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-104">The Asset library is a storage location for the various assets that are associated with a tenant in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e4f2c-105">LCS には、共用資産ライブラリとプロジェクト レベルのアセット ライブラリの 2 種類のアセット ライブラリがあります。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-105">Two types of Asset library are available in LCS: the Shared asset library and the project-level Asset library.</span></span>

- <span data-ttu-id="e4f2c-106">**共有資産ライブラリ** – 共有資産ライブラリは、Microsoft およびパートナーによって資産を共有するために複数のテナント、プロジェクト、および LCS の環境の間で 使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-106">**Shared asset library** – The Shared asset library is used by Microsoft and Partners to share assets across multiple tenants, projects, and environments in LCS.</span></span> <span data-ttu-id="e4f2c-107">このライブラリは、LCS にサインインするすべてのユーザーがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-107">This library can be accessed by any user who signs in to LCS.</span></span> <span data-ttu-id="e4f2c-108">共用資産ライブラリにアクセスするには、LCS にサイン インして、**共用資産ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-108">To access the Shared asset library, sign in to LCS, and then click the **Shared asset library** tile.</span></span>

    <span data-ttu-id="e4f2c-109">[![共有アセット ライブラリ タイル](./media/SharedAssetLibrary.jpg)](./media/SharedAssetLibrary.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4f2c-109">[![Shared asset library tile](./media/SharedAssetLibrary.jpg)](./media/SharedAssetLibrary.jpg)</span></span>

- <span data-ttu-id="e4f2c-110">**プロジェクト レベルのアセット ライブラリ** – プロジェクト レベルの資産ライブラリは、LCS のプロジェクト内の環境全体で資産を共有するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-110">**Project-level Asset library** – The project-level Asset library is used to share assets across environments within a project in LCS.</span></span> <span data-ttu-id="e4f2c-111">このライブラリはプロジェクト内のすべてのユーザーがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-111">This library can be accessed by all users within a project.</span></span> <span data-ttu-id="e4f2c-112">。プロジェクト レベルのアセット ライブラリにアクセスするには、LCS にサイン インし、プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-112">To access the project-level Asset library, sign in to LCS, and open a project.</span></span> <span data-ttu-id="e4f2c-113">ハンバーガー メニューで、**アセット ライブラリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-113">Then, on the hamburger menu, click **Asset library**.</span></span>

    <span data-ttu-id="e4f2c-114">[![プロジェクト レベル資産ライブラリを開きます](./media/ProjectAssetLibrary.jpg)](./media/ProjectAssetLibrary.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4f2c-114">[![Opening the project-level Asset library](./media/ProjectAssetLibrary.jpg)](./media/ProjectAssetLibrary.jpg)</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e4f2c-115">プロジェクト アセット ライブラリ内で同じアセットのバージョンのアップロードはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-115">Uploading versions for the same asset in the project asset library is not supported.</span></span> 

## <a name="asset-library-support"></a><span data-ttu-id="e4f2c-116">アセット ライブラリ サポート</span><span class="sxs-lookup"><span data-stu-id="e4f2c-116">Asset library support</span></span>
<span data-ttu-id="e4f2c-117">アセット ライブラリは、複数のタイプの資産をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-117">The Asset library supports multiple types of assets.</span></span> <span data-ttu-id="e4f2c-118">頻繁に使用されるいくつかの資産タイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-118">Here are some asset types that are frequently used:</span></span>

- <span data-ttu-id="e4f2c-119">**ソフトウェア配置可能パッケージ** – この資産のタイプは、環境を最新のアップデートセットで更新するために使用されるすべてのパッケージを表します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-119">**Software deployable package** – This asset type represents all the packages that are used to update an environment with the latest set of updates.</span></span>
- <span data-ttu-id="e4f2c-120">**データ パッケージ** - このアセット タイプは、コンフィギュレーションおよびデータ管理に使用されるアセットを格納します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-120">**Data package** – This asset type stores assets that are used for configuration and data management.</span></span>
- <span data-ttu-id="e4f2c-121">**GER コンフィギュレーション** – この資産タイプは、クライアントに適用されるすべてのローカライズおよび翻訳資産を格納します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-121">**GER Configuration** – This asset type stores all localization and translation assets that are applied to the client.</span></span>
- <span data-ttu-id="e4f2c-122">**Retail SDK** – この資産タイプには Retail ソフトウェアの開発キット (SDK) の最新のスクリプトがすべて格納されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-122">**Retail SDK** – This asset type stores all the latest scripts for the Retail software development kit (SDK).</span></span>
- <span data-ttu-id="e4f2c-123">**データベース バックアップ** - このアセット タイプは、サンドボックス階層 2 - 5 環境からデータベースをインポートおよびエクスポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-123">**Database backups** - This asset type is used for import and export of databases from Sandbox Tiers 2 - 5 environments.</span></span>

### <a name="asset-scopes"></a><span data-ttu-id="e4f2c-124">アセット スコープ</span><span class="sxs-lookup"><span data-stu-id="e4f2c-124">Asset scopes</span></span>
<span data-ttu-id="e4f2c-125">アセット ライブラリがサポートするすべての資産には複数のスコープがあります。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-125">Every asset that the Asset library supports has multiple scopes.</span></span> <span data-ttu-id="e4f2c-126">サポートされる資産スコープのいくつかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-126">Here are some of the supported asset scopes:</span></span>

- <span data-ttu-id="e4f2c-127">**自分自身** – 資産は、アップロードされるときに、**自分自身** スコープに設定されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-127">**Me** – When an asset is uploaded, it's set to the **Me** scope.</span></span> <span data-ttu-id="e4f2c-128">**Me** スコープの資産は、資産をアップロードしたユーザーにのみに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-128">An asset that has the **Me** scope is visible only to the person who uploaded the asset.</span></span>
- <span data-ttu-id="e4f2c-129">**プロジェクト** – アセットを **グローバル** スコープから別のプロジェクトにインポートすると、**プロジェクト** スコープに設定されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-129">**Project** – When an asset is imported from the **Global** scope to another project, it's set to the **Project** scope.</span></span>
- <span data-ttu-id="e4f2c-130">**組織** – テナント内の複数のユーザーで資産を共有するとき、テナント管理は、資産を **組織** スコープに昇格できます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-130">**Organization** – When an asset must be shared with multiple users within a tenant, the tenant admin can promote the asset to the **Organization** scope.</span></span>
- <span data-ttu-id="e4f2c-131">**グローバル** – Microsoft だけが資産を **グローバル** スコープにアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-131">**Global** – Only Microsoft can upload assets to the **Global** scope.</span></span> <span data-ttu-id="e4f2c-132">これらのアセットは、Microsoft がすべての LCS プロジェクトおよびユーザーに公に利用されることを望むアセットです。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-132">These assets are assets that Microsoft wants to be made publicly available to all LCS projects and users.</span></span>

### <a name="asset-status"></a><span data-ttu-id="e4f2c-133">アセット ステータス</span><span class="sxs-lookup"><span data-stu-id="e4f2c-133">Asset status</span></span>
<span data-ttu-id="e4f2c-134">すべての資産には **ドラフト** または **発行済** の 2 つ状態のどちらかがあります。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-134">Every asset has one of two statuses: **Draft** or **Published**.</span></span>

- <span data-ttu-id="e4f2c-135">**ドラフト** - 資産はまだ編集できます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-135">**Draft** – The asset can still be edited.</span></span>
- <span data-ttu-id="e4f2c-136">**公開済** – 資産は、**組織** または **グローバル** スコープ、および編集を完了します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-136">**Published** – The asset is published at an **Organization** or **Global** scope, and edits are completed.</span></span>

## <a name="actions-in-the-asset-library"></a><span data-ttu-id="e4f2c-137">資産ライブラリのアクション</span><span class="sxs-lookup"><span data-stu-id="e4f2c-137">Actions in the Asset library</span></span>
<span data-ttu-id="e4f2c-138">必要に応じてアセット ライブラリでさまざまなアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-138">You can perform various actions in the Asset library as you require.</span></span>

### <a name="upload-an-asset-to-the-asset-library"></a><span data-ttu-id="e4f2c-139">アセットをアセット ライブラリにアップロード</span><span class="sxs-lookup"><span data-stu-id="e4f2c-139">Upload an asset to the Asset library</span></span>
1. <span data-ttu-id="e4f2c-140">資産をアップロードするタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-140">Select the tab to upload the asset to.</span></span>
2. <span data-ttu-id="e4f2c-141">プラス記号 (**+**) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-141">Click the plus sign (**+**).</span></span>
3. <span data-ttu-id="e4f2c-142">資産の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-142">Enter a name and description for the asset.</span></span>
4. <span data-ttu-id="e4f2c-143">アセットのファイルをアップロードし、**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-143">Upload the file for the asset, and then click **Confirm**.</span></span>

### <a name="upload-a-new-version-for-a-specific-asset-shared-asset-library-only"></a><span data-ttu-id="e4f2c-144">特定のアセットの新しいバージョンをアップロードする (共有アセット ライブラリのみ)</span><span class="sxs-lookup"><span data-stu-id="e4f2c-144">Upload a new version for a specific asset (Shared asset library only)</span></span>
1. <span data-ttu-id="e4f2c-145">アセット ライブラリで資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-145">Select the asset in the Asset library.</span></span>
2. <span data-ttu-id="e4f2c-146">ツール バーで、**新しいバージョンのアップロード** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-146">On the toolbar, click the **Upload new version** button.</span></span>
3. <span data-ttu-id="e4f2c-147">前の手順の手順を繰り返し、「資産を資産ライブラリにアップロード」します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-147">Repeat the steps in the previous procedure, "Upload an asset to the asset library."</span></span>
4. <span data-ttu-id="e4f2c-148">ツール バーで、**バージョン** をクリックして、単一の資産の複数のバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-148">On the toolbar, click **Versions** to view multiple versions for a single asset.</span></span>
5. <span data-ttu-id="e4f2c-149">これにより、個々のバージョンを特定のプロジェクト アセット ライブラリに必要に応じてインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-149">Individual versions can then be imported in to a specific project asset library as required.</span></span>

### <a name="move-assets-from-the-shared-asset-library-to-the-project-level-asset-library"></a><span data-ttu-id="e4f2c-150">共有アセット ライブラリからプロジェクト レベルのアセット ライブラリへ資産を移動する</span><span class="sxs-lookup"><span data-stu-id="e4f2c-150">Move assets from the Shared asset library to the project-level Asset library</span></span>
<span data-ttu-id="e4f2c-151">共有アセット ライブラリからプロジェクト レベルのアセット ライブラリに資産を移動するには、資産をインポートするかコピーするかの 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-151">There are two ways to move an asset from the Shared asset library to the project-level asset library: you can import the asset or copy it.</span></span>

#### <a name="import-from-the-shared-asset-library"></a><span data-ttu-id="e4f2c-152">共有アセット ライブラリからのインポート</span><span class="sxs-lookup"><span data-stu-id="e4f2c-152">Import from the Shared asset library</span></span>
<span data-ttu-id="e4f2c-153">共有アセット ライブラリからの資産をプロジェクト レベルのアセット ライブラリへインポートして、環境間で適用できるようにするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-153">Follow these steps to import an asset from the Shared asset library to the project-level Asset library so that it can be applied across environments.</span></span>

1. <span data-ttu-id="e4f2c-154">プロジェクト レベルのアセット ライブラリで、インポートするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-154">In the project-level Asset library, select the tab for the asset type to import.</span></span>
2. <span data-ttu-id="e4f2c-155">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-155">Click **Import**.</span></span>
3. <span data-ttu-id="e4f2c-156">共有アセット ライブラリのアセットの一覧で、インポートするアセットを選択してから **選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-156">In the list of assets in the Shared asset library, select the asset to import, and then click **Pick**.</span></span>

<span data-ttu-id="e4f2c-157">選択したアセットをインポートし、プロジェクト レベルのアセット ライブラリに配置します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-157">The selected asset is imported and put into the project-level Asset library.</span></span> <span data-ttu-id="e4f2c-158">プロジェクト レベルのアセット ライブラリのアセットの状態は **公開済** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-158">The status of the asset in the project-level Asset library is set to **Published**.</span></span> <span data-ttu-id="e4f2c-159">このメソッドは、編集する予定のないパッケージを対象としています。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-159">This method is for packages that you don't plan to edit.</span></span> <span data-ttu-id="e4f2c-160">インポートされたパッケージを編集する場合は、次の手順を使用して、コピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-160">If you want to edit an imported package, create a copy by using the following procedure.</span></span> <span data-ttu-id="e4f2c-161">パッケージの状態は **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-161">The status of the package will then be **Draft**.</span></span>

#### <a name="copy-from-the-shared-asset-library"></a><span data-ttu-id="e4f2c-162">共有アセット ライブラリからのコピー</span><span class="sxs-lookup"><span data-stu-id="e4f2c-162">Copy from the Shared asset library</span></span>
<span data-ttu-id="e4f2c-163">資産のコピーを編集できるよう作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-163">Follow these steps to create a copy of an asset so that it can be edited.</span></span>

1. <span data-ttu-id="e4f2c-164">プロジェクト レベルのアセット ライブラリで、コピーするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-164">In the project-level Asset library, select the tab for the asset type to copy.</span></span>
2. <span data-ttu-id="e4f2c-165">コピーするアセットを選択し、ツール バーで **コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-165">Select the asset to copy, and then, on the toolbar, click **Copy**.</span></span>

<span data-ttu-id="e4f2c-166">発行済みのアセットのコピーが作成され、状態は **Draft** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-166">A copy of the published asset is created, and the status is set to **Draft**.</span></span>

### <a name="save-to-my-library"></a><span data-ttu-id="e4f2c-167">自分のライブラリに保存</span><span class="sxs-lookup"><span data-stu-id="e4f2c-167">Save to my library</span></span>
<span data-ttu-id="e4f2c-168">アセットを編集した後、以下の手順に従って編集したアセットを共有アセット ライブラリに戻し、**組織** スコープを促進させることにより複数の顧客と共有することができます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-168">After you've edited an asset, follow these steps to move the edited asset back to the Shared asset library so that it can be promoted to the **Organization** scope and shared with multiple customers.</span></span>

1. <span data-ttu-id="e4f2c-169">プロジェクト レベルのアセット ライブラリで、インポートするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-169">In the project-level Asset library, select the tab for the asset type to import.</span></span>
2. <span data-ttu-id="e4f2c-170">保存する資産を選択し、**ライブラリに保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-170">Select the asset to save, and then click **Save to my library**.</span></span>

<span data-ttu-id="e4f2c-171">資産が、プロジェクト レベルのアセット ライブラリから共有アセット ライブラリに再び保存され、範囲が **自分自身** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-171">The asset is saved from the project-level Asset library back to the Shared asset library, and the scope is set to **Me**.</span></span>

## <a name="asset-library-preview"></a><span data-ttu-id="e4f2c-172">資産ライブラリ (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="e4f2c-172">Asset library (Preview)</span></span> 
<span data-ttu-id="e4f2c-173">資産ライブラリのパフォーマンスと信頼性を向上させるために、資産ライブラリのプレビュー バージョンを有効にすると、ページ読み込みエクスペリエンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-173">To improve the performance and reliability of the Asset library, we’re enabling a Preview version of the Asset library with an improved page loading experience.</span></span> 

<span data-ttu-id="e4f2c-174">資産ライブラリのプレビュー バージョンは、すべての LCS 地域およびプロジェクト タイプの **共有アセット ライブラリ** と **プロジェクト レベルのアセット ライブラリ** の両方で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-174">The Preview version of the Asset library will be available for both the **Shared asset library** and the **project-level Asset library** across all LCS regions and project types.</span></span> 

<span data-ttu-id="e4f2c-175">資産ライブラリ (プレビュー) は、すべてのタイプの資産をサポートし、いくつかの拡張機能を加えた同じ機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-175">The Asset library (Preview) supports all types of assets and has the same functionalities with a few enhancements:</span></span>

- <span data-ttu-id="e4f2c-176">**オンデマンド資産負荷**: ページの読み込み時間を短縮するために、アクセスする資産タイプを選択するまで、資産ライブラリ ページの読み込み時に既定の資産が表示されません。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-176">**Asset load on demand**: To reduce the page loading time, there will be no default asset displayed upon loading the asset library page until you select the asset type that you want to access.</span></span> <span data-ttu-id="e4f2c-177">また、資産タイプ間を移動するために、資産ライブラリ ページ全体の読み込みが完了するまで待つ必要もありません。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-177">Also, you won’t need to wait until the entire asset library page completes loading to navigate through the asset types.</span></span>
- <span data-ttu-id="e4f2c-178">**ファイル資産の更新**: ファイルの一覧を更新するために新しい更新ボタンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-178">**Refresh for file assets**:  A new refresh button is added to refresh a file list.</span></span> <span data-ttu-id="e4f2c-179">ページ全体を更新する必要なく、ファイル資産の一覧を更新できます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-179">You’ll be able to refresh a file asset list without having to refresh the entire page.</span></span> 

<span data-ttu-id="e4f2c-180">プレビュー バージョンを試している間でも既存の資産ライブラリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-180">You can still access the existing Asset library while trying out the Preview version.</span></span> <span data-ttu-id="e4f2c-181">新しいエクスペリエンスに完全に切り替える前に、翌月のプレビュー期間中のパフォーマンスと使用状況を監視し、既知の問題に対処します。</span><span class="sxs-lookup"><span data-stu-id="e4f2c-181">We’ll monitor the performance and usage during the preview period for the coming month and address any known issues before we switch to the new experience permanently.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
