---
title: "アセット ライブラリ (LCS)"
description: "このトピックでは、Lifecycle Services (LCS) のアセット ライブラリ機能について説明します。"
author: manalidongre
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 266824
ms.assetid: 
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dd3951b365ce36dc10737a55a2e0b0594bce7618
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="asset-library-lcs"></a><span data-ttu-id="a6e21-103">アセット ライブラリ (LCS)</span><span class="sxs-lookup"><span data-stu-id="a6e21-103">Asset library (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6e21-104">アセット ライブラリは、Microsoft Dynamics Lifecycle Services (LCS) のテナントに関連付けられているさまざまな資産の保管場所です。</span><span class="sxs-lookup"><span data-stu-id="a6e21-104">The Asset library is a storage location for the various assets that are associated with a tenant in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a6e21-105">LCS には、共用資産ライブラリとプロジェクト レベルのアセット ライブラリの 2 種類のアセット ライブラリがあります。</span><span class="sxs-lookup"><span data-stu-id="a6e21-105">Two types of Asset library are available in LCS: the Shared asset library and the project-level Asset library.</span></span>

- <span data-ttu-id="a6e21-106">**共有資産ライブラリ** – 共有資産ライブラリは、Microsoft およびパートナーによって資産を共有するために複数のテナント、プロジェクト、および LCS の環境の間で 使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-106">**Shared asset library** – The Shared asset library is used by Microsoft and Partners to share assets across multiple tenants, projects, and environments in LCS.</span></span> <span data-ttu-id="a6e21-107">このライブラリは、LCS にサインインするすべてのユーザーがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-107">This library can be accessed by any user who signs in to LCS.</span></span> <span data-ttu-id="a6e21-108">共用資産ライブラリにアクセスするには、LCS にサイン インして、**共用資産ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-108">To access the Shared asset library, sign in to LCS, and then click the **Shared asset library** tile.</span></span>

    <span data-ttu-id="a6e21-109">[![共有アセット ライブラリ タイル](./media/SharedAssetLibrary.jpg)](./media/SharedAssetLibrary.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6e21-109">[![Shared asset library tile](./media/SharedAssetLibrary.jpg)](./media/SharedAssetLibrary.jpg)</span></span>

- <span data-ttu-id="a6e21-110">**プロジェクト レベルのアセット ライブラリ** – プロジェクト レベルの資産ライブラリは、LCS のプロジェクト内の環境全体で資産を共有するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-110">**Project-level Asset library** – The project-level Asset library is used to share assets across environments within a project in LCS.</span></span> <span data-ttu-id="a6e21-111">このライブラリはプロジェクト内のすべてのユーザーがアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-111">This library can be accessed by all users within a project.</span></span> <span data-ttu-id="a6e21-112">。プロジェクト レベルのアセット ライブラリにアクセスするには、LCS にサイン インし、プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-112">To access the project-level Asset library, sign in to LCS, and open a project.</span></span> <span data-ttu-id="a6e21-113">ハンバーガー メニューで、**アセット ライブラリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-113">Then, on the hamburger menu, click **Asset library**.</span></span>

    <span data-ttu-id="a6e21-114">[![プロジェクト レベル資産ライブラリを開きます](./media/ProjectAssetLibrary.jpg)](./media/ProjectAssetLibrary.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6e21-114">[![Opening the project-level Asset library](./media/ProjectAssetLibrary.jpg)](./media/ProjectAssetLibrary.jpg)</span></span>

## <a name="asset-library-support"></a><span data-ttu-id="a6e21-115">アセット ライブラリ サポート</span><span class="sxs-lookup"><span data-stu-id="a6e21-115">Asset library support</span></span>
<span data-ttu-id="a6e21-116">アセット ライブラリは、複数のタイプの資産をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a6e21-116">The Asset library supports multiple types of assets.</span></span> <span data-ttu-id="a6e21-117">頻繁に使用されるいくつかの資産タイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-117">Here are some asset types that are frequently used:</span></span>

- <span data-ttu-id="a6e21-118">**ソフトウェア配置可能パッケージ** – この資産のタイプは、環境を最新のアップデートセットで更新するために使用されるすべてのパッケージを表します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-118">**Software deployable package** – This asset type represents all the packages that are used to update an environment with the latest set of updates.</span></span>
- <span data-ttu-id="a6e21-119">**データ パッケージ** - このアセット タイプは、コンフィギュレーションおよびデータ管理に使用されるアセットを格納します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-119">**Data package** – This asset type stores assets that are used for configuration and data management.</span></span>
- <span data-ttu-id="a6e21-120">**GER コンフィギュレーション** – この資産タイプは、クライアントに適用されるすべてのローカライズおよび翻訳資産を格納します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-120">**GER Configuration** – This asset type stores all localization and translation assets that are applied to the client.</span></span>
- <span data-ttu-id="a6e21-121">**Dynamics 365 for Retail SDK** - この資産タイプには Retail ソフトウェアの開発キット (SDK) の最新のスクリプトがすべて格納されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-121">**Dynamics 365 for Retail SDK** – This asset type stores all the latest scripts for the Retail software development kit (SDK).</span></span>

### <a name="asset-scopes"></a><span data-ttu-id="a6e21-122">アセット スコープ</span><span class="sxs-lookup"><span data-stu-id="a6e21-122">Asset scopes</span></span>
<span data-ttu-id="a6e21-123">アセット ライブラリがサポートするすべての資産には複数のスコープがあります。</span><span class="sxs-lookup"><span data-stu-id="a6e21-123">Every asset that the Asset library supports has multiple scopes.</span></span> <span data-ttu-id="a6e21-124">サポートされる資産スコープのいくつかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-124">Here are some of the supported asset scopes:</span></span>

- <span data-ttu-id="a6e21-125">**自分自身** – 資産は、アップロードされるときに、**自分自身**スコープに設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-125">**Me** – When an asset is uploaded, it's set to the **Me** scope.</span></span> <span data-ttu-id="a6e21-126">**Me** スコープの資産は、資産をアップロードしたユーザーにのみに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-126">An asset that has the **Me** scope is visible only to the person who uploaded the asset.</span></span>
- <span data-ttu-id="a6e21-127">**プロジェクト** – プロジェクトを**グローバル** スコープから別のプロジェクトにインポートすると、**プロジェクト** スコープに設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-127">**Project** – When a project is imported from the **Global** scope to another project, it's set to the **Project** scope.</span></span>
- <span data-ttu-id="a6e21-128">**組織** – テナント内の複数のユーザーで資産を共有するとき、テナント管理は、資産を**組織**スコープに昇格できます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-128">**Organization** – When an asset must be shared with multiple users within a tenant, the tenant admin can promote the asset to the **Organization** scope.</span></span>
- <span data-ttu-id="a6e21-129">**グローバル** – Microsoft だけが資産を**グローバル** スコープにアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-129">**Global** – Only Microsoft can upload assets to the **Global** scope.</span></span> <span data-ttu-id="a6e21-130">これらのアセットは、Microsoft がすべての LCS プロジェクトおよびユーザーに公に利用されることを望むアセットです。</span><span class="sxs-lookup"><span data-stu-id="a6e21-130">These assets are assets that Microsoft wants to be made publicly available to all LCS projects and users.</span></span>

### <a name="asset-status"></a><span data-ttu-id="a6e21-131">アセット ステータス</span><span class="sxs-lookup"><span data-stu-id="a6e21-131">Asset status</span></span>
<span data-ttu-id="a6e21-132">すべての資産には**ドラフト**または**発行済**の 2 つ状態のどちらかがあります。</span><span class="sxs-lookup"><span data-stu-id="a6e21-132">Every asset has one of two statuses: **Draft** or **Published**.</span></span>

- <span data-ttu-id="a6e21-133">**ドラフト** - 資産はまだ編集できます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-133">**Draft** – The asset can still be edited.</span></span>
- <span data-ttu-id="a6e21-134">**公開済** – 資産は、**組織**または**グローバル** スコープ、および編集を完了します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-134">**Published** – The asset is published at an **Organization** or **Global** scope, and edits are completed.</span></span>

## <a name="actions-in-the-asset-library"></a><span data-ttu-id="a6e21-135">資産ライブラリのアクション</span><span class="sxs-lookup"><span data-stu-id="a6e21-135">Actions in the Asset library</span></span>
<span data-ttu-id="a6e21-136">必要に応じてアセット ライブラリでさまざまなアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-136">You can perform various actions in the Asset library as you require.</span></span>

### <a name="upload-an-asset-to-the-asset-library"></a><span data-ttu-id="a6e21-137">アセットをアセット ライブラリにアップロード</span><span class="sxs-lookup"><span data-stu-id="a6e21-137">Upload an asset to the Asset library</span></span>
1. <span data-ttu-id="a6e21-138">資産をアップロードするタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-138">Select the tab to upload the asset to.</span></span>
2. <span data-ttu-id="a6e21-139">プラス記号 (**+**) をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="a6e21-139">Click the plus sign (**+**).</span></span>
3. <span data-ttu-id="a6e21-140">資産の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-140">Enter a name and description for the asset.</span></span>
4. <span data-ttu-id="a6e21-141">アセットのファイルをアップロードし、**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-141">Upload the file for the asset, and then click **Confirm**.</span></span>

### <a name="upload-a-new-version-for-a-specific-asset"></a><span data-ttu-id="a6e21-142">特定のアセットの新しいバージョンをアップロード</span><span class="sxs-lookup"><span data-stu-id="a6e21-142">Upload a new version for a specific asset</span></span>
1. <span data-ttu-id="a6e21-143">アセット ライブラリで資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-143">Select the asset in the Asset library.</span></span>
2. <span data-ttu-id="a6e21-144">ツール バーで、**アップロード**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-144">On the toolbar, click the **Upload** button.</span></span>
3. <span data-ttu-id="a6e21-145">前の手順の手順を繰り返し、「資産を資産ライブラリにアップロード」します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-145">Repeat the steps in the previous procedure, "Upload an asset to the asset library."</span></span>
4. <span data-ttu-id="a6e21-146">ツール バーで、**バージョン**をクリックして、単一の資産の複数のバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-146">On the toolbar, click **Versions** to view multiple versions for a single asset.</span></span>

### <a name="move-assets-from-the-global-asset-library-to-the-project-level-asset-library"></a><span data-ttu-id="a6e21-147">グローバル アセット ライブラリからプロジェクト レベルのアセット ライブラリへのアセット移動</span><span class="sxs-lookup"><span data-stu-id="a6e21-147">Move assets from the Global asset library to the project-level Asset library</span></span>
<span data-ttu-id="a6e21-148">グローバル アセット ライブラリからプロジェクト レベル アセット ライブラリにアセットを移動するには、アセットをインポートするかコピーするかの 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="a6e21-148">There are two ways to move an asset from the Global asset library to the project-level asset library: you can import the asset or copy it.</span></span>

#### <a name="import-from-the-global-asset-library"></a><span data-ttu-id="a6e21-149">グローバル アセット ライブラリからのインポート</span><span class="sxs-lookup"><span data-stu-id="a6e21-149">Import from the Global asset library</span></span>
<span data-ttu-id="a6e21-150">グローバル アセット ライブラリからの資産をプロジェクト レベルのアセット ライブラリへインポートして、環境間で適用できるようにするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a6e21-150">Follow these steps to import an asset from the Global asset library to the project-level Asset library so that it can be applied across environments.</span></span>

1. <span data-ttu-id="a6e21-151">プロジェクト レベルのアセット ライブラリで、インポートするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-151">In the project-level Asset library, select the tab for the asset type to import.</span></span>
2. <span data-ttu-id="a6e21-152">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-152">Click **Import**.</span></span>
3. <span data-ttu-id="a6e21-153">共有アセット ライブラリのアセットの一覧で、インポートするアセットを選択してから**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-153">In the list of assets in the Shared asset library, select the asset to import, and then click **Pick**.</span></span>

<span data-ttu-id="a6e21-154">選択したアセットをインポートし、プロジェクト レベルのアセット ライブラリに配置します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-154">The selected asset is imported and put into the project-level Asset library.</span></span> <span data-ttu-id="a6e21-155">プロジェクト レベルのアセット ライブラリのアセットの状態は **公開済** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a6e21-155">The status of the asset in the project-level Asset library is set to **Published**.</span></span> <span data-ttu-id="a6e21-156">このメソッドは、編集する予定のないパッケージを対象としています。</span><span class="sxs-lookup"><span data-stu-id="a6e21-156">This method is for packages that you don't plan to edit.</span></span> <span data-ttu-id="a6e21-157">インポートされたパッケージを編集する場合は、次の手順を使用して、コピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-157">If you want to edit an imported package, create a copy by using the following procedure.</span></span> <span data-ttu-id="a6e21-158">パッケージの状態は **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="a6e21-158">The status of the package will then be **Draft**.</span></span>

#### <a name="copy-from-the-global-asset-library"></a><span data-ttu-id="a6e21-159">グローバル アセット ライブラリからのコピー</span><span class="sxs-lookup"><span data-stu-id="a6e21-159">Copy from the Global asset library</span></span>
<span data-ttu-id="a6e21-160">資産のコピーを編集できるよう作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a6e21-160">Follow these steps to create a copy of an asset so that it can be edited.</span></span>

1. <span data-ttu-id="a6e21-161">プロジェクト レベルのアセット ライブラリで、コピーするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-161">In the project-level Asset library, select the tab for the asset type to copy.</span></span>
2. <span data-ttu-id="a6e21-162">コピーするアセットを選択し、ツール バーで **コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-162">Select the asset to copy, and then, on the toolbar, click **Copy**.</span></span>

<span data-ttu-id="a6e21-163">発行済みのアセットのコピーが作成され、状態は **Draft** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a6e21-163">A copy of the published asset is created, and the status is set to **Draft**.</span></span>

### <a name="save-to-my-library"></a><span data-ttu-id="a6e21-164">自分のライブラリに保存</span><span class="sxs-lookup"><span data-stu-id="a6e21-164">Save to my library</span></span>
<span data-ttu-id="a6e21-165">アセットを編集した後、以下の手順に従って編集したアセットを共有アセット ライブラリに戻し、**組織**スコープを促進させることにより複数の顧客と共有することができます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-165">After you've edited an asset, follow these steps to move the edited asset back to the Shared asset library so that it can be promoted to the **Organization** scope and shared with multiple customers.</span></span>

1. <span data-ttu-id="a6e21-166">プロジェクト レベルのアセット ライブラリで、インポートするアセット タイプのタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e21-166">In the project-level Asset library, select the tab for the asset type to import.</span></span>
2. <span data-ttu-id="a6e21-167">保存する資産を選択し、**ライブラリに保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e21-167">Select the asset to save, and then click **Save to my library**.</span></span>

<span data-ttu-id="a6e21-168">資産が、プロジェクト レベルのアセット ライブラリから共有アセット ライブラリに再び保存され、範囲が **自分自身** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a6e21-168">The asset is saved from the project-level Asset library back to the Shared asset library, and the scope is set to **Me**.</span></span>

