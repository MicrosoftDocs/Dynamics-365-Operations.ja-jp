---
title: "バージョン 8.0 から 8.1 への環境の更新"
description: "このトピックでは、8.1 アプリケーション リリースに既存の Finance and Operations 8.0 環境を更新するために必要な手順について説明します。"
author: laneswenka
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 96fbd10d5e1b36057b73a41cc2dad6cda475b45f
ms.contentlocale: ja-jp
ms.lasthandoff: 10/05/2018

---

# <a name="update-environments-from-version-80-to-81"></a><span data-ttu-id="3e0a4-103">バージョン 8.0 から 8.1 への環境の更新</span><span class="sxs-lookup"><span data-stu-id="3e0a4-103">Update environments from version 8.0 to 8.1</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e0a4-104">このトピックでは、8.1 アプリケーション リリースに既存の Dynamics 365 for Finance and Operations 8.0 環境を更新するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-104">This topic explains the steps required to update existing Dynamics 365 for Finance and Operations 8.0 environments to the 8.1 application release.</span></span>

> [!NOTE]
> <span data-ttu-id="3e0a4-105">8.1 バイナリ更新プログラム パッケージは、2018 年 10 月 15 日より後に利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-105">The 8.1 binary update package will be available after October 15, 2018.</span></span> <span data-ttu-id="3e0a4-106">このパッケージは、手順 5 ～ 7 に影響を与えます。つまり、2018 年 10 月 1 日より後に手順 1 ～ 4 を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-106">This package impacts steps 5-7, which means that steps 1-4 can be started after October 1, 2018.</span></span>

## <a name="background"></a><span data-ttu-id="3e0a4-107">バックグラウンド</span><span class="sxs-lookup"><span data-stu-id="3e0a4-107">Background</span></span>

<span data-ttu-id="3e0a4-108">従来、アプリケーションの新しいバージョンへの移行には、追加の仮想マシンの展開、コード アップグレード、データ アップグレード、および Microsoft Dynamics サービス エンジニアリング (DSE) チームとの数日前の事前スケジューリングを含む厳格なアップグレードが必要でした。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-108">Traditionally, moving to a newer application version has involved a rigorous upgrade that includes deployment of additional virtual machines, code upgrade, data upgrade, and scheduling several days in advance with the Microsoft Dynamics Service Engineering (DSE) team.</span></span>  <span data-ttu-id="3e0a4-109">最新バージョンの取得がより簡単になっており、これは継続的に改善されていきます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-109">You will notice that we are making the uptake of the latest version simpler, and this will continue to improve over time.</span></span>

<span data-ttu-id="3e0a4-110">このために、フル アップグレードと比較した場合の更新エクスペリエンスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-110">To this end, we are supporting an update experience as compared to a full upgrade.</span></span>  <span data-ttu-id="3e0a4-111">これは、8.0 および 8.1 アプリケーション スキーマ間にはデータ アップグレードまたはコード アップグレードの手順が存在しないために可能です。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-111">This is possible because there are no Data Upgrade or Code Upgrade steps between the 8.0 and 8.1 application schema.</span></span>  <span data-ttu-id="3e0a4-112">プラットフォーム アップデートを適用するのと同じように、対象となる環境が更新されます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-112">The target environments will be updated just like you would apply a Platform update.</span></span>

<span data-ttu-id="3e0a4-113">バージョン 8.0 から 8.1 に更新するプロセスの概要は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-113">The high-level process to update from version 8.0 to 8.1 includes the following:</span></span>

1. <span data-ttu-id="3e0a4-114">8.1 開発者環境とビルド環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-114">Deploy 8.1 developer and build environments.</span></span>
2. <span data-ttu-id="3e0a4-115">バージョン管理を分岐し、アプリケーション修正プログラムを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-115">Branch in version control and remove any application hotfixes.</span></span>
3. <span data-ttu-id="3e0a4-116">カスタム拡張機能や ISV ソリューションを再コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-116">Recompile custom extensions and/or ISV solutions.</span></span>
4. <span data-ttu-id="3e0a4-117">1 つのソフトウェア展開可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-117">Produce a single software deployable package.</span></span>
5. <span data-ttu-id="3e0a4-118">展開可能パッケージを 8.1 バイナリ アップデート パッケージとマージします。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-118">Merge a deployable package with the 8.1 binary update package.</span></span>
6. <span data-ttu-id="3e0a4-119">検証用の対象環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-119">Deploy to target environments for validation.</span></span>
7. <span data-ttu-id="3e0a4-120">生産環境に展開します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-120">Deploy to Production.</span></span>

## <a name="deploy-81-developer-and-build-environments"></a><span data-ttu-id="3e0a4-121">8.1 開発者環境とビルド環境を展開</span><span class="sxs-lookup"><span data-stu-id="3e0a4-121">Deploy 8.1 developer and build environments</span></span>
<span data-ttu-id="3e0a4-122">Lifecycle Services を使用して 1 つ以上の開発者環境と 1 つの新しいビルド環境をアプリケーション 8.1リリースに展開します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-122">Using Lifecycle Services, deploy at least one developer environment and a single, new build environment on application 8.1 release.</span></span>

<span data-ttu-id="3e0a4-123">平均では、これには 3 ～ 4 時間かかり、同時に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-123">On average this takes 3-4 hours and can be done simultaneously.</span></span> <span data-ttu-id="3e0a4-124">ビルド環境で、**エージェント プールの新規作成**を行い、**詳細オプション** 画面でこの環境に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-124">For the build environment, **Create a new agent pool** and assign it to this environment on the **Advanced options** screen.</span></span>

<span data-ttu-id="3e0a4-125">Azure DevOps で、既存のビルド定義にアクセスし、8.1 用の新しいエージェント プールを使用していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-125">In Azure DevOps, visit your existing Build Definition and ensure that it is not using your new agent pool for 8.1.</span></span> <span data-ttu-id="3e0a4-126">これにより、新しいビルド エージェントが古いアプリケーション コードをコンパイルしようとしなくなります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-126">This will keep your new build agent from trying to compile older application code.</span></span>

## <a name="begin-branch-work-for-version-control-and-remove-any-application-hotfixes"></a><span data-ttu-id="3e0a4-127">バージョン管理の分岐作業を開始し、アプリケーション修正プログラムを削除</span><span class="sxs-lookup"><span data-stu-id="3e0a4-127">Begin branch work for version control and remove any application hotfixes</span></span>
<span data-ttu-id="3e0a4-128">新しい環境が展開されるとき、更新の分岐作業を開始します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-128">While the new environments are deploying, begin the branching work for your update.</span></span> <span data-ttu-id="3e0a4-129">例として、バージョン管理での次の分岐構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-129">Use the following branch structure in version control as an example.</span></span>  <span data-ttu-id="3e0a4-130">分岐の設計は顧客ごとに異なりますので、分岐の設定に基づき、それに応じてステップを調整するように注意してください。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-130">Branching design varies for each customer, so be careful to adjust your steps accordingly based on how your branches are set up.</span></span>

<span data-ttu-id="3e0a4-131">[![VersionControl](./media/VersionControl.png)](./media/VersionControl.png)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-131">[![VersionControl](./media/VersionControl.png)](./media/VersionControl.png)</span></span>

### <a name="prepare-using-visual-studio"></a><span data-ttu-id="3e0a4-132">Visual Studio の使用準備</span><span class="sxs-lookup"><span data-stu-id="3e0a4-132">Prepare using Visual Studio</span></span>
<span data-ttu-id="3e0a4-133">その他の開発コンピューター (展開される新規コンピューター以外) で、Visual Studio を開き、ソース管理エクスプローラーに移動します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-133">On any other development machine (other than the new ones being deployed), open Visual Studio and visit the Source Control Explorer.</span></span> <span data-ttu-id="3e0a4-134">8.1 更新用に分離される新しい分岐を作成します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-134">You will create a new branch that will be isolated for the 8.1 update.</span></span>

<span data-ttu-id="3e0a4-135">[![BranchFor81](./media/BranchFor81.png)](./media/BranchFor81.png)</span><span class="sxs-lookup"><span data-stu-id="3e0a4-135">[![BranchFor81](./media/BranchFor81.png)](./media/BranchFor81.png)</span></span>

<span data-ttu-id="3e0a4-136">次に、この分岐で Microsoft パッケージ フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-136">Next, delete any Microsoft package folders in this branch.</span></span> <span data-ttu-id="3e0a4-137">削除する必要のある 8.0 での修正プログラムの適用するからチェックインした、ApplicationSuite などのパッケージがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-137">You may have packages, such as ApplicationSuite, checked in from applying hotfixes on 8.0 which need to be removed.</span></span> <span data-ttu-id="3e0a4-138">カスタム パッケージまたは ISV が残っているときのみ、分岐にこれらの変更をチェックインします。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-138">When only your custom packages or ISVs remain, check these changes in to the branch.</span></span>

>[!Important]
> <span data-ttu-id="3e0a4-139">バージョン管理ワークスペースを新しい開発環境にマップする前に、これを行うことが重要です。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-139">It is critical that this is done before you map version control workspaces on your new development environments.</span></span> <span data-ttu-id="3e0a4-140">これは、Microsoft 修正プログラムが削除されて、作業環境に伝播され、手を触れていない 8.1 アプリケーション コードが削除されることのないようにすることです。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-140">This is to avoid the deletion of the Microsoft hotfixes to cascade to your working environment and delete untouched 8.1 application code.</span></span>

## <a name="recompile-custom-extensions-andor-isv-solutions"></a><span data-ttu-id="3e0a4-141">カスタム拡張機能や ISV ソリューションを再コンパイル</span><span class="sxs-lookup"><span data-stu-id="3e0a4-141">Recompile custom extensions and/or ISV solutions</span></span>
<span data-ttu-id="3e0a4-142">新しい開発環境にこの分岐をマッピングし、ソース コードが提供される場合に拡張および ISV ソリューションをコンパイルする準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-142">Now you are ready to map this branch to a new development environment and compile your extensions and ISV solutions if they have provided you with source code.</span></span>  <span data-ttu-id="3e0a4-143">ISV が提供されたバイナリ パッケージのみ持っている場合、それらをソース管理にチェックインできます。ビルド環境では、1 つのソフトウェア展開可能パッケージを生産するために、拡張パッケージとバイナリが結合されます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-143">If your ISVs have only provided binary packages, you can check them in to source control, and the build environment will merge the binaries with your extension package to produce a single software deployable package.</span></span> <span data-ttu-id="3e0a4-144">このプロセスの追加の情報は、[サード パーティからの展開可能パッケージ](../dev-tools/manage-runtime-packages.md#deployable-packages-from-third-parties)にあります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-144">Additional information on this process can be found at [Deployable packages from third parties](../dev-tools/manage-runtime-packages.md#deployable-packages-from-third-parties).</span></span>  <span data-ttu-id="3e0a4-145">これは、後で 8.1 バイナリ アップデートとパッケージを結合するときに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-145">This will help later when you merge your package with the 8.1 binary update.</span></span>

>[!NOTE]
> <span data-ttu-id="3e0a4-146">この**ステップは必要**です。8.1 アプリケーション コードにはバイナリ レベルから 8.0 との互換性がないためです。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-146">This **step is necessary** as the 8.1 application code is not backward compatible with 8.0 from a binary level.</span></span> <span data-ttu-id="3e0a4-147">アプリケーションの将来のリリースでは、この手順はオプションとなります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-147">In future application releases this step will be optional.</span></span>

## <a name="produce-a-single-software-deployable-package"></a><span data-ttu-id="3e0a4-148">1 つのソフトウェア展開可能パッケージを作成</span><span class="sxs-lookup"><span data-stu-id="3e0a4-148">Produce a single software deployable package</span></span>
<span data-ttu-id="3e0a4-149">開発者環境でコンパイルし、解決するためのエラーがない場合、以前設定した新しい 8.1 ビルド環境エージェントを使用して Azure DevOps でビルドを開始します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-149">After you have compiled in a developer environment and there are no errors to resolve, start a build in Azure DevOps using your new 8.1 build environment agent that was setup earlier.</span></span> <span data-ttu-id="3e0a4-150">これが完了したら、展開可能パッケージ コンポーネントがビルド結果に添付されます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-150">When this is complete, a deployable package artifact will be attached to your build results.</span></span> <span data-ttu-id="3e0a4-151">このパッケージをダウンロードして、Lifecycle Services アセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-151">Download this package and upload it to the Lifecycle Services Asset Library.</span></span>  <span data-ttu-id="3e0a4-152">この 1 つのパッケージに、拡張機能と ISV ソリューションがすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-152">This single package should have all of your extensions and ISV solutions.</span></span>

## <a name="merge-the-deployable-package-with-the-81-binary-update-package"></a><span data-ttu-id="3e0a4-153">展開可能パッケージを 8.1 バイナリ アップデート パッケージとマージ</span><span class="sxs-lookup"><span data-stu-id="3e0a4-153">Merge the deployable package with the 8.1 binary update package</span></span>
<span data-ttu-id="3e0a4-154">Lifecycle Services で、生産 8.0 環境の詳細ページを参照します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-154">In Lifecycle Services, visit your Production 8.0 environment details page.</span></span> <span data-ttu-id="3e0a4-155">**すべてのバイナリ更新プログラム** タイルに、8.1 アプリケーション リリースのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-155">On the **All binary updates** tile, you will see an option for the 8.1 Application release.</span></span> <span data-ttu-id="3e0a4-156">アセット ライブラリにこのパッケージを保存します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-156">Save this package to your Asset Library.</span></span>  

<span data-ttu-id="3e0a4-157">アセット ライブラリで、保存したばかりの新しい 8.1 ソフトウェア展開可能パッケージと 8.1 バイナリ更新プログラム パッケージの両方を検索します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-157">In the Asset Library, find both your new 8.1 software deployable package and the 8.1 binary update package that was just saved.</span></span>  <span data-ttu-id="3e0a4-158">両方のパッケージを強調表示し、**マージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-158">Highlight both packages and select **Merge**.</span></span> <span data-ttu-id="3e0a4-159">これにより、ファイルが、マージされた更新パッケージに結合されます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-159">This will combine the files in to a merged update package.</span></span>  <span data-ttu-id="3e0a4-160">このパッケージをさまざまなテスト環境に適用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-160">You are now ready to apply this package to your various test environments.</span></span>

## <a name="deploy-to-target-environments-for-validation"></a><span data-ttu-id="3e0a4-161">検証用の対象環境を展開</span><span class="sxs-lookup"><span data-stu-id="3e0a4-161">Deploy to target environments for validation</span></span>
<span data-ttu-id="3e0a4-162">マージされた更新パッケージを使用して、これをさまざまなテスト環境に展開します。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-162">Using the merged update package, deploy this to your various test environments.</span></span>  <span data-ttu-id="3e0a4-163">この方法の詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-163">For more on how to do this, see [Apply updates to cloud environments](../deployment/apply-deployable-package-system.md).</span></span>  <span data-ttu-id="3e0a4-164">少なくとも、サブスクリプションに付属しているサンドボックス第 2 層環境に展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-164">At a minimum, you must deploy this to the sandbox Tier-2 environment that comes with your subscription.</span></span>  <span data-ttu-id="3e0a4-165">検証が完了したら、マージされた更新パッケージをリリース候補としてマークします。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-165">After you have finished with validation, mark the merged update package as a Release Candidate.</span></span>

## <a name="deploy-to-production"></a><span data-ttu-id="3e0a4-166">生産環境に展開</span><span class="sxs-lookup"><span data-stu-id="3e0a4-166">Deploy to Production</span></span>
<span data-ttu-id="3e0a4-167">アセット ライブラリでリリース候補をマークしたら、実稼働環境への展開をスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-167">After you have marked the Release Candidate in your Asset Library, you can schedule the deployment to your Production environment.</span></span>  <span data-ttu-id="3e0a4-168">これは、他のソフトウェア展開可能パッケージの適用と同じプロセスに従います。</span><span class="sxs-lookup"><span data-stu-id="3e0a4-168">This will follow the same process for applying other software deployable packages.</span></span>

